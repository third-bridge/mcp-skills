# Third Bridge MCP Server

## Overview

The **Third Bridge Public Content MCP Server** exposes read-only access to a curated subset of Third Bridge investment research content via the Model Context Protocol (MCP). It is designed for:

- High-quality, citation-focused investment research in Claude and other MCP-compatible clients.
- Deep Research workflows that need structured snippets and, when necessary, full-document retrieval.
- Safe, auditable use of proprietary Third Bridge content with strict non-destructive semantics.

The server is registered under:

- `serverName`: `public`
- `name`: `third-bridge-content`
- `title`: `Third Bridge Content Server`
- `version`: `1.2.0`

This server is public (no end-user authentication required) and internally scoped to the Third Bridge corpus configured for the target environment.

## Capabilities

The server implements the following MCP capabilities:

- **Tools**
  - Custom tools with full MCP tool definitions and JSON input/output schemas.
  - Tool list is dynamically discoverable (`capabilities.tools.listChanged: true`).
- **Prompts**
  - Custom server-side prompts for research and debugging workflows.
  - Prompt list is dynamically discoverable (`capabilities.prompts.listChanged: true`).
- **Resources**
  - Subscribable resources for future streaming updates (`capabilities.resources.subscribe: true`).
  - Resource list is dynamically discoverable (`capabilities.resources.listChanged: true`).

Every tool in this server is strictly read-only: there are **no** write, update, delete, or side-effecting operations against user data or Third Bridge systems.

## Tool Catalog

All tools follow Anthropic’s MCP tool conventions and include mandatory safety annotations:

- `readOnlyHint: true`
- `destructiveHint: false`
- `openWorldHint: false` (corpus is closed to the configured Third Bridge knowledge base)

### 1. `third_bridge_content_query`

- **Class**: `QueryTool`
- **Title**: `Third Bridge Content Query (TBCQ)`
- **Role**: Primary semantic retrieval tool for investment research use cases.
- **Scope**:
  - Allowed topics: company strategy, competitive dynamics, supply chain, macro trends, capital markets, ticker-driven research, and related institutional-investor questions.
  - Excluded topics: general knowledge, coding, math, entertainment, consumer advice, and non-financial domains.
- **Behavior**:
  - Breaks the user request into atomic topics and issues one tool call per topic.
  - For each topic, generates 1–3 natural-language queries incorporating entities, tickers, regions, and timeframes.
  - Applies filters such as `companyNames`, `companyTickers`, and `sectors` when provided.
  - Uses a multi-pass retrieval loop (baseline, date-window expansion, filter removal, query rewrite) to maximize snippet quality.
  - Returns curated content snippets designed for citation-based investment analysis.
- **Response format**:
  - Single MCP content item of type `text`.
  - Payload is a JSON string with a `results` array, each element containing metadata and `contentSnippets`.
  - Designed for strict Third Bridge Citations Format (TBCF): every snippet-backed sentence must include a clickable markdown citation.

**When to use**:

- Default choice for **investment Q&A**, equity research, and thematic analysis where high-quality snippets and citations are required.
- Use whenever the user is asking about financial markets, companies, or sectors and Third Bridge coverage is likely to exist.
- Do **not** use for general web search, generic trivia, or non-investment topics.

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

## Authentication Model

- This **public** content MCP server does **not** require end-user OAuth.
- All requests are processed under a backend-scoped identity using:
  - A configured `companyUuid` (via `ResourceEnvironmentUtils.CompanyUuid`).
  - Infrastructure modules for AppConfig, Bedrock, and S3.
- There is no user-specific data persistence, user profile storage, or write access to Third Bridge systems.

From the MCP Directory perspective:

- No OAuth 2.0 flow is needed for connector installation.
- No test user accounts are required; a single backend configuration is sufficient for validation.

## Data Sources and Storage

- **Primary corpus**: Third Bridge investment research content configured for the environment.
- **Retrieval infrastructure**:
  - AWS AppConfig for feature and environment configuration.
  - AWS Bedrock Knowledge Bases for semantic retrieval.
  - AWS Bedrock Reranking for improved result ordering (where applicable).
  - S3-backed knowledge base for content storage.
- **Data residency and caching**:
  - The server may leverage transient in-memory caching for performance.
  - No user-generated content is stored by this server beyond request/response lifecycles.
  - Third Bridge source documents remain in the underlying storage systems; this server only reads them.

The server never:

- Writes, updates, or deletes data in user accounts.
- Modifies Third Bridge source documents.
- Sends notifications, emails, or webhooks on behalf of users.

## Safety Annotations and Behavior

All tools are annotated as:

- `readOnlyHint: true`
- `destructiveHint: false`
- `openWorldHint: false`

This reflects the following behavioral guarantees:

- Tools **only read** from a fixed Third Bridge corpus and related search indices.
- No stateful mutation of user or provider data.
- No arbitrary outbound network calls beyond configured Third Bridge and AWS infrastructure.
- No capability to interact with external services such as email providers, webhooks, or messaging systems.

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

## Production Readiness

This MCP server is designed for production usage:

- **Stability**:
  - Backed by NestJS and a modular infrastructure (`PublicContentMcpServerModule`).
  - Uses AWS-managed services (AppConfig, Bedrock, S3) for configuration and retrieval.
- **Performance**:
  - Tools are stateless and horizontally scalable.
  - Retrieval is optimized for typical institutional research workloads.
- **Safety and compliance**:
  - Strictly read-only toolset with explicit MCP safety annotations.
  - Content scope is restricted to the Third Bridge corpus; no open web access.
- **Monitoring and debugging**:
  - Dedicated debug prompt for easier troubleshooting.
  - Clean separation between production and debug pathways.

## Support and Contact

For directory reviewers and integrators:

- **Technical contact**: [Your engineering contact or team]
- **Product contact**: [Your product/BD contact]
- **Documentation**: Replace this file with your canonical docs URL once deployed.

For end users, please follow your organization’s standard support channels when using Third Bridge content integrations.
