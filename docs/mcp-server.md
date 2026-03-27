# Third Bridge MCP Server

## Overview

The **Third Bridge MCP Server** exposes read-only access to a curated subset of Third Bridge investment research content via the Model Context Protocol (MCP). It is designed for:

- High-quality, citation-focused investment research in Claude and other MCP-compatible clients.
- Deep Research workflows that need structured content snippets.
- Safe, auditable use of proprietary Third Bridge content with strict non-destructive semantics.

## Capabilities

The server implements the following MCP capabilities:

- **Tools**
  - Custom tools with full MCP tool definitions and JSON input/output schemas.
  - Tool list is dynamically discoverable (`capabilities.tools.listChanged: true`).
- **Prompts**
  - Custom server-side prompts for research and debugging workflows.
  - Prompt list is dynamically discoverable (`capabilities.prompts.listChanged: true`).

## Tool Catalog

All tools follow Anthropic’s MCP tool conventions and include mandatory safety annotations:

- `readOnlyHint: true`
- `destructiveHint: false`
- `openWorldHint: false` (corpus is closed to the configured Third Bridge knowledge base)

### 1. `third_bridge_content_query`

- **Title**: `Third Bridge Content Query (TBCQ)`
- **Role**: Primary semantic retrieval tool for investment research use cases.

## Prompts

The server ships with two key prompt templates:

- **`ThirdBridgePublicAnswerPrompt` (`research.prompt.ts`)**
  - Main production prompt for investment insight generation.
  - Ensures responses:
    - Use only retrieved Third Bridge snippets.
    - Follow TBCF citation rules (clickable markdown citations, one index per unique source).
    - Adopt the tone and structure of professional institutional research.

- **`ThirdBridgePublicDebugAnswerPrompt` (`debug.prompt.ts`)**
  - Debugging-oriented variant used for inspection and troubleshooting.
  - Surfaces additional internal details about retrieval passes and snippet usage.

Both prompts are exposed through the MCP prompt capability so that compatible clients can list and select them.

## Authentication
This server requires OAuth authentication. You must be Third Bridge Forum user with proper permissions to access the content.

## Usage Examples

Below are example flows that illustrate how to use this server in practice. Each example assumes a Claude or MCP-compatible client where tools can be invoked programmatically or via UI.

### Example 1: Standard Investment Q&A with Citations (Recommended)

1. The user asks:
   “What are the key competitive advantages of NVIDIA in data center GPUs over the last 3 years?”
2. The assistant:
   - Calls `third_bridge_content_query` with:
     - `topic`: “NVIDIA data center GPUs competitive advantages”
     - `companyNames`: `["NVIDIA"]`
     - `companyTickers`: `["NVDA"]`
     - `sectors`: `["Semiconductors"]`
     - Default date window: last 36 months.
3. The tool returns a JSON payload with `results[]` containing `contentSnippets` and URLs.
4. The assistant writes a structured answer:
   - Executive summary.
   - Thematic breakdown (technology, ecosystem, pricing, supply chain).
   - Every sentence backed by snippets ends with a TBCF citation such as:
     `[[1]](https://example.thirdbridge.com/doc1 "NVIDIA data center interview, Q2 2024")`.

### Example 2: Multi-Topic Equity Research Overview

1. The user asks:
   “Compare the demand outlook over the next 2 years for TSMC and Samsung Foundry in advanced nodes.”
2. The assistant:
   - Splits the question into two topics: TSMC advanced nodes, Samsung Foundry advanced nodes.
   - Issues **two** `third_bridge_content_query` calls, one per topic, reusing the user’s timeframe and sectors.
3. Each call returns topic-specific snippets with URLs and titles.
4. The assistant:
   - Builds a side-by-side comparison table.
   - Uses distinct citation indices for each underlying content source.
   - Clearly calls out where coverage is strong, mixed, or limited.

## Support
- Email: support@thirdbridge.com
- Documentation: https://github.com/third-bridge/mcp-skills/docs
- Issues: https://github.com/third-bridge/mcp-skills/issues