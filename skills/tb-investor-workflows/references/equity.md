# Equity Workflows

## Table of Contents
1. Sector Idea Generation (Long/Short)
2. Rapid Thesis Build (Bull vs Bear)
3. Variant Perception Analysis
4. Earnings Preview / Post-Earnings Debrief
5. Competitive Dynamics Deep Dive
6. Management Quality Signal Check

---

## 1. Sector Idea Generation

**When to use:** User wants long/short ideas across a sector or universe.
**Default horizon:** 6–18 months
**Complexity:** High (6–10 atomic questions, 12–20 MCP calls)

### Prompt Template

Scan Third Bridge transcripts across **[sector/universe]** to identify the **3 strongest long ideas and 3 strongest short ideas**. Prioritise evidence from customers, suppliers, competitors, and former executives that points to accelerating or deteriorating fundamentals over the next **6–18 months**. Focus on demand trajectory, pricing power, competitive positioning, market-share change, product differentiation, execution quality, and margin implications. Quantify all relevant signals where possible and distinguish consensus views from variant views. For each name, provide the likely catalyst, the key KPI to monitor, the strongest disconfirming evidence, and why the transcript evidence suggests the market may be under- or overestimating the setup.

### Retrieval Decomposition

Break the sector into 3–5 sub-themes or company clusters. For each cluster:
1. Search by sector keywords + "growth" / "demand" / "pricing" / "market share"
2. Search by specific company names surfaced in initial results
3. Search for supplier/customer perspectives on the strongest candidates

### Output Structure

| Company | Direction | Key Driver | Catalyst | KPI to Monitor | Disconfirming Evidence | Expert Source |
|---------|-----------|-----------|----------|----------------|----------------------|---------------|

Follow with a narrative section for each name covering:
- **The setup:** What transcript evidence reveals about the fundamental trajectory
- **Consensus vs. variant:** Where the transcript view diverges from market pricing
- **Risk to thesis:** The strongest counterargument from expert evidence
- **Timeframe:** When the catalyst should materialise and what would delay it

---

## 2. Rapid Thesis Build (Bull vs Bear)

**When to use:** User wants a structured debate on a specific company.
**Default horizon:** 12 months
**Complexity:** Medium (4–6 atomic questions, 8–15 MCP calls)

### Prompt Template

Build an institutional-quality **bull vs bear transcript debate** on **[Company]** versus **[peer set]**. Use only transcript evidence to identify the 3–5 most important drivers of upside and downside over the next **12 months**, with emphasis on pricing, volume, retention, unit economics, competitive response, and management execution. Highlight where experts are aligned and where they diverge materially. Explicitly identify any evidence that contradicts company messaging or prevailing investor expectations. End with the single most important variable that would decide the thesis.

### Retrieval Decomposition

1. **Company-specific:** Search target company for revenue drivers, pricing, customer sentiment
2. **Competitive:** Search peer names for relative positioning, win/loss dynamics
3. **Customer/supplier lens:** Search for external validation of the company's claims
4. **Management/execution:** Search for former employee or partner views on leadership

### Output Structure

**Bull Case (ranked by conviction)**
| # | Driver | Evidence | Expert Source | Confidence |
|---|--------|----------|---------------|------------|

**Bear Case (ranked by conviction)**
| # | Driver | Evidence | Expert Source | Confidence |
|---|--------|----------|---------------|------------|

**Expert Alignment Matrix**
| Topic | Consensus View | Dissenting View | Implication |
|-------|---------------|----------------|-------------|

**Verdict:** The single most important swing variable and what evidence would resolve it.

---

## 3. Variant Perception Analysis

**When to use:** User wants to identify where transcript evidence diverges from consensus.
**Default horizon:** 3–12 months
**Complexity:** Medium (3–5 atomic questions, 6–12 MCP calls)

### Prompt Template

Review Third Bridge transcripts on **[Company]** and identify the most important **variant perceptions** versus management guidance, sell-side framing, or widely held investor assumptions. Prioritise experts with direct operational exposure and surface only findings with clear valuation relevance over the next **3–12 months**. For each variant, quantify the potential earnings or valuation impact where evidence permits, identify what would confirm or refute the variant, and assess how widely held the alternative view appears to be among experts.

### Retrieval Decomposition

1. Search target company broadly to establish the evidence base
2. Search for specific KPIs or business lines where management has made explicit claims
3. Search competitors and customers for external validation or contradiction

### Output Structure

| Variant # | Consensus/Mgmt View | Transcript Evidence Says | Valuation Relevance | Confirmation Signal | Expert Source |
|-----------|---------------------|-------------------------|--------------------|--------------------|---------------|

For each variant, provide a 2–3 paragraph narrative explaining why this matters and how differentiated the view appears to be.

---

## 4. Earnings Preview / Post-Earnings Debrief

**When to use:** User wants to pressure-test expectations ahead of or immediately after earnings.
**Default horizon:** Current quarter + next quarter
**Complexity:** Medium (4–6 atomic questions, 8–12 MCP calls)

### Prompt Template

**Pre-earnings version:**
Using Third Bridge transcripts, build a **channel-check-style earnings preview** for **[Company]** ahead of their upcoming quarter. Focus on demand signals, order patterns, pricing realisation, customer behaviour, inventory dynamics, competitive wins/losses, and any operational disruptions cited by customers, suppliers, distributors, or former employees in the last **6 months**. Identify where transcript evidence suggests upside or downside risk to consensus expectations on revenue, margins, and guidance. Flag any leading indicators that experts believe the market is underweighting.

**Post-earnings version:**
**[Company]** just reported earnings. Using Third Bridge transcripts, assess whether the results and guidance **confirm or challenge** what experts have been saying about demand trajectory, pricing power, competitive position, and margin sustainability. Identify where the earnings data validates expert concerns or optimism, and where new questions emerge that transcript evidence can help frame. Focus on the 2–3 most important implications for the next 6 months.

### Retrieval Decomposition

1. Search company + "demand" / "orders" / "pricing" / "volume" (recent 6 months)
2. Search company + "margin" / "cost" / "profitability"
3. Search customers/distributors for independent demand signals
4. Search competitors for relative performance context

### Output Structure

**Expectations vs. Expert Evidence**
| Metric | Consensus Expectation | Transcript Signal | Direction | Confidence | Source |
|--------|----------------------|-------------------|-----------|------------|--------|

**Key Risks to Watch**
- Upside risks with supporting evidence
- Downside risks with supporting evidence

**Most Important Signal:** What one data point from the transcript evidence should investors focus on.

---

## 5. Competitive Dynamics Deep Dive

**When to use:** User wants to understand market structure, share shifts, or competitive threats.
**Default horizon:** 12–24 months
**Complexity:** High (5–8 atomic questions, 10–18 MCP calls)

### Prompt Template

Map the **competitive landscape** around **[Company]** using Third Bridge transcripts. Identify who is gaining and losing share, what is driving the shifts, and how durable the current competitive positions appear over the next **12–24 months**. Focus on pricing behaviour, product differentiation, go-to-market effectiveness, customer switching dynamics, technology advantages, scale economics, and barriers to entry. Assess whether the competitive structure is stable, consolidating, or fragmenting and what that means for pricing power and margins across the sector. Identify the most underappreciated competitive threat and the most overestimated competitive advantage.

### Retrieval Decomposition

1. Search target company for competitive positioning references
2. Search each major competitor by name
3. Search customers for switching behaviour and vendor selection criteria
4. Search sector-level for structural trends (consolidation, new entrants, regulation)

### Output Structure

**Competitive Position Map**
| Player | Share Trend | Strengths | Vulnerabilities | Expert View | Source |
|--------|------------|-----------|----------------|-------------|--------|

**Key Dynamics:**
- Share migration drivers and durability
- Pricing environment and trajectory
- Most underappreciated threat
- Most overestimated advantage

---

## 6. Management Quality Signal Check

**When to use:** User wants to assess leadership credibility and execution capability from external evidence.
**Default horizon:** N/A (structural assessment)
**Complexity:** Low-Medium (2–4 atomic questions, 4–10 MCP calls)

### Prompt Template

Using Third Bridge transcripts, assess **[Company]'s management team** quality and credibility through the lens of former employees, customers, competitors, suppliers, and industry specialists. Focus on strategy clarity, capital allocation discipline, pricing decisions, talent retention, operational execution, acquisition track record, communication credibility, and cultural signals. Distinguish between expert observations that reflect structural management strengths/weaknesses and those that may be situational. Identify the single most important management-related risk or strength for the investment case.

### Retrieval Decomposition

1. Search company + "management" / "CEO" / "leadership" / "strategy"
2. Search company + "execution" / "culture" / "talent" / "turnover"
3. Search former employees specifically (these often yield the richest management insights)

### Output Structure

| Dimension | Expert Assessment | Evidence Quality | Source |
|-----------|------------------|-----------------|--------|

**Summary assessment:** Is management a net positive or net negative for the investment case, and what would change that view?
