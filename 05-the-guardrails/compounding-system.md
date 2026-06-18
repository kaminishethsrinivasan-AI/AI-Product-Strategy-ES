# Compounding System Design

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| Negotiation Learning Loop | Negotiation strategies, user edits, supplier counteroffers, final negotiated outcomes | Improved negotiation playbooks, pricing recommendations, concession strategies, and target price predictions | Y | active |
| Pricing & Finance Diligence Loop | Supplier quotes, should-cost models, market benchmarks, finance reviews, realized savings | Better pricing benchmarks, supplier margin estimates, TCO models, and savings opportunity detection | Y | active |
| Supplier Performance Loop | Award decisions, supplier scorecards, delivery performance, SLA adherence, risk events | Improved supplier rankings, risk predictions, sourcing recommendations, and award decisions | Y | active |
| Policy & Governance Loop	| Procurement, Legal, Privacy, Risk, and Compliance reviews |	Stronger policy adherence, reduced hallucinations, improved governance, and safer autonomous execution	| Y	| Active |
| Cross-Category Intelligence Loop	| Spend data, sourcing events, contracts, negotiations across categories	| Better category strategies, sourcing wave planning, and enterprise-wide procurement intelligence	| Y	| Active |
| User Feedback Loop	| Explicit ratings, overrides, corrections, manual approvals	| Better prompts, recommendations, confidence calibration, and evaluation datasets	| Y	| Missing (planned roadmap item) |

**Broken loop identified by partner:**

The system captures sourcing recommendations but does not consistently capture why procurement professionals overrode AI recommendations, causing valuable learning signals to be lost.

**Fix plan:**
* Capture every manual override with structured reason codes.
* Log negotiation edits and supplier award changes.
* Feed approved changes into offline evaluation datasets.
* Enterprise context shared across domains.

## Context Connectivity
<!-- How does knowledge flow across teams and domains? Where does it silo? -->
Enterprise context shared across domain

The Procurement Intelligence Layer connects:
* ERP spend data
* Contract Lifecycle Management (CLM)
* Supplier Relationship Management (SRM)
* Spend Analytics
* Market intelligence providers
* Third-party risk platforms
* Financial benchmarks
* Procurement policies
* Historical sourcing events
* Historical negotiations
* Category strategies
Knowledge flows bidirectionally between sourcing, contracting, supplier management, finance, and risk functions.
Remaining silos
* Email negotiations outside integrated systems
* Offline spreadsheets
* Regional procurement playbooks
* Legal redlines maintained outside CLM
* Finance models stored locally
* Category-specific tribal knowledge
Future roadmap includes ingestion and indexing of these artifacts into the Procurement Knowledge Graph.

## Governance Policy
**Scope:**
The AI supports procurement planning, supplier intelligence, negotiation preparation, sourcing recommendations, pricing diligence, and autonomous workflow orchestration while remaining subject to enterprise governance policies.

**Autonomy boundaries:**
The AI may autonomously:
* Generate negotiation strategies
* Analyze supplier responses
* Recommend sourcing approaches
* Draft RFx documents
* Draft supplier communications
* Generate pricing diligence reports
* Produce should-cost analyses
* Prepare executive summaries
The AI may not autonomously:
* Award contracts
* Execute supplier selection
* Commit financial obligations
* Approve price increases
* Sign agreements
* Modify legal clauses
* Override procurement policy
* Bypass regulatory controls
  
**Escalation triggers:**
* Spend exceeds approval thresholds
* Confidence score below 70%
* Missing supplier financial data
* Pricing diligence uncertainty
* High-risk supplier recommendation
* Legal clause modifications
* Privacy or confidential data concerns
* Third-party risk score exceeds tolerance
* Conflicting enterprise data sources

**Audit cadence:**
* Daily automated policy validation
* Weekly Golden Dataset evaluation
* Monthly model drift analysis
* Quarterly Procurement, Finance, Privacy, Risk, and Legal review
* Annual independent governance audit
  
**Regulatory exposure (EU AI Act / other):**
* Enterprise procurement decision support may qualify as a high-impact business application requiring transparency and human oversight.
* All recommendations should be explainable, auditable, and traceable.
* Human approval remains mandatory for contract awards and legally binding commitments.
* Maintain compliance with applicable privacy regulations (e.g., GDPR, CCPA) and enterprise data governance policies.

## Agent Topology
<!-- If using agents: what can each agent do? What can't it do? Who approves what? -->
Procurement Orchestrator Agent
Can:
* Coordinate workflows
* Delegate tasks
* Aggregate results
* Generate executive recommendations
Cannot:
* Approve supplier awards
* Execute financial commitments

Negotiation Strategy Agent
Can:
* Build negotiation playbooks
* Simulate counteroffers
* Recommend concessions
* Estimate walk-away thresholds
Cannot:
* Commit negotiated terms
* Finalize commercial agreements

Pricing & Finance Agent
Can:
* Perform should-cost analysis
* Estimate supplier margins
* Validate pricing proposals
* Produce TCO models
* Estimate savings opportunities
Cannot:
* Approve budgets
* Commit financial decisions

Supplier Intelligence Agent
Can:
* Analyze supplier performance
* Aggregate market intelligence
* Assess supplier risk
* Recommend supplier rankings
Cannot:
* Blacklist suppliers
* Override enterprise risk policy

Compliance & Governance Agent
Can:
* Validate procurement policy
* Detect privacy concerns
* Flag legal issues
* Check regulatory requirements
* Verify approval workflows
Cannot:
* Provide legal opinions
* Waive policy requirements

Human Approvers
Category Leader
* Reviews sourcing strategy
* Reviews negotiation recommendations
Finance
* Approves pricing diligence
* Reviews supplier economics
* Validates savings calculations
Legal
* Reviews contractual language
* Approves legal deviations
Privacy
* Reviews confidential information handling
* Validates privacy compliance
Risk
* Reviews supplier risk
* Approves high-risk sourcing decisions
* 
## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| Individual procurement professionals using public LLMs for supplier analysis | Business Users | H | govern |
| Standalone spreadsheet-based pricing and should-cost calculators | Finance & Sourcing | M | govern |
| Unsanctioned contract summarization or RFx generation tools | Procurement Teams | H | kill |

**Total tools found:**
15
**Tools after triage:**
6 governed enterprise-approved tools consolidated into the Autonomous Sourcing & Negotiation platform

**Estimated hidden spend:**
Approximately $250K–$500K annually across duplicate AI subscriptions, shadow productivity tools, fragmented pricing models, manual spreadsheet maintenance, and inconsistent procurement workflows. Consolidation into a governed enterprise platform is expected to reduce hidden costs while improving compliance, auditability, and decision quality.
