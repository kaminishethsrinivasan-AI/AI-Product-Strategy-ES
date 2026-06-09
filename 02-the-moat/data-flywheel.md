# Data Flywheel Map

> Score each loop 1-5. Your weakest loop is where competitors attack first.
> The four loops below are the M2 starting point - adapt if your product has 2 or 6 loops instead of 4.

## Flywheel Loops

| Loop | What It Measures | Score 1 | Score 5 | Score |
|------|------------------|---------|---------|-------|
| **Correction** | Do users fix AI outputs? Is that signal captured and reused? | No capture | Automated retraining | 2/5 |
| **Preference** | Does the product learn individual / team preferences over time? | Stateless | Deep personalization | 2/5 |
| **Domain Context** | Does usage in one area improve quality in adjacent areas? | Siloed | Cross-domain transfer | 3/5 |
| **Network** | Does each new user / team make the product better for everyone? | Isolated | Strong network effects | 1/5 |

### Correction Loop - 2/5
**What you capture today:**
User prompts
AI-generated negotiation strategies
RFx analyses
Session history
Explicit thumbs up/down feedback (if available)

**How it compounds:**
Today, corrections are primarily used within the current session or for manual product improvement. They do not automatically improve future recommendations or retrain negotiation strategies.
Opportunity: Capture edits to negotiation plans, supplier rankings, and award recommendations as structured learning signals.

### Preference Loop - 2/5
**What you capture today:**
Recent conversations
Saved analyses
Active sourcing projects
Organization-level configuration
Connected enterprise systems

**How it compounds:**
The agent provides some contextual continuity but does not yet learn enduring buyer preferences, negotiation styles, or stakeholder priorities across engagements.
Opportunity: Build persistent procurement profiles for users, teams, and business units.

### Domain Context Loop - 3/5
**What you capture today:**
ERP spend data
Supplier master records
Contract metadata
Risk platform integrations
Spend analytics outputs

**How it compounds:**
The AI can combine multiple enterprise data sources to generate richer recommendations, but knowledge transfer between sourcing events remains limited because historical execution outcomes are not systematically incorporated.
Opportunity: Create a Procurement Knowledge Graph linking suppliers, categories, negotiations, contracts, and outcomes.

### Network Loop - 1/5
**What you capture today:**
Very little cross-customer learning
No anonymized benchmarking
No shared negotiation intelligence
No industry-wide pricing insights

**How it compounds:**
Each customer benefits only from its own enterprise data. New customers do not materially improve recommendations for others.
Opportunity: Introduce privacy-preserving aggregation of market benchmarks, supplier risk trends, and pricing indices.

**Total Flywheel Score: 8/20**
**Weakest Loop:**
Network (1/5)

**Fix for weakest loop:**
Launch an Anonymized Procurement Intelligence Exchange that aggregates:
Commodity price trends
Supplier performance benchmarks
Category savings benchmarks
Market inflation indicators
Standard contract clause prevalence
Negotiation trend analytics

---

## Encroachment Threat Assessment

### 1. Platform Encroachment
**Attacker:**
Enterprise platform providers ((e.g., SAP, Zip, AWS, Microsoft, Salesforce)

**Vector:**
Embed generative AI agents directly into existing ERP and procurement workflows.
Use native access to spend data, contracts, suppliers, and approvals to provide sourcing recommendations without requiring a separate platform.
Position AI capabilities as included features rather than standalone products.

**Time-to-threat:**
6–12 months

**% of value at risk:**
50%

### 2. Vertical Competitor
**Attacker:**
Procurement suites such as Coupa, Ivalua, Jaggaer, GEP, or Zycus

**Vector:**
Add autonomous sourcing and negotiation modules to their existing procurement offerings.
Leverage years of customer-specific sourcing history and supplier data.
Bundle AI into existing procurement subscriptions with minimal switching costs

**Time-to-threat:**
3–9 months

**% of value at risk:**
35%

### 3. Adjacent Expansion
**Attacker:**
Contract lifecycle management (CLM), spend analytics, and supplier risk vendors

**Vector:**
Expand from analytics or contract management into sourcing orchestration.
Use existing integrations and enterprise relationships to layer on AI-driven negotiation recommendations and RFx automation.
Position themselves as end-to-end procurement intelligence platforms.

**Time-to-threat:**
12–24 months

**% of value at risk:**
15%

---

## 90-Day Encroachment Plan

*Your partner played the Big Tech attacker. What was their plan to kill you?*

**Attacker:**
A major ERP platform provider with embedded AI capabilities.

**Attack vector (target the weakest loop):**
Exploit the lack of proprietary learning and network effects by delivering AI sourcing assistance directly within the ERP, eliminating the need for a standalone procurement intelligence layer.

**Weeks 1-4 - what they ship:**
AI-generated RFx templates
Supplier bid summaries
Negotiation strategy drafts
Spend opportunity analysis
Natural-language procurement assistant embedded in existing workflows

**Weeks 5-8 - how they poach users:**
Include AI features at no additional cost for current customers
Promote seamless deployment with zero integration effort
Emphasize unified governance, security, and compliance
Offer migration services and procurement modernization packages

**Weeks 9-12 - why users don't come back:**
Procurement teams become accustomed to AI embedded in their daily systems
Existing enterprise data remains centralized in the ERP
Leadership favors platform consolidation to reduce vendor complexity
The standalone product struggles to demonstrate differentiated value beyond basic AI assistance

**Your defense:**
- Build a moat based on proprietary procurement intelligence rather than workflow ownership by:
- Capturing user edits to negotiation strategies, supplier rankings, and sourcing recommendations as structured feedback.
- Learning from sourcing outcomes, realized savings, and supplier performance to improve future recommendations.
- Creating organization-specific procurement profiles that adapt to stakeholder preferences and governance policies.
- Building a Procurement Knowledge Graph that connects suppliers, categories, contracts, market intelligence, and historical negotiations.
- Delivering cross-platform orchestration across ERP, CLM, supplier management, risk, and spend analytics systems so the agent remains valuable regardless of the underlying enterprise stack.

The strategic objective is to evolve from an AI assistant layered on procurement systems into the enterprise system of intelligence that continuously improves from procurement outcomes, making replacement increasingly difficult over time.
