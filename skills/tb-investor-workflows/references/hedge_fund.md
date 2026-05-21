# Hedge Fund / Multi-Strategy Workflows

## Table of Contents
1. Catalyst Mapping
2. Pair Trade Construction
3. Thematic Screening
4. Activist Thesis Build
5. Short Thesis Construction
6. Event Arbitrage (M&A / Spin-off / IPO)

---

## 1. Catalyst Mapping

**When to use:** Identifying upcoming catalysts and their likely direction from expert evidence.
**Default horizon:** 1–6 months
**Complexity:** Medium (3–5 atomic questions, 6–12 MCP calls)

### Prompt Template

Using Third Bridge transcripts, build a **catalyst map** for **[Company]** over the next **1–6 months**. Identify the 3–5 most important upcoming events or inflection points (earnings, product launches, regulatory decisions, contract renewals, competitive entries, pricing resets, management changes) and assess the likely direction and magnitude of each based on expert evidence. For each catalyst, estimate whether the market is positioned correctly, and identify what transcript evidence suggests the consensus expectation is most likely to be wrong. Rank catalysts by expected impact on the stock and by the quality of the transcript evidence supporting the directional view.

### Retrieval Decomposition

1. Company + "launch" / "product" / "pipeline" / "approval" / "regulation"
2. Company + "contract" / "renewal" / "RFP" / "bid" / "win"
3. Company + "pricing" / "reset" / "renegotiation" / "cost"
4. Competitors for context on competitive catalysts

### Output Structure

**Catalyst Timeline**
| Catalyst | Expected Timing | Consensus View | Transcript View | Surprise Direction | Confidence | Source |
|----------|----------------|---------------|----------------|-------------------|------------|--------|

**Highest Conviction Catalyst:** The one event where transcript evidence most clearly diverges from market positioning.

**Position Sizing Implication:** How the evidence quality maps to conviction level.

---

## 2. Pair Trade Construction

**When to use:** Building a relative trade between two names using fundamental evidence.
**Default horizon:** 3–12 months
**Complexity:** High (6–10 atomic questions, 12–18 MCP calls)

### Prompt Template

Using Third Bridge transcripts, construct a **fundamental pair trade** between **[Long Candidate]** and **[Short Candidate]** within **[sector]**. Assess the relative strength of each name across demand trajectory, pricing power, customer loyalty, competitive position, management quality, margin trajectory, and capex needs. Identify the 3 most important dimensions where transcript evidence suggests the relative gap is wider (or narrower) than the market appreciates. Assess the key risk to the pair (what would cause convergence or reversal) and the expected timeframe for the thesis to play out.

### Retrieval Decomposition

For each name:
1. Company-specific fundamentals (demand, pricing, margin)
2. Customer/competitive perspective
3. Cross-reference both names in same transcripts where possible

### Output Structure

**Pair Trade Thesis**
| Dimension | Long Candidate | Short Candidate | Relative Edge | Source |
|-----------|---------------|----------------|--------------|--------|

**Core Thesis:** Why the relative gap exists and why it should narrow/widen.

**Key Risks to Pair**
- Convergence risk (what makes the short work against you)
- Correlation risk (what moves both names the same direction)

**Optimal Timeframe:** When transcript evidence suggests the thesis should materialise.

---

## 3. Thematic Screening

**When to use:** Identifying companies exposed to a macro or industry theme.
**Default horizon:** 12–36 months
**Complexity:** High (6–10 atomic questions, 12–20 MCP calls)

### Prompt Template

Using Third Bridge transcripts, screen for companies with the highest **positive and negative exposure** to **[theme: e.g., AI infrastructure spend, GLP-1 adoption, nearshoring, defence budget expansion, EV transition, rate sensitivity]**. Identify which companies experts describe as primary beneficiaries, which face displacement risk, and which are consensus beneficiaries but where transcript evidence suggests the upside is overestimated. For each name surfaced, assess the quality and recency of the transcript evidence, the magnitude of exposure, and whether the market appears to have fully priced the theme.

### Retrieval Decomposition

1. Theme keywords broadly (no company filter) to discover relevant names
2. Top surfaced companies searched individually for depth
3. "Loser" names searched for displacement/disruption evidence
4. Customer/supplier searches for independent validation of theme exposure

### Output Structure

**Theme Exposure Map**
| Company | Exposure Direction | Magnitude | Market Pricing | Evidence Quality | Source |
|---------|-------------------|-----------|---------------|-----------------|--------|

**Consensus Beneficiaries at Risk:** Names where transcript evidence challenges the bullish narrative.

**Non-Obvious Beneficiaries:** Names where transcript evidence suggests underappreciated exposure.

**Non-Obvious Losers:** Names where displacement risk isn't reflected in market pricing.

---

## 4. Activist Thesis Build

**When to use:** Building or evaluating an activist case on a specific company.
**Default horizon:** 6–24 months
**Complexity:** High (5–8 atomic questions, 12–18 MCP calls)

### Prompt Template

Using Third Bridge transcripts, assess the **activist opportunity** at **[Company]**. Identify expert evidence supporting or refuting the key levers an activist would target: operational inefficiency, capital misallocation, strategic misdirection, governance weaknesses, margin gap versus peers, underperforming divisions, excess cost structure, or undervalued asset base. Evaluate management's track record on capital allocation, strategic execution, and responsiveness to shareholder feedback. Assess the feasibility and timeline of an activist campaign based on the operational complexity of the recommended changes.

### Retrieval Decomposition

1. Company + "margin" / "efficiency" / "cost" / "overhead" / "underperforming"
2. Company + "management" / "capital allocation" / "strategy" / "governance"
3. Company + "division" / "segment" / "asset" / "divestiture" / "separation"
4. Peers for margin/efficiency benchmarking context
5. Former executives for internal operational perspective

### Output Structure

**Activist Lever Assessment**
| Lever | Opportunity Size | Feasibility | Timeline | Evidence | Source |
|-------|-----------------|------------|----------|----------|--------|

**Management Vulnerability Assessment:** Where leadership track record creates openings.

**Campaign Feasibility:** Operational complexity of proposed changes and likely board/management response.

**Downside Risk:** What could go wrong if an activist pushes these changes.

---

## 5. Short Thesis Construction

**When to use:** Building or validating a short case with independent evidence.
**Default horizon:** 3–12 months
**Complexity:** Medium-High (4–7 atomic questions, 10–16 MCP calls)

### Prompt Template

Using Third Bridge transcripts, construct or validate a **short thesis** on **[Company]**. Focus on evidence of: demand deterioration, pricing erosion, customer churn, competitive displacement, margin pressure, accounting quality concerns, management credibility gaps, or structural business model challenges. Prioritise evidence from customers (defecting or reducing spend), competitors (gaining share), and former employees (identifying internal problems). For each short driver, assess the likely timing and magnitude of impact, and identify what would invalidate the short thesis. Explicitly note where the bear case contradicts the most common bull arguments.

### Retrieval Decomposition

1. Company + "churn" / "loss" / "cancel" / "defection" / "switching"
2. Company + "pricing" / "discount" / "erosion" / "competition"
3. Company + "quality" / "accounting" / "add-back" / "adjustment" / "aggressive"
4. Competitors + "gain" / "win" / "taking share" / "displacement"
5. Former employees for internal deterioration signals

### Output Structure

**Short Thesis Drivers (ranked by conviction)**
| # | Driver | Evidence | Timing | Magnitude | Invalidation Signal | Source |
|---|--------|----------|--------|-----------|--------------------| -------|

**Bull Case Rebuttal:** For each common bull argument, the transcript evidence that challenges it.

**Borrow / Crowding Risk:** Any evidence suggesting the short is already consensus.

**Key Monitoring Points:** What to watch for thesis confirmation or invalidation.

---

## 6. Event Arbitrage (M&A / Spin-off / IPO)

**When to use:** Assessing the fundamental backdrop to a corporate event for event-driven positioning.
**Default horizon:** Event-specific (typically 1–12 months)
**Complexity:** Medium-High (4–7 atomic questions, 10–16 MCP calls)

### Prompt Template

Using Third Bridge transcripts, assess the fundamental context around **[event: merger, acquisition, spin-off, IPO, carve-out, strategic review]** involving **[Company/Companies]**. Focus on evidence relevant to: deal rationale validity, synergy achievability, integration risk, standalone viability of separated entities, management capability to execute, regulatory or customer risk to deal completion, and likely valuation implications. Identify where transcript evidence suggests the market is mispricing the probability, timing, or terms of the event, and where the fundamental risk/reward diverges from the event-driven pricing.

### Retrieval Decomposition

1. Target/acquirer + "merger" / "acquisition" / "deal" / "synergy"
2. Target/acquirer + "integration" / "culture" / "overlap" / "retention"
3. Target/acquirer + "regulation" / "antitrust" / "approval" / "customer consent"
4. Standalone entity + fundamental assessment keywords if spin-off/carve-out
5. Sector precedents for comparable events

### Output Structure

**Event Assessment**
| Dimension | Market Assumption | Transcript Evidence | Gap | Source |
|-----------|------------------|--------------------|----|--------|

**Probability / Timing Assessment:** Does transcript evidence change the base-case probability or timeline?

**Synergy / Value Assessment:** Are the stated synergies or value creation claims supported by expert evidence?

**Key Risk:** The most underappreciated risk to the event thesis, with supporting evidence.
