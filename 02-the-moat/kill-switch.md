# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | | H | |
| **Abstraction** | | M | |
| **Routing** | | M | |
| **Eval** | | H | |

## Portability Score
<!-- Ready / Partial / Locked -->
Partial
The application architecture is portable, but production readiness depends on reducing reliance on a single LLM provider and expanding cross-model evaluation coverage.

## If [primary vendor] doubles pricing tomorrow:
<!-- What's your 48-hour response? -->

- Redirect inference traffic through the existing model abstraction layer.
- Shift low-risk workloads (summarization, document extraction, RFx analysis) to lower-cost or open-weight models.
- Reserve premium models for high-value negotiation planning and executive recommendations.
- Enable cost-based routing policies to optimize spend automatically.
- Re-run evaluation suites to confirm acceptable quality before scaling traffic.

Because procurement logic, integrations, and orchestration remain independent of the foundation model, customer workflows continue uninterrupted.

## If [primary vendor] ships a competing product:
<!-- What's defensible that they can't replicate? -->

- The defensible moat is not the language model—it is the enterprise-specific procurement intelligence accumulated over time:
- Organization-specific sourcing policies and governance rules
- Historical sourcing projects and negotiation context
- Connected ERP, CLM, supplier management, and spend analytics integrations
- Procurement Knowledge Graph linking suppliers, categories, contracts, and market intelligence
- Customer-specific negotiation playbooks and approval workflows
- Institutional expertise embedded in autonomous sourcing agents
- Outcome-based learning from sourcing decisions, realized savings, and supplier performance (as these signals are captured over time)
- Cross-system orchestration that executes actions across heterogeneous enterprise platforms rather than within a single vendor ecosystem
