# Credit Workflows

## Table of Contents
1. Initial Issuer Underwriting
2. Liquidity / Refinancing Risk
3. Covenant / Structural Risk
4. Distressed / Restructuring
5. Relative Value / Spread Mispricing
6. Sponsor Support / Private Credit
7. Event-Driven Credit
8. Ongoing Monitoring / Early Warning
9. Recovery Analysis
10. Capital Structure Arbitrage

---

## 1. Initial Issuer Underwriting

**When to use:** First-time credit assessment of an issuer.
**Default horizon:** 12–24 months
**Complexity:** High (6–8 atomic questions, 12–18 MCP calls)

### Prompt Template

Build a **transcript-based credit underwrite** on **[Issuer]**. Use expert evidence to assess revenue durability, customer concentration, pricing power, margin resilience, working capital behaviour, maintenance capex intensity, cyclicality, refinancing risk, and management credibility over the next **12–24 months**. Prioritise observations that map directly to leverage sustainability, liquidity runway, covenant headroom, and downside protection. Highlight both consensus and dissenting expert views, then conclude with the most likely credit impairment path and the strongest mitigating factors.

### Retrieval Decomposition

1. **Revenue quality:** Company + "revenue" / "demand" / "customer" / "contract" / "retention"
2. **Margin resilience:** Company + "margin" / "cost" / "pricing" / "input costs"
3. **Working capital & capex:** Company + "capex" / "inventory" / "receivables" / "cash"
4. **Competitive position:** Company + "competition" / "market share" / "pricing power"
5. **Management & governance:** Company + "management" / "strategy" / "capital allocation"
6. **Customer/supplier perspective:** Search without company filter using industry keywords

### Output Structure

**Credit Scorecard**
| Factor | Assessment | Direction | Evidence Quality | Source |
|--------|-----------|-----------|-----------------|--------|
| Revenue durability | | | | |
| Customer concentration | | | | |
| Pricing power | | | | |
| Margin resilience | | | | |
| Working capital | | | | |
| Capex intensity | | | | |
| Cyclicality | | | | |
| Management credibility | | | | |

**Leverage Sustainability Assessment:** Based on transcript evidence, is the current capital structure sustainable under base and stress cases?

**Impairment Path:** The most likely sequence of events that leads to credit deterioration, with probability assessment.

**Mitigating Factors:** What would need to hold or improve to avoid impairment.

---

## 2. Liquidity / Refinancing Risk

**When to use:** Assessing near-term cash and refinancing pressure.
**Default horizon:** 6–24 months
**Complexity:** Medium (4–6 atomic questions, 8–14 MCP calls)

### Prompt Template

Assess **[Issuer]'s liquidity and refinancing risk** using only transcript evidence. Focus on cash generation, receivables quality, inventory build, supplier payment terms, cost flexibility, capex obligations, customer concentration, lender sentiment, and sponsor support. Extract any expert commentary relevant to near-term liquidity pressure or refinance feasibility over the next **6–24 months**. Rank the 3 most important early warning indicators and show which transcript evidence suggests stabilisation versus deterioration.

### Retrieval Decomposition

1. Company + "cash" / "liquidity" / "working capital" / "cash flow"
2. Company + "debt" / "refinancing" / "maturity" / "lenders" / "banks"
3. Suppliers + payment terms, customer payment behaviour
4. Company + "capex" / "investment" / "spending" / "cost cutting"

### Output Structure

**Liquidity Traffic Light**
| Indicator | Status (Green/Amber/Red) | Evidence | Source |
|-----------|-------------------------|----------|--------|

**Early Warning Ranking**
1. [Most important] — evidence and monitoring trigger
2. [Second] — evidence and monitoring trigger
3. [Third] — evidence and monitoring trigger

**Stabilisation vs. Deterioration:** Which way does the balance of transcript evidence point?

---

## 3. Covenant / Structural Risk

**When to use:** Assessing creditor protections and structural leakage.
**Default horizon:** Structural (ongoing)
**Complexity:** Medium (3–5 atomic questions, 6–12 MCP calls)

### Prompt Template

Review transcripts for evidence relevant to **creditor protections and structural leakage risk** at **[Issuer]**. Focus on asset portability, collateral quality, opco/holdco separation, unrestricted subsidiaries, dividend behaviour, sponsor aggressiveness, EBITDA add-backs, and management attitudes toward creditor interests. Only include points with clear expert support. Conclude with what a creditor should underwrite as the main structural risk and what specific follow-up expert calls would best clarify recoveries or covenant leakage potential.

### Retrieval Decomposition

1. Company + "covenant" / "lender" / "creditor" / "debt terms"
2. Company + "sponsor" / "private equity" / "dividend" / "recap"
3. Company + "EBITDA" / "add-backs" / "adjustments" / "pro forma"
4. Company + "asset" / "collateral" / "subsidiary" / "transfer"

### Output Structure

**Structural Risk Map**
| Risk Type | Evidence | Severity | Source |
|-----------|----------|----------|--------|

**Creditor Alignment Assessment:** Does management/sponsor behaviour suggest alignment or adversarial posture toward creditors?

**Key Structural Risk:** Single most important structural concern with supporting evidence.

**Recommended Follow-Up Calls:** Specific expert profiles that would best clarify recovery or leakage risk.

---

## 4. Distressed / Restructuring

**When to use:** Business in or approaching distress — assessing recovery and restructuring paths.
**Default horizon:** 6–18 months
**Complexity:** High (6–10 atomic questions, 15–20 MCP calls)

### Prompt Template

Build a **restructuring and recovery analysis** for **[Issuer]** using transcript evidence from operators, lenders, suppliers, customers, and sector specialists. Identify what parts of the business are mission-critical, where value could erode quickly in distress, and which assets, contracts, customer relationships, or operational capabilities support recovery value. Prioritise evidence on vendor dependence, labour intensity, regulatory constraints, sponsor incentives, and business continuity risk. Separate enterprise-value durability from near-term liquidity risk.

### Retrieval Decomposition

1. Company + "restructuring" / "distressed" / "turnaround" / "bankruptcy"
2. Company + "customer" / "contract" / "retention" — assess customer stickiness in distress
3. Company + "supplier" / "vendor" / "trade credit" — assess supply chain fragility
4. Company + "assets" / "real estate" / "IP" / "equipment" — recovery value
5. Company + "employee" / "talent" / "retention" / "morale" — operational continuity
6. Sector + "restructuring" / "precedent" — comparable situations

### Output Structure

**Business Segment Value Map**
| Segment | Mission-Critical? | Value Durability in Distress | Key Risk | Source |
|---------|-------------------|------------------------------|----------|--------|

**Recovery Drivers**
- Assets, contracts, or relationships supporting floor value
- Factors that could cause rapid value erosion

**Restructuring Path Assessment**
- Most likely restructuring scenario based on expert evidence
- Sponsor incentives and likely behaviour
- Business continuity risks through process

**Enterprise Value vs. Liquidity:** Are these the same problem or different problems?

---

## 5. Relative Value / Spread Mispricing

**When to use:** Comparing credits within a sector to find mispriced risk.
**Default horizon:** 6–12 months
**Complexity:** High (6–10 atomic questions, 15–20 MCP calls)

### Prompt Template

Compare **[Issuer List]** within **[sector]** and identify where transcript evidence suggests the market may be mispricing fundamental credit risk. Rank names by likely spread tightening or widening over the next **6–12 months**. Focus on durability of cash flow, pricing, customer behaviour, capex intensity, asset quality, competitive pressure, and sponsor behaviour. Highlight any transcript-derived risk or resilience factor that appears underappreciated by broader market narratives.

### Retrieval Decomposition

For each issuer in the list:
1. Company-specific fundamentals search
2. Cross-reference with sector-level searches for comparative context
3. Customer/supplier searches for independent validation

### Output Structure

**Relative Value Ranking**
| Rank | Issuer | Direction | Key Driver | Underappreciated Factor | Confidence | Source |
|------|--------|-----------|-----------|------------------------|------------|--------|

**Pair Trade Opportunities:** Where transcript evidence most strongly supports a relative positioning.

**Common Sector Risk:** What risk affects the whole group and might not be priced.

---

## 6. Sponsor Support / Private Credit

**When to use:** Assessing private equity sponsor behaviour toward a portfolio company.
**Default horizon:** 12–24 months (base + downside)
**Complexity:** Medium (4–6 atomic questions, 8–14 MCP calls)

### Prompt Template

Analyse **[Sponsor]'s likely behaviour** toward **[Issuer]** under base and downside scenarios using transcript evidence. Search for views on the sponsor's historical willingness to inject equity, support liquidity, accept amendments, prioritise add-ons over deleveraging, or optimise around lenders. Combine this with transcript evidence on the issuer's operational resilience and capital needs. Distinguish between cases where sponsor support is likely economic and cases where it may be optional or withheld.

### Retrieval Decomposition

1. Sponsor name + "portfolio" / "support" / "equity injection" / "amendment"
2. Company + "sponsor" / "private equity" / "owner" / "shareholder"
3. Sector + "sponsor behaviour" / "private equity" — for pattern matching
4. Company + operational fundamentals to assess capital needs

### Output Structure

**Sponsor Behaviour Assessment**
| Scenario | Likely Sponsor Action | Economic Rationale | Evidence | Source |
|----------|----------------------|-------------------|----------|--------|

**Support Probability Matrix**
| Action | Base Case | Downside Case | Evidence Quality |
|--------|-----------|---------------|-----------------|
| Equity injection | | | |
| Amendment consent | | | |
| Add-on vs. delever | | | |
| Asset stripping risk | | | |

---

## 7. Event-Driven Credit

**When to use:** Assessing credit impact of a specific event (M&A, regulation, input shock, etc.).
**Default horizon:** Event-specific
**Complexity:** Medium-High (4–8 atomic questions, 10–16 MCP calls)

### Prompt Template

Assess the credit impact of **[event: acquisition, asset sale, regulation, input-cost shock, legal issue, refinancing, covenant reset]** on **[Issuer]** using only transcript evidence. Focus on the effect on leverage, liquidity, capex, working capital, margins, collateral quality, and refinancing flexibility. Identify which impacts are temporary versus structural and which assumptions experts believe are most fragile. End with the likely implication for different parts of the capital structure.

### Retrieval Decomposition

1. Company + event-specific keywords
2. Company + fundamental impact keywords (leverage, liquidity, margin)
3. Sector + event type for precedent/pattern evidence
4. Customer/supplier perspective on event impact

### Output Structure

**Event Impact Assessment**
| Dimension | Impact | Temporary vs. Structural | Confidence | Source |
|-----------|--------|-------------------------|------------|--------|

**Capital Structure Implications**
| Tranche | Impact Direction | Key Assumption | Fragility |
|---------|-----------------|----------------|-----------|

**Most Fragile Assumption:** What experts believe is most uncertain about the event's impact.

---

## 8. Ongoing Monitoring / Early Warning

**When to use:** Building or updating a watchlist/monitoring framework for an existing position.
**Default horizon:** Rolling 3–12 months
**Complexity:** Medium (4–6 atomic questions, 8–14 MCP calls)

### Prompt Template

Create a **credit early-warning dashboard** for **[Issuer]** from transcript evidence. Focus on signals most likely to foreshadow EBITDA disappointment, cash burn, covenant pressure, refinancing difficulty, or restructuring risk. Prioritise commentary on demand weakness, discounting, order slippage, customer loss, inventory build, labour issues, supplier strain, project delays, regulatory friction, and sponsor posture. Distinguish lagging indicators from true leading indicators and identify what change in evidence would alter the credit view materially.

### Retrieval Decomposition

1. Company + "demand" / "orders" / "pipeline" / "bookings" (leading indicators)
2. Company + "pricing" / "discount" / "competition" / "loss" (competitive health)
3. Company + "employee" / "supplier" / "payment" / "terms" (operational stress)
4. Company + "sponsor" / "lender" / "covenant" / "amendment" (capital structure)

### Output Structure

**Early Warning Dashboard**
| Signal | Current Status | Leading or Lagging? | Trigger for Concern | Source |
|--------|---------------|--------------------|--------------------|--------|

**View-Changing Threshold:** What specific evidence shift would materially alter the credit assessment?

**Recommended Monitoring Frequency:** How often to re-run this workflow based on credit quality.

---

## 9. Recovery Analysis

**When to use:** Estimating recovery values for a specific part of the capital structure.
**Default horizon:** Through-cycle
**Complexity:** High (5–8 atomic questions, 12–18 MCP calls)

### Prompt Template

Build a **transcript-based recovery analysis** for **[Issuer]** focusing on **[specific tranche or the full capital structure]**. Use expert evidence to assess the durability and realisability of key asset values: real estate, IP, customer contracts, equipment, inventory, brand value, and going-concern earnings power. Identify which assets are likely to retain value through distress and which would suffer material haircuts. Assess the likely form of restructuring (in-court vs. out-of-court, liquidation vs. going concern) based on business characteristics and stakeholder incentives. Map recovery expectations to specific tranches of the capital structure.

### Retrieval Decomposition

1. Company + "assets" / "real estate" / "property" / "equipment" / "IP"
2. Company + "customer contracts" / "backlog" / "recurring" / "retention in distress"
3. Company + "brand" / "franchise" / "goodwill" / "going concern"
4. Sector + "restructuring" / "recovery" / "liquidation" — precedent values
5. Company + "workforce" / "operational" / "continuity" — going-concern viability

### Output Structure

**Asset Recovery Map**
| Asset Category | Estimated Recovery Range | Evidence Basis | Key Risk to Value | Source |
|---------------|------------------------|----------------|-------------------|--------|

**Capital Structure Waterfall**
| Tranche | Recovery Expectation | Key Driver | Sensitivity |
|---------|---------------------|-----------|-------------|

**Restructuring Form:** Most likely path and why, based on transcript evidence.

---

## 10. Capital Structure Arbitrage

**When to use:** Identifying mispricing between different parts of an issuer's capital structure.
**Default horizon:** 3–12 months
**Complexity:** Medium (3–5 atomic questions, 8–12 MCP calls)

### Prompt Template

Using Third Bridge transcripts, assess whether **[Issuer]'s** capital structure pricing accurately reflects the relative risk across tranches (secured vs. unsecured, opco vs. holdco, term loan vs. bond, equity vs. credit). Focus on evidence that would differentially affect recovery or subordination: asset quality, intercompany flows, restricted vs. unrestricted subsidiary dynamics, collateral coverage, and sponsor incentives. Identify where transcript evidence suggests one part of the stack is mispriced relative to another.

### Retrieval Decomposition

1. Company + "secured" / "collateral" / "asset" / "lien"
2. Company + "subsidiary" / "intercompany" / "holdco" / "opco"
3. Company + "sponsor" / "equity" / "subordination" / "recovery"

### Output Structure

**Cross-Stack Assessment**
| Tranche Pair | Relative Pricing View | Supporting Evidence | Risk to View | Source |
|-------------|----------------------|--------------------|--------------| -------|

**Recommended Position:** Where transcript evidence most strongly supports a relative value view within the stack.
