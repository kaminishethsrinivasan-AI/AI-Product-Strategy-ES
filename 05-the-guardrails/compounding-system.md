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
Enterprise context shared across domains
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

## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |

**Total tools found:**
**Tools after triage:**
**Estimated hidden spend:**
