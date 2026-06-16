# Golden Dataset & Reliability Contract

## Golden Dataset Spec

| # | Input | Expected Output | Edge Case? | Judge Type |
|---|-------|----------------|-----------|-----------|
| 1 | "Prepare a negotiation strategy for a Tier A IT Services supplier requesting an 8% price increase." | Generates target price, walk-away threshold, concession strategy, leverage points, negotiation sequencing, and executive summary aligned with procurement policy. | N | LLM |
| 2 | "Compare bids from Suppliers A, B, and C and recommend an award decision." | Correctly ranks suppliers based on weighted commercial, technical, risk, and total cost criteria with transparent rationale and no calculation errors. | N | Both |
| 3 | "Perform pricing diligence on a contingent labor supplier charging $145/hour when market benchmarks indicate $125/hour." 
| "Identifies pricing variance, benchmarks against market data, estimates negotiation opportunity, recommends target pricing, and explains assumptions." | N | rule / LLM |
| 4 | "Estimate whether Supplier X can maintain a 20% gross margin based on proposed pricing, labor rates, overhead allocation, and SG&A assumptions." | "Produces a defensible should-cost model, estimates supplier margin range, highlights assumptions, and flags unrealistic economics or unsupported conclusions." | Y | rule / LLM |
| 5 | "Recommend whether to single-source or dual-source a $50M marketing services category considering supplier financial health, capacity constraints, business continuity risks, and total cost of ownership." | "Recommends sourcing strategy with quantified trade-offs across savings, resilience, concentration risk, and operational continuity while documenting confidence and rationale." | Y | LLM |

**Adversarial rows included:** __
**Coverage gaps identified by partner:**

## Confidence UX Design

**Approach:** show uncertainty / tiered confidence / human-in-loop trigger

**High confidence (>90%):**
**Medium confidence (70-90%):**
**Low confidence (<70%):**

**User control surface:**

## Reliability Contract

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | | | |
| Hallucination rate | | | |
| Latency (p95) | | | |
| Drift velocity | | | |

## HITL Architecture
<!-- When does a human step in? What's the escalation path? -->

## Red-Team Findings
*What failure mode did your partner find that you missed?*
