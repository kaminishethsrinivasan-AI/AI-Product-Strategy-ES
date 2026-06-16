# Cost Curve & Pricing Strategy

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | $20–$30 | Use only for negotiation strategy, should-cost analysis, and autonomous planning |
| Inference (cascading/triage) | $5–$10 | Route chat, retrieval, summarization, and extraction to low-cost models |
| Infrastructure | $8–$12 | Multi-tenant architecture with autoscaling |
| Data/storage | $3–$5 | Efficient vector indexing and document lifecycle management |
| Human-in-the-loop | $2–$5 | Trigger only for exceptions or premium services |
| **Total AI COGS** | $38–$62/user/month | Sustainable for unlimited usage pricing |

## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->
      
**Triage model:**

* Lightweight LLM or open-weight model for:
    * Rex parsing
    * Contract summarization
    * Supplier document extraction
    * Spend lookups
    * Search and retrieval
    * Basic procurement Q&A
    * 
**Frontier model:**

* Premium reasoning model for:
    * Negotiation strategy generation
    * Multi-agent sourcing execution
    * Should-cost analysis
    * Supplier award optimization
    * Executive recommendations
    * Scenario simulation

**Routing rule:**

1. Route simple retrieval, summarization, and classification requests to the triage model.
2. Use deterministic business logic where structured data is available.
3. Escalate only complex reasoning and planning tasks to the frontier model.
4. Cache reusable outputs (supplier summaries, category strategies, market benchmarks) to minimize repeat inference.
5. Reuse previously generated analyses whenever underlying data has not materially changed.
   
**Expected cascade ratio:**

* 85% → Triage model
* 10% → Medium-cost processing/business logic
* 5% → Frontier reasoning model

## Pricing Model

**Current pricing:**

* Traditional enterprise SaaS subscription
* Named-user licensing
* Unlimited procurement workflows
* No differentiated AI monetization
  
**Proposed AI pricing:**

* Enterprise platform subscription
* Premium named-user license for procurement professionals
* Unlimited AI usage included
* Unlimited negotiation strategy generation
* Unlimited supplier intelligence queries
* Unlimited sourcing analyses
* Unlimited award recommendations
* Unlimited autonomous sourcing assistance
  
**Model:** seat-based / usage-based / outcome-based / hybrid

Seat-based with unlimited AI usage bundled into premium enterprise licenses.

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x |  Moderate reduction in gross margin due to unlimited usage model. |  Increase routing to lower-cost models, expand caching, optimize prompts, and reserve frontier models only for complex reasoning tasks. |
| Heaviest segment doubles | Limited impact because power users represent a small portion of the user base but consume disproportionate compute. | Monitor cost per user internally, optimize scheduling and caching, and maintain backend controls without exposing usage limits to calendars. |
| Model provider raises prices 50% | Moderate margin compression if dependent on a single provider. | Shift traffic through a model abstraction layer, rebalance workloads across alternative providers, and increase use of open-weight models where quality permits.
 |

## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

**Before (traditional SaaS):**

* Revenue generated primarily through annual seat licenses.
* Software value tied to workflow automation and reporting.
* Predictable infrastructure costs with limited AI differentiation.
* Growth dependent on increasing seat count and module adoption.
  
**After (AI-enabled):**

* Premium-priced enterprise seats include unlimited AI usage.
* AI becomes the primary interface for sourcing, negotiations, supplier intelligence, and category planning.
* Revenue increases through higher-value enterprise licenses rather than metered token consumption.
* Backend costs are actively managed through intelligent model routing, retrieval-first architecture, caching, and orchestration.
* Customers purchase measurable procurement outcomes—including faster sourcing cycles, improved supplier decisions, and greater savings realization—rather than software access alone.
  
**Net margin shift:**

* Short term: Slight reduction in gross margins due to AI inference and infrastructure investments.
* Medium term: Margins stabilize as cascading, retrieval optimization, and caching reduce inference costs.
* Long term: Premium AI-enabled pricing combined with efficient backend architecture supports target gross margins of 70–80% while maintaining an unlimited AI usage customer experience.
  
