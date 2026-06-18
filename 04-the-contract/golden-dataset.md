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

**Adversarial rows included:** 2
* Incomplete supplier financial information for margin estimation.
* Conflicting pricing benchmarks and missing cost assumptions during sourcing strategy evaluation.
  
**Coverage gaps identified by partner:**
* Multi-language supplier proposals and negotiations.
* Highly volatile commodity pricing environments.
* Conflicting ERP, CLM, and spend analytics records.
* Multi-party negotiations involving consortium suppliers.
* Cross-border sourcing scenarios with tax and currency implications.
* ESG, regulatory, and geopolitical constraints affecting supplier selection.
* Limited historical data for new suppliers or emerging categories.
  
## Confidence UX Design

**Approach:** show uncertainty / tiered confidence / human-in-loop trigger
Tiered confidence scoring with explicit uncertainty indicators and automatic Human-in-the-Loop (HITL) escalation for business-critical procurement decisions.

**High confidence (>90%):**

* Recommendation displayed as ready for execution.
* Supporting calculations, benchmarks, and evidence are visible.
* Users may launch sourcing events or negotiation workflows directly.
  
**Medium confidence (70-90%):**
* Recommendation includes highlighted assumptions and alternative scenarios.
* User is prompted to review pricing models, supplier rankings, or sourcing strategy before execution.
  
**Low confidence (<70%):**
* Recommendation is labeled "Requires Review."
* Missing data, conflicting evidence, and uncertainty sources are explicitly surfaced.
* Automatic escalation to procurement or finance approver before action is permitted.
  
**User control surface:**
* View confidence score and rationale.
* Inspect underlying calculations and pricing assumptions.
* Review benchmark data and retrieved source documents.
* Compare alternative sourcing or negotiation strategies.
* Override AI recommendations with justification.
* Request manual procurement or finance review.
* Submit feedback to improve future recommendations.
  
## Reliability Contract

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | ≥95% | Evaluation against Golden Dataset | <92% rolling average |
| Hallucination rate | <1% | Human audit and retrieval-grounded evaluation | >2% |
| Latency (p95) | <15 seconds | End-to-end production telemetry | >20 seconds |
| Drift velocity | <3% degradation month-over-month | Continuous benchmark regression testing | >5% decline |

## HITL Architecture
<!-- When does a human step in? What's the escalation path? -->
Human intervention triggers:
* Award recommendation exceeds configurable spend threshold.
* Estimated savings exceed predefined materiality limits.
* Pricing diligence confidence falls below 70%.
* Supplier margin assumptions cannot be validated.
* Conflicting ERP, CLM, or finance data sources.
* Regulatory or procurement policy compliance uncertainty.
* High-risk contract deviations or sourcing exceptions.
  
Escalation path:
1. AI generates recommendation and confidence score.
2. Automated validation checks calculations and policy compliance.
3. Low-confidence or high-risk scenarios route to Category Manager or Procurement Lead.
4. Finance reviews pricing diligence and supplier economics where required.
5. Executive approver validates strategic sourcing recommendation.
6. Final decision and human feedback are captured for evaluation and future model improvement.
  
## Red-Team Findings
*What failure mode did your partner find that you missed?*

Failure mode identified by partner:
The agent produced a persuasive negotiation recommendation based solely on supplier quoted pricing without validating whether the requested increase was supported by underlying labor costs, commodity indices, or supplier margin assumptions.
Business risk:
The organization could accept unjustified price increases or reject commercially viable proposals because the AI failed to perform independent pricing diligence and financial validation.
Mitigation:
* Require pricing recommendations to reference benchmark data or should-cost models.
* Block autonomous negotiation recommendations when financial evidence is incomplete.
* Validate supplier economics using deterministic calculation engines before invoking the LLM.
* Require Human-in-the-Loop review for all high-value pricing and sourcing decisions with low confidence or missing financial inputs.
