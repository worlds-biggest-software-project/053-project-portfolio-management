# Project Portfolio Management — Feature & Functionality Survey

> Candidate #53 · Researched: 2026-05-01

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| Planview | Commercial SaaS | Proprietary; $45+/user/month; $200K–$1M+/year enterprise | https://www.planview.com |
| Oracle Primavera P6 | Commercial | Proprietary; ~$2,570/year licence + $550 maintenance; cloud on request | https://www.oracle.com/industries/construction-engineering/primavera |
| Microsoft Project for the Web / Planner | Commercial SaaS | Proprietary; included in M365; Project Plan 3 $30/user/month; Plan 5 $55/user/month | https://www.microsoft.com/en-us/microsoft-365/project |
| Smartsheet | Commercial SaaS | Proprietary; Business $19/user/month; Enterprise custom | https://www.smartsheet.com |
| Wrike | Commercial SaaS | Proprietary; from $9.80/user/month; Business ~$24.80/user/month | https://www.wrike.com |
| Celoxis | Commercial SaaS | Proprietary; $10–$45/user/month | https://www.celoxis.com |
| Prism PPM | Commercial SaaS | Proprietary; Standard $20/user/month | https://www.prismppm.com |
| Resource Guru | Commercial SaaS | Proprietary; from $6.65/user/month | https://resourceguruapp.com |
| OpenProject | Open Source | GPL v3 (Community); Cloud from €7.25/user/month | https://www.openproject.org |
| ProjectLibre | Open Source | Common Public Attribution Licence (CPAL); desktop free | https://www.projectlibre.com |

## Feature Analysis by Solution

### Planview

**Core features**
- Portfolio prioritisation and scoring: rank projects against strategic objectives with configurable criteria and weighted scoring
- Resource capacity management: identify bottlenecks, analyse team efficiency, and generate smart allocation recommendations across the full portfolio
- Financial management: budget tracking, benefit realisation, cost variance, and portfolio-level ROI analysis
- AI-powered portfolio risk analysis: surface schedule variances, cross-project dependencies, and actionable optimisation recommendations
- Conversational AI assistant: natural-language queries across portfolio data ("which projects are at risk of missing Q3 milestones?") with best-practice recommendations
- Sentiment analysis: analyse the tone of project comments and status updates to surface positive, neutral, or negative trends before they become risks
- Automated status reports: AI-generated project and portfolio status summaries reducing manual reporting overhead
- Scaled Agile (SAFe) portfolio boards alongside traditional stage-gate governance

**Differentiating features**
- Named Gartner Magic Quadrant Leader for Strategic Portfolio Management (2025) and Adaptive Project Management and Reporting — the only tool in both quadrants
- Conversational AI across the full portfolio dataset enables executive-level natural-language access to portfolio intelligence without dashboard navigation
- Sentiment analysis of unstructured project comments is unique among PPM tools — surfaces health signals from text that structured RAG status reports miss
- Planview built its AI assistant on Amazon Bedrock (AWS), providing a scalable, secure foundation for enterprise-grade AI PPM queries

**UX patterns**
- Executive dashboard with portfolio-level KPIs and AI-generated insight cards
- Planner UI for resource allocation across multiple concurrent projects
- Portfolio board for drag-and-drop project prioritisation and scenario comparison
- Team-level project views consistent with agile board patterns

**Integration points**
- Salesforce, SAP, Oracle, and Workday financial system connectors for budget synchronisation
- Jira and Azure DevOps integration for software delivery portfolio tracking
- Microsoft 365 (Teams, SharePoint) for status update and document management
- OData and REST APIs for custom BI and reporting integration

**Known gaps**
- Enterprise cost ($200K–$1M+/year) limits access to large organisations; mid-market is underserved at this price point
- Complex initial configuration; typical enterprise implementation 3–6 months
- AI features require clean, complete portfolio data — organisations with inconsistent project tracking practices get limited AI value initially

**Licence / IP notes**
- Fully proprietary SaaS; Planview has made multiple acquisitions (Changepoint 2017, Spigit 2019) to consolidate the strategic planning market

---

### Oracle Primavera P6

**Core features**
- Critical path method (CPM) scheduling with activity-level detail across programmes of hundreds of thousands of activities
- Resource loading and levelling across project hierarchies
- Earned Value Management (EVM) with cost and schedule performance indices (CPI, SPI) per ANSI/EIA-748
- Risk analysis: Monte Carlo simulation for schedule and cost uncertainty quantification
- Portfolio-level summary rollups from individual project schedules
- Baseline management: unlimited baseline storage with variance analysis

**Differentiating features**
- Industry standard for capital project portfolios in construction, energy, aerospace, and government — Primavera P6 experience is a professional certification in its own right
- Monte Carlo schedule risk analysis is native — no separate risk tool required
- Handles activity counts (100,000+ per programme) and resource pools (10,000+ resources) that cause other tools to fail

**UX patterns**
- Desktop-thick-client (P6 Professional) and web client (P6 EPPM) both available
- Steep learning curve; dedicated Primavera training certifications exist
- Optimised for professional schedulers and project controls engineers rather than general project managers

**Integration points**
- Oracle EBS, Fusion, and JD Edwards financial system integration
- P6 API for custom integrations
- Primavera Unifier for capital programme management and cost control
- Microsoft Project import/export for schedule exchange

**Known gaps**
- UI is dated even with the P6 EPPM web client; significant UX investment required for end-user adoption beyond professional schedulers
- Not suitable for IT or software delivery portfolios — designed for physical capital projects
- No AI features for schedule risk prediction, resource optimisation, or natural-language query
- High total cost of ownership when training, support, and infrastructure are included

**Licence / IP notes**
- Fully proprietary; Oracle licence and maintenance

---

### Microsoft Project for the Web / Planner

**Core features**
- Gantt, board, and timeline views for project task management
- Resource assignment and basic capacity tracking across Microsoft 365 users
- Portfolio summary view with project-level status rollups
- Microsoft Copilot integration: AI task generation from project goals, status update drafting, and natural-language project query
- Native Microsoft 365 integration: tasks sync with Planner, status updates in Teams, documents in SharePoint
- Microsoft retiring Project Online (September 2026) — large installed base forced to migrate

**Differentiating features**
- Copilot AI for project management: generate task lists from goals, draft status updates, and answer natural-language questions about project health — included in M365 subscriptions
- Lowest friction adoption in M365-centric organisations: no separate sign-on, data lives in the Microsoft 365 tenant, familiar interface patterns
- Project Online retirement is creating a significant migration market — Project for the Web is Microsoft's designated successor

**UX patterns**
- Modern web UI consistent with Microsoft 365 design language
- Accessible to non-PMO project owners; lower learning curve than Primavera or Planview
- Teams integration embeds project views directly in channels

**Integration points**
- Native Microsoft 365 ecosystem (Teams, SharePoint, Power BI, Power Automate)
- Dataverse integration for custom app development on project data
- Power BI for advanced portfolio reporting

**Known gaps**
- Significantly less powerful than Project Online for complex enterprise portfolio management — resource optimisation, EVM, and portfolio financial modelling are all weaker
- Project Online retirement is forcing organisations to either migrate to Project for the Web (reduced capability) or to third-party tools — creating a displacement opportunity
- Not suitable for capital project scheduling at Primavera scale

**Licence / IP notes**
- Fully proprietary SaaS; Microsoft licence; included in select M365 plans

---

### OpenProject

**Core features**
- Work package management: tasks, user stories, bugs, and milestones with configurable type and status workflows
- Gantt chart planning with dependencies, milestones, and baseline comparison across multiple projects in a unified view
- Agile boards: Scrum and Kanban with sprint planning and backlog management
- Portfolio management: project portfolio view with health status, progress, and budget summary across grouped projects
- Resource planning: assign people and roles across multiple projects with capacity management, workload balancing, and utilisation visibility in a global multi-project view
- Time tracking: log hours against work packages for billing and cost tracking
- Budgeting: project-level budget tracking with actual vs. planned cost comparison
- Self-hosted Community edition: free, GPL v3 licensed — full data sovereignty with no per-user cost on self-hosted deployment
- GDPR-compliant by design; EU-hosted and EU-founded (Berlin-based) — strong positioning for European public sector and regulated industries

**Differentiating features**
- Only credible open-source PPM tool with both project management depth (Gantt, agile, time tracking, budgeting) and multi-project portfolio visibility
- Self-hosted Community edition provides full feature access at infrastructure cost only — zero licence fee regardless of user count
- EU-native company and GDPR-by-design architecture gives OpenProject a trust advantage in European public sector procurement
- Roadmap includes AI features (announced): AI-powered project and portfolio management capabilities are in active development
- PMflex integration: OpenProject provides the technical platform for PMflex, the German Federal Government's standardised PM methodology and tooling

**UX patterns**
- Modern web UI with consistent design across project and portfolio views
- Role-based views: portfolio level for PMO directors; project level for PMs; team level for developers
- Accessible to non-specialist users compared to Primavera or Planview

**Integration points**
- REST API with full documentation for all work package, project, and user data
- GitHub and GitLab integration for development team work package linking
- Nextcloud integration for document management
- Single sign-on via SAML 2.0 (Enterprise and Cloud editions)
- Jira migration tools for teams transitioning from Atlassian

**Known gaps**
- No AI features shipping as of 2026 — roadmap is in development but not yet released
- Advanced financial portfolio modelling (portfolio ROI analysis, benefit realisation forecasting) is less powerful than Planview or Primavera
- Resource optimisation is capacity visibility rather than algorithmic optimisation — bottleneck resolution is manual
- Enterprise-scale implementations (500+ users, 1000+ projects) require the paid Cloud or Enterprise licence for full support and SLA guarantees
- No Earned Value Management (EVM) module — not suitable for US federal and defense contractors

**Licence / IP notes**
- Community edition: GNU GPL v3 — open source; self-hosted deployments free; modifications must be released under GPL v3
- Cloud and Enterprise editions: commercial; additional enterprise features (SAML SSO, advanced security, priority support) are proprietary add-ons
- Core codebase on GitHub: github.com/opf/openproject

---

### Smartsheet

**Core features**
- Spreadsheet-familiar grid interface with project tracking, dependency management, and Gantt visualisation
- Portfolio dashboards with project-level status rollups and configurable KPI metrics
- Resource management: team capacity and utilisation tracking across projects
- Automated workflows: no-code rule-based automation for approvals, notifications, and status updates
- AI features: Smartsheet AI for formula generation, text summarisation, and automated status report drafting

**Differentiating features**
- Lowest adoption friction for organisations familiar with spreadsheets — the grid interface is instantly comprehensible without PPM training
- Best tool in the market for marketing and creative portfolio management; less suited to engineering or capital project portfolios
- Strong workflow automation platform for non-technical PPM administrators

**UX patterns**
- Grid, Gantt, card, and calendar views all available on the same sheet data
- Dashboard builder with configurable charts, metrics, and text widgets

**Integration points**
- Salesforce, Jira, Microsoft 365, Google Workspace connectors
- Smartsheet Bridge for no-code workflow automation with external systems
- REST API for custom integrations

**Known gaps**
- Less powerful than Planview or Primavera for complex resource optimisation and portfolio financial modelling
- AI features are utility-level (formula help, text summaries) rather than strategic portfolio intelligence
- Not suitable for capital project scheduling at the scale and precision Primavera provides

**Licence / IP notes**
- Fully proprietary SaaS

---

### Wrike

**Core features**
- Project and portfolio tracking with Gantt, board, table, and analytics views
- Resource management with workload balancing
- Intake forms and request management for portfolio demand management
- AI features: Wrike AI for task automation, content generation, and smart suggestions
- Cross-tagging: work items can belong to multiple projects and portfolios simultaneously

**Differentiating features**
- Cross-tagging is a unique data model differentiator — work items visible in multiple project contexts simultaneously, reflecting matrix organisation reality
- Strong for marketing, creative, and professional services portfolio management

**UX patterns**
- Flexible view system (Gantt, board, table, analytics) configurable per user preference
- Inbox-driven work management highlights next actions

**Integration points**
- Salesforce, HubSpot, Jira, GitHub, Slack, Microsoft 365, Google Workspace
- REST API for custom integrations
- 400+ native connectors

**Known gaps**
- Less capable for engineering or capital project portfolios requiring EVM or constraint-based scheduling
- AI features are task-level assistance rather than portfolio-level strategic intelligence
- Resource optimisation requires manual decision-making after bottleneck identification

**Licence / IP notes**
- Fully proprietary SaaS

---

### Celoxis

**Core features**
- Project tracking, resource management, portfolio analysis, and financial management in a single mid-market platform
- Portfolio dashboard with budget, timeline, and resource utilisation summary
- Custom reporting and dashboard builder
- Risk management: risk register with probability/impact assessment

**Differentiating features**
- Best value-for-money mid-market PPM: $10–$45/user/month includes financial management and portfolio analysis that enterprise tools charge significantly more for
- Risk register integration within the PPM tool rather than as a separate application

**UX patterns**
- Functional dashboard-driven interface; not as polished as enterprise tools but adequate for mid-market PMOs
- Configurable report builder for custom portfolio metrics

**Integration points**
- Salesforce CRM sync
- REST API for custom integrations
- Jira and Microsoft Project data import

**Known gaps**
- No AI features
- Less powerful resource optimisation than Planview
- Smaller ecosystem and partner network than enterprise competitors

**Licence / IP notes**
- Fully proprietary SaaS

---

### Resource Guru

**Core features**
- Resource scheduling: visual timeline for assigning people to projects with drag-and-drop ease
- Capacity management: utilisation rates and availability overview across the team
- Leave management integrated with project scheduling
- Clash detection: identifies double-bookings and over-allocation automatically
- Waiting list: queue work requests when resources are fully booked

**Differentiating features**
- Purpose-built for resource scheduling rather than full PPM — the simplest and most intuitive resource management tool in the market
- Leave management integrated with scheduling is a practical differentiator: actual availability is always correct

**UX patterns**
- Visual timeline interface optimised for resource managers scheduling work across teams

**Integration points**
- Harvest time tracking integration
- REST API for integration with project management tools

**Known gaps**
- Not a PPM tool — no portfolio prioritisation, financial management, or project health tracking
- Intended as a companion tool to project management platforms, not a standalone PPM solution
- No AI features

**Licence / IP notes**
- Fully proprietary SaaS

---

## Cross-Cutting Feature Themes

### Table-Stakes Features
- Project portfolio dashboard with health status, budget, timeline, and resource utilisation summary across all active projects
- Gantt chart scheduling with task dependencies, milestones, and baseline comparison
- Resource capacity management: assign people across projects and identify over-allocation
- Portfolio prioritisation: rank projects against strategic criteria with configurable scoring
- Budget tracking with actual vs. planned cost comparison at project and portfolio level
- Risk register with probability and impact assessment
- Status reporting with configurable templates for stakeholder communication
- Integration with financial systems (ERP) and development tools (Jira, Azure DevOps)

### Differentiating Features
- Conversational AI across portfolio data for natural-language executive queries (Planview)
- Sentiment analysis of project comments and status updates for early health signal detection (Planview)
- Monte Carlo schedule risk simulation for capital project uncertainty quantification (Primavera P6)
- AI-generated status reports and proactive risk identification (Planview, Microsoft Project Copilot)
- SAFe portfolio boards alongside traditional stage-gate governance in a single tool (Planview)
- Self-hosted GPL v3 open-source deployment with full feature access at zero licence cost (OpenProject)
- GDPR-by-design architecture with EU-native hosting (OpenProject)
- Microsoft 365 native embedding with Copilot AI for task generation and natural-language query (Microsoft Project)

### Underserved Areas / Opportunities
- Automated resource conflict resolution: all tools surface over-allocation as a visual indicator but leave resolution to the PM — an AI agent that proposes concrete rebalancing plans with impact simulation would transform resource management from reactive to proactive
- AI-driven project health inference from unstructured signals: current tools rely on manually updated RAG statuses; AI inferring health from commit frequency, meeting attendance, action item closure rates, and status update sentiment would provide more accurate, earlier warnings
- Dynamic portfolio prioritisation aligned to changing strategy: most tools score projects against criteria set at planning time; continuous re-scoring as market conditions and business outcomes change is absent from every tool surveyed
- Natural-language portfolio what-if queries: "what happens to our 2026 delivery forecast if we redirect two senior engineers from Project A to Project B?" — no tool answers this in real time without manual scenario modelling
- Microsoft Project Online retirement opportunity: September 2026 retirement forces a large enterprise installed base to migrate — creating the largest single portfolio management market displacement event in a decade; an open-source or affordable alternative with credible feature parity is well-positioned

### AI-Augmentation Candidates
- Automated resource rebalancing agent: continuously monitor portfolio resource assignments, detect emerging conflicts weeks in advance, propose concrete rebalancing plans (swap assignments, defer low-priority projects, hire contractors), and simulate the impact of each option
- Project health inference engine: infer project health from commit frequency, meeting attendance, action item closure rates, budget burn velocity, and status update sentiment — providing earlier, more accurate risk signals than manually updated RAG statuses
- Natural-language portfolio intelligence: answer executive queries in plain language with portfolio data, identifying at-risk projects, milestone gaps, and resource bottlenecks without dashboard navigation
- Dynamic portfolio re-prioritisation: continuously re-score and re-rank the portfolio as strategic objectives, market conditions, and delivery outcomes change — surfacing reallocation recommendations before the next formal planning cycle

## Legal & IP Summary

Two open-source PPM tools exist: OpenProject (GPL v3 — copyleft; self-hosted Community free; enterprise/cloud features are commercial proprietary add-ons; source on GitHub) and ProjectLibre (CPAL licence — a form of copyleft with attribution requirements; desktop only; no portfolio management capability). All other surveyed tools are fully proprietary SaaS or licensed software. PMI PMBOK, PRINCE2, ISO 21500, and ISO 21504 are freely adoptable standards; PMBOK is published by PMI and PRINCE2 is published by AXELOS (Peoplecert-owned as of 2024) — neither licence restricts implementation of the methodology in software. ANSI/EIA-748 EVM is an open US government standard. OData and REST API standards are open with no IP restrictions. iCalendar (RFC 5545) is an IETF open standard. Project and portfolio data processed by PPM tools contains PII for employees and contractors (time records, performance data) which is subject to GDPR and equivalent regulations. Microsoft Project Online retirement (September 2026) is the most significant near-term IP/commercial event in this space — organisations with Project Online licences face forced migration. Planview's acquisition strategy (Changepoint, Spigit) has consolidated significant PPM IP into a single commercial entity.

## Recommended Feature Scope

**Must-have (MVP)**:
- Portfolio dashboard with project health status, budget summary, timeline milestones, and resource utilisation rollup
- Gantt chart scheduling with multi-project view, task dependencies, milestones, and baseline comparison
- Resource capacity management: assign people across projects, surface over-allocation, and visualise team utilisation
- Portfolio prioritisation with configurable scoring criteria and scenario comparison
- AI-inferred project health from structured signals (budget burn, milestone completion, action item closure) with plain-language health summary
- Status report generation from live project data (auto-populated templates)

**Should-have (v1.1)**:
- Natural-language portfolio query interface for executive use ("which projects are at risk of missing Q3 milestones and why?")
- Automated resource conflict detection with concrete rebalancing proposal and impact simulation
- Risk register with probability/impact assessment and portfolio-level risk rollup
- Financial portfolio management: budget tracking, benefit realisation forecast, and portfolio ROI analysis
- Integration with Jira and Azure DevOps for software delivery portfolio tracking

**Nice-to-have (backlog)**:
- AI-driven dynamic portfolio re-prioritisation: continuously re-score projects as strategic conditions change
- Sentiment analysis of project status updates and comments for early health signal detection
- Earned Value Management (EVM) module for US federal and defense contractor compliance
- SAFe portfolio board alongside traditional stage-gate governance
- What-if scenario modelling: simulate the delivery impact of redirecting resources between projects and across the portfolio
