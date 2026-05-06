# Project Portfolio Management

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An AI-native, open-source platform for resource planning, project tracking, and budget management across portfolios — built to fill the gap left by retiring incumbents and overpriced enterprise suites.

Project Portfolio Management (PPM) gives PMOs, CIOs, and CFOs unified visibility across dozens to hundreds of concurrent projects: portfolio health, resource capacity, financial roll-ups, and strategic prioritisation in one place. This project targets the underserved middle of the market — organisations priced out of Planview and Oracle Primavera, but who need more than OpenProject offers today, especially as Microsoft retires Project Online in September 2026.

---

## Why Project Portfolio Management?

- **Enterprise PPM is prohibitively expensive.** Planview enterprise contracts run $200K–$1M+/year, and Oracle Primavera P6 carries ~$2,570/year per licence plus maintenance and steep training costs. Mid-market organisations are forced down to weaker tools.
- **The only credible open-source option lacks AI and advanced finance.** OpenProject (GPL v3) covers Gantt, agile, time tracking, and budgeting, but ships no AI features as of 2026 and is weaker than Planview/Primavera on portfolio ROI, benefit realisation, and resource optimisation.
- **Microsoft Project Online retires September 2026.** A large enterprise installed base must migrate to Project for the Web (a less capable successor) or to third-party tools — the largest PPM market displacement event in a decade.
- **Existing tools surface problems but do not solve them.** Every surveyed tool flags resource over-allocation as a red indicator and leaves resolution to the project manager. None infer project health from unstructured signals or answer executive what-if questions in real time.
- **Static prioritisation is the norm.** Projects are scored against criteria set at planning time; no surveyed tool continuously re-scores the portfolio as strategy, market conditions, or delivery outcomes change.

---

## Key Features

### Portfolio Visibility & Prioritisation

- Portfolio dashboard with project health status, budget summary, timeline milestones, and resource utilisation roll-up across all active projects
- Configurable scoring criteria for ranking projects against strategic objectives, with scenario comparison
- Multi-project Gantt view with task dependencies, milestones, and baseline comparison
- Status report generation auto-populated from live project data

### Resource & Capacity Management

- Assign people across multiple projects with capacity, workload, and utilisation visibility in a global view
- Automated detection of over-allocation and resource conflicts
- Concrete rebalancing proposals — swap assignments, defer low-priority projects, hire contractors — with simulated impact for each option
- Leave-aware scheduling so actual availability stays correct

### Financial Portfolio Management

- Project- and portfolio-level budget tracking with planned vs. actual cost comparison
- Benefit realisation forecasting and portfolio ROI analysis
- ERP integration (SAP, Oracle, Workday, Dynamics) over OData and REST APIs for budget synchronisation

### AI-Native Intelligence

- Project health inference from structured and unstructured signals: budget burn, milestone completion, action item closure, commit frequency, meeting attendance, and status update sentiment
- Natural-language portfolio queries for executive use: "which projects are at risk of missing Q3 milestones and why?", "what happens to our 2026 forecast if we redirect two senior engineers from Project A to Project B?"
- AI-generated status summaries reducing manual reporting overhead
- Dynamic portfolio re-prioritisation as strategic objectives, market conditions, and delivery outcomes change

### Risk & Governance

- Risk register with probability/impact assessment and portfolio-level risk roll-up
- Configurable stage-gate governance alongside SAFe portfolio boards
- Earned Value Management (EVM, ANSI/EIA-748) module for US federal and defense contractor compliance (backlog)
- Alignment with PMI PMBOK, PRINCE2, ISO 21500, and ISO 21504

---

## AI-Native Advantage

Incumbent PPM tools surface problems and rely on manually maintained RAG statuses and percent-complete estimates that are notoriously optimistic. Project Portfolio Management uses AI to infer project health from real signals (commits, meeting attendance, action item closure, budget burn, sentiment), to propose concrete resource rebalancing plans with simulated impact rather than just flagging conflicts, and to answer executive what-if questions in plain language without dashboard navigation. Continuous re-scoring keeps the portfolio aligned to strategy between formal planning cycles — a capability absent from every tool surveyed.

---

## Tech Stack & Deployment

- **Deployment modes:** self-hosted (full data sovereignty, GDPR-friendly) and managed cloud
- **Standards alignment:** PMI PMBOK 7, PRINCE2, ISO 21500, ISO 21504, ANSI/EIA-748 (EVM), iCalendar (RFC 5545)
- **Integration surface:** REST and OData APIs for ERP financial systems (SAP, Oracle, Workday, Dynamics); native connectors for Jira and Azure DevOps for software delivery portfolio tracking; SAML 2.0 SSO; calendar interoperability via RFC 5545
- **Migration paths:** designed to absorb the Project Online retirement cohort and offer Jira-style import for teams transitioning from incumbent tools

---

## Market Context

The global PPM software market is valued at $9.91 billion in 2026, projected to reach $16.87 billion by 2031 at a CAGR of 11.3%, with Asia-Pacific growing fastest at 15.3% (MarketsandMarkets, 2026). Pricing spans free open-source (OpenProject) through enterprise tiers at $45–$100/user/month and heavy-enterprise contracts of $200K–$1M+/year (Oracle Primavera, Planview). Primary buyers are PMO directors at enterprises managing 50–500 concurrent projects, CIOs balancing IT demand against capacity, capital project managers in construction and energy, CFOs tracking portfolio ROI and benefit realisation, and agile program managers running SAFe portfolios alongside financial governance.

---

## Project Status

> This project is in the **research and specification phase**.  
> Contributions, feedback, and domain expertise are welcome.

---

## Contributing

We welcome contributions from developers, domain experts, and potential users.
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Important:** All contributions must be your own original work or clearly attributed
open-source material with a compatible licence. Copyright infringement and licence
violations will not be tolerated and will result in immediate removal of the offending
contribution. If you are unsure whether a piece of code, text, or other material is
safe to contribute, open an issue and ask before submitting.

---

## Licence

Licence to be determined. See [discussion](#) for context.
