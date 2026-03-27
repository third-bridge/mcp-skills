# Private Equity Workflows

## Table of Contents
1. Sector Mapping / Origination
2. Deal Screen / IOI Decision
3. Commercial Diligence
4. Management Diligence
5. Underwriting / IC Memo Support
6. Value Creation / 100-Day Plan
7. Buy-and-Build / Add-on M&A
8. Exit Readiness
9. Vendor Due Diligence Pressure Test
10. Portfolio Monitoring

---

## 1. Sector Mapping / Origination

**When to use:** Exploring a subsector for investment themes and attractive pockets.
**Default horizon:** 3–5 years
**Complexity:** High (6–10 atomic questions, 12–20 MCP calls)

### Prompt Template

Use Third Bridge transcripts to build a **subsector map** for **[subsector]**. Identify the most attractive pockets for investment and the business models experts repeatedly describe as structurally advantaged or disadvantaged. Prioritise themes with clear implications for growth durability, pricing power, market fragmentation, consolidation potential, customer stickiness, and margin structure over the next **3–5 years**. Highlight where transcript evidence suggests a sector is benefiting from structural tailwinds versus cyclical noise.

### Retrieval Decomposition

1. Sector keywords + "growth" / "tailwind" / "structural" / "trend"
2. Sector + "fragmented" / "consolidation" / "roll-up" / "M&A"
3. Sector + "margin" / "pricing" / "economics" / "unit economics"
4. Sector + "customer" / "stickiness" / "switching" / "retention"
5. Sector + "competition" / "barrier" / "moat" / "differentiation"

### Output Structure

**Subsector Attractiveness Map**
| Pocket / Model | Attractiveness | Growth Durability | Pricing Power | Fragmentation | Key Insight | Source |
|---------------|---------------|-------------------|--------------|---------------|-------------|--------|

**Structural vs. Cyclical Assessment:** What experts say is durable vs. temporary.

**Top Origination Targets:** Business profiles that experts repeatedly describe as advantaged, with evidence.

**Sector Risks:** Common pitfalls or headwinds that would affect any investment in the space.

---

## 2. Deal Screen / IOI Decision

**When to use:** Quick go/no-go assessment on a specific target.
**Default horizon:** 12–24 months (investment period view)
**Complexity:** Medium (4–6 atomic questions, 8–15 MCP calls)

### Prompt Template

Build a **go / no-go transcript screen** on **[Target]**. Use relevant transcripts from customers, suppliers, competitors, former executives, and sector specialists to assess whether the asset merits advancing to **IOI / LOI**. Focus on demand durability, customer value proposition, renewal behaviour, market structure, pricing power, management quality, operational bottlenecks, and execution risk. Identify the 3 strongest reasons to proceed, the 3 strongest reasons to pause, and the critical diligence questions still unresolved.

### Retrieval Decomposition

1. Company + "customer" / "value proposition" / "retention" / "renewal"
2. Company + "pricing" / "margin" / "competitive" / "differentiation"
3. Company + "management" / "execution" / "operations" / "bottleneck"
4. Sector/competitors for market structure context

### Output Structure

**Go / No-Go Scorecard**

| Factor | Assessment | Evidence Quality | Source |
|--------|-----------|-----------------|--------|

**3 Reasons to Proceed**
1. [Evidence-backed reason]
2. [Evidence-backed reason]
3. [Evidence-backed reason]

**3 Reasons to Pause**
1. [Evidence-backed reason]
2. [Evidence-backed reason]
3. [Evidence-backed reason]

**Critical Unresolved Questions:** What must be answered in diligence before conviction can be formed.

**Recommendation:** Proceed / Pause / Pass — with the key condition for changing the view.

---

## 3. Commercial Diligence

**When to use:** Deep assessment of the commercial thesis — customer, product, market.
**Default horizon:** 3–5 year hold period
**Complexity:** High (6–8 atomic questions, 12–18 MCP calls)

### Prompt Template

Conduct a **commercial diligence synthesis** on **[Target]** using transcript evidence only. Evaluate customer mission-criticality, ROI to the customer, retention drivers, churn risk, willingness to absorb price increases, switching costs, implementation complexity, product differentiation, and competitor threat. Where possible, quantify renewal rates, spend growth, sales-cycle dynamics, win rates, or share-of-wallet trends cited by experts. Separate structural customer loyalty from temporary demand conditions and conclude with the most important underwriting implication.

### Retrieval Decomposition

1. Company + "customer" / "retention" / "churn" / "renewal" / "NPS"
2. Company + "pricing" / "price increase" / "willingness to pay" / "ROI"
3. Company + "switching" / "implementation" / "integration" / "lock-in"
4. Company + "product" / "differentiation" / "feature" / "roadmap"
5. Competitors + "win" / "loss" / "competitive" / "alternative"
6. Customers directly for independent demand validation

### Output Structure

**Commercial Thesis Scorecard**
| Dimension | Assessment | Underwriting Implication | Evidence Quality | Source |
|-----------|-----------|------------------------|-----------------|--------|
| Mission-criticality | | | | |
| Customer ROI | | | | |
| Retention / Churn | | | | |
| Price increase absorptability | | | | |
| Switching costs | | | | |
| Product differentiation | | | | |
| Competitive moat durability | | | | |

**Structural vs. Temporary Demand:** What transcript evidence distinguishes durable demand from cyclical or one-off.

**Key Underwriting Implication:** The single most important commercial finding for the investment case.

---

## 4. Management Diligence

**When to use:** Assessing the leadership team as part of deal evaluation.
**Default horizon:** N/A (structural)
**Complexity:** Medium (3–5 atomic questions, 6–12 MCP calls)

### Prompt Template

Build a **management quality assessment** on **[Target leadership team]** from transcript references by former employees, sector experts, customers, competitors, and former partners. Focus on decision-making quality, strategy clarity, execution cadence, pricing discipline, talent retention, sales leadership, integration capability, budgeting realism, and operational accountability. Prioritise repeated expert observations over anecdotal comments, but include clearly differentiated concerns if they come from highly relevant operators. Identify which management strengths or weaknesses would matter most post-close.

### Retrieval Decomposition

1. Company + "CEO" / "management" / "leadership" / "founder"
2. Company + "culture" / "talent" / "retention" / "turnover" / "morale"
3. Company + "execution" / "strategy" / "decision" / "accountability"
4. Company + "acquisition" / "integration" / "M&A track record" (if relevant)

### Output Structure

**Management Assessment Matrix**
| Dimension | Assessment | Evidence Weight | Post-Close Relevance | Source |
|-----------|-----------|----------------|---------------------|--------|
| Decision quality | | | | |
| Strategy clarity | | | | |
| Execution cadence | | | | |
| Pricing discipline | | | | |
| Talent retention | | | | |
| Sales leadership | | | | |
| Integration capability | | | | |
| Budgeting realism | | | | |

**Post-Close Implication:** What the management assessment means for hold-period execution — where to lean in, where to supplement.

---

## 5. Underwriting / IC Memo Support

**When to use:** Building or pressure-testing the investment case for IC.
**Default horizon:** Full hold period (3–5+ years)
**Complexity:** High (6–10 atomic questions, 15–20 MCP calls)

### Prompt Template

Create a **transcript-supported underwriting pack** for **[Target]**. Pressure-test the investment case using only expert evidence on growth durability, pricing, gross margins, go-to-market effectiveness, customer concentration, capex intensity, working capital, and competitive behaviour. Translate transcript findings into implications for the base, upside, and downside underwriting cases. Highlight which assumptions are strongly supported by repeated expert evidence and which rely on management optimism or remain insufficiently evidenced.

### Retrieval Decomposition

1. Growth: Company + "growth" / "demand" / "pipeline" / "new customer" / "expansion"
2. Pricing: Company + "pricing" / "price increase" / "contract" / "ASP"
3. Margins: Company + "margin" / "cost" / "efficiency" / "gross profit"
4. Competition: Company + "competitive" / "share" / "threat" / "disruption"
5. Customers: Company + "concentration" / "top customer" / "dependency"
6. Capex/WC: Company + "capex" / "working capital" / "cash conversion"

### Output Structure

**Underwriting Assumption Validation**
| Assumption | CIM/Mgmt Claim | Transcript Evidence | Supported? | Risk Level | Source |
|-----------|---------------|--------------------|-----------|-----------| -------|

**Case Mapping**
| Scenario | Key Assumptions | Transcript Support | Confidence |
|----------|----------------|-------------------|------------|
| Bull | | | |
| Base | | | |
| Bear | | | |

**IC Red Flags:** Assumptions that lack expert support or where evidence actively contradicts the thesis.

---

## 6. Value Creation / 100-Day Plan

**When to use:** Identifying post-close value creation levers.
**Default horizon:** 12–36 months (phased)
**Complexity:** High (5–8 atomic questions, 10–18 MCP calls)

### Prompt Template

Identify the highest-probability **value-creation levers** for **[Target]** using transcript evidence from operators, customers, suppliers, competitors, and former executives. Prioritise pricing opportunity, salesforce productivity, procurement, automation, product mix, channel optimisation, international expansion, cross-sell, or operational discipline where experts identify specific bottlenecks or upside. Rank initiatives by likely EBITDA impact, implementation complexity, required capabilities, and time to realise value. Flag the most common reasons similar initiatives fail in this sector.

### Retrieval Decomposition

1. Company + "pricing" / "price increase" / "underpriced" / "margin opportunity"
2. Company + "sales" / "go to market" / "salesforce" / "productivity"
3. Company + "cost" / "procurement" / "automation" / "efficiency"
4. Company + "product" / "cross-sell" / "upsell" / "expansion"
5. Sector + "value creation" / "operational improvement" / "best practice"

### Output Structure

**Value Creation Lever Ranking**
| Rank | Initiative | EBITDA Impact Est. | Complexity | Time to Value | Key Risk | Source |
|------|-----------|-------------------|-----------|---------------|----------|--------|

**Quick Wins (0–6 months)**
- Initiatives with supporting evidence and low complexity

**Medium-Term (6–18 months)**
- Initiatives requiring capability build or investment

**Structural (18+ months)**
- Transformational initiatives with higher risk/reward

**Common Failure Modes:** Why similar initiatives have failed in this sector, per expert evidence.

---

## 7. Buy-and-Build / Add-on M&A

**When to use:** Evaluating roll-up or add-on acquisition strategy.
**Default horizon:** 3–5 year hold period
**Complexity:** High (5–8 atomic questions, 12–18 MCP calls)

### Prompt Template

Use transcript evidence to identify the strongest **buy-and-build paths** for **[Platform]** in **[subsector]**. Assess which adjacencies, customer sets, capabilities, or geographies appear most complementary and defensible. Focus on cross-sell potential, shared customer relationships, procurement overlap, integration complexity, pricing implications, and cultural or operational risks. Highlight where transcript evidence suggests roll-ups typically succeed, and where they destroy value due to fragmentation, customer churn, poor integration, or low switching costs.

### Retrieval Decomposition

1. Platform company + "acquisition" / "M&A" / "bolt-on" / "add-on"
2. Subsector + "fragmented" / "consolidation" / "roll-up" / "independent"
3. Subsector + "integration" / "cross-sell" / "synergy" / "overlap"
4. Subsector + "customer" / "switching" / "retention post-acquisition"

### Output Structure

**Add-on Opportunity Map**
| Adjacency / Target Profile | Strategic Fit | Integration Risk | Cross-Sell Potential | Evidence | Source |
|---------------------------|--------------|-----------------|---------------------|----------|--------|

**Roll-Up Success Factors:** What transcript evidence says makes consolidation work in this sector.

**Roll-Up Failure Modes:** What typically goes wrong and why.

**Recommended Sequencing:** Which acquisitions to prioritise and why.

---

## 8. Exit Readiness

**When to use:** Assessing how a portfolio company would be received by buyers.
**Default horizon:** 12–24 months to exit
**Complexity:** Medium-High (5–7 atomic questions, 10–16 MCP calls)

### Prompt Template

Build an **exit-readiness assessment** for **[PortCo]** using transcript evidence relevant to how strategic buyers, sponsors, and lenders are likely to view the asset. Focus on growth quality, pricing durability, customer concentration, management depth, recurring revenue quality, margin resilience, competitive positioning, capex needs, and integration or carve-out complexity. Identify which transcript-backed strengths could support premium valuation and which unresolved issues would likely drive diligence discounting at exit.

### Retrieval Decomposition

1. Company + "growth" / "recurring" / "revenue quality" / "visibility"
2. Company + "customer" / "concentration" / "retention" / "NRR"
3. Company + "margin" / "profitability" / "efficiency" / "scalability"
4. Company + "competition" / "moat" / "positioning" / "threat"
5. Company + "management" / "team" / "depth" / "bench"

### Output Structure

**Exit Attractiveness Scorecard**
| Dimension | Buyer Appeal | Evidence | Risk of Diligence Discount | Source |
|-----------|------------|----------|--------------------------|--------|

**Premium Drivers:** What transcript evidence supports a premium multiple.

**Discount Risks:** What would likely come up in buyer diligence and compress value.

**Buyer Universe Implications:** Which buyer types (strategic vs. sponsor) the evidence suggests would value the asset most highly, and why.

---

## 9. Vendor Due Diligence Pressure Test

**When to use:** Reviewing or challenging a VDD report using independent transcript evidence.
**Default horizon:** N/A (snapshot assessment)
**Complexity:** Medium (4–6 atomic questions, 8–14 MCP calls)

### Prompt Template

Using Third Bridge transcripts, **pressure-test the key claims** in the vendor due diligence for **[Target]**. Focus on the VDD's assertions about market size, growth rate, competitive positioning, customer satisfaction, pricing power, and margin sustainability. For each major claim, assess whether transcript evidence from customers, competitors, suppliers, and former employees corroborates, contradicts, or adds nuance to the VDD narrative. Identify the 3 areas where transcript evidence most diverges from the VDD framing and the 3 areas where it provides strongest independent confirmation.

### Retrieval Decomposition

1. Company + core VDD claim keywords (market size, growth, positioning)
2. Competitors for independent market context
3. Customers for independent satisfaction/value prop validation
4. Former employees for internal reality check

### Output Structure

**VDD Claim Validation**
| VDD Claim | Transcript Evidence | Verdict (Confirmed/Challenged/Nuanced) | Source |
|-----------|--------------------|-----------------------------------------|--------|

**Top 3 Divergences from VDD**
**Top 3 Confirmations from Transcript Evidence**

---

## 10. Portfolio Monitoring

**When to use:** Periodic check-in on an existing portfolio company using fresh transcript evidence.
**Default horizon:** Rolling quarterly
**Complexity:** Medium (3–5 atomic questions, 6–12 MCP calls)

### Prompt Template

Run a **quarterly transcript monitoring update** on **[PortCo]**. Search for any new Third Bridge transcript evidence from the last **6 months** that is relevant to the investment thesis, value creation plan, or risk factors. Focus on changes in customer sentiment, competitive dynamics, pricing environment, demand trajectory, operational execution, management quality signals, and sector structural shifts. Flag any evidence that would change the hold/exit decision or reprioritise the value creation plan.

### Retrieval Decomposition

1. Company + broad keywords, filtered to last 6 months
2. Key competitors for relative positioning changes
3. Sector-level for structural shifts

### Output Structure

**Monitoring Dashboard**
| Thesis Element | Last Assessment | New Evidence | Direction of Change | Action Required? | Source |
|---------------|----------------|-------------|--------------------|-----------------| -------|

**Thesis Confirmation / Challenge:** Has the balance of evidence shifted?

**Value Creation Plan Implications:** Any evidence suggesting re-prioritisation?

**Recommended Actions:** Follow-up expert calls, diligence, or portfolio actions.
