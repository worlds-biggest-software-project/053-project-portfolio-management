# Standards & API Reference

> Project: Project Portfolio Management · Generated: 2026-05-06

## Industry Standards & Specifications

### ISO Standards

**ISO 21500:2021 — Project, Programme and Portfolio Management: Context and Concepts**
- URL: https://www.iso.org/standard/75704.html
- Second edition (March 2021); replaced the 2012 edition. Provides the organizational context and underlying concepts for undertaking project, programme and portfolio management, and describes relationships among the ISO 21500 family of standards (ISO 21502, ISO 21503, ISO 21504, ISO 21505). Applicable to any organization regardless of size, sector, or type. A PPM tool aligning to this standard should reflect its model of nested portfolio/programme/project relationships and governance structures.

**ISO 21504:2015 — Guidance on Portfolio Management**
- URL: https://www.iso.org/standard/61518.html
- The dedicated ISO standard for project and programme portfolio management. Defines a portfolio as a collection of portfolio components grouped together to facilitate management and meet strategic objectives. Covers prerequisites for portfolio management, managing portfolios, and portfolio governance. Targets executives, senior managers, and decision-makers responsible for portfolio selection and authorization — the exact user personas a PPM tool must serve. A 2022 British Standard edition (BS ISO 21504:2022) is also published.

**ISO 21502:2020 — Guidance on Project Management**
- URL: https://www.iso.org/standard/74947.html
- Provides harmonized guidance on project management, replacing the project-management content that was in ISO 21500:2012. Relevant to PPM tools that manage individual projects as portfolio components; defines core lifecycle concepts (initiating, planning, performing, closing) that a PPM tool should map to its project data model.

**ISO 21503:2022 — Guidance on Programme Management**
- URL: https://www.iso.org/standard/82868.html
- Provides guidance on programme management — the coordinated management of related projects and activities to deliver benefits. Relevant to PPM tools that support multi-project programme governance and benefit realisation tracking alongside project-level scheduling.

**ISO 21505:2017 — Governance of Projects, Programmes and Portfolios**
- URL: https://standards.globalspec.com/std/10157317/iso-21505
- Provides guidance on governance within the context of project, programme, and portfolio management. Covers how executive and senior management oversee PPM and enable strategic alignment. Shapes the governance framework and audit trail requirements of an enterprise PPM tool.

---

### W3C & IETF Standards

**RFC 5545 — Internet Calendaring and Scheduling Core Object Specification (iCalendar)**
- URL: https://datatracker.ietf.org/doc/html/rfc5545
- IETF standard (September 2009) defining the iCalendar data format for representing and exchanging calendaring and scheduling information: events, to-dos, journal entries, and free/busy data. Relevant to PPM resource scheduling: the `RESOURCES` property allows equipment and resource assignments to be expressed in a machine-readable, interoperable format. Tools that export resource calendars or integrate with Outlook, Google Calendar, and Apple Calendar implement RFC 5545.

**RFC 7643 & RFC 7644 — SCIM 2.0 (System for Cross-domain Identity Management)**
- URLs: https://datatracker.ietf.org/doc/html/rfc7643 and https://datatracker.ietf.org/doc/html/rfc7644
- IETF standard (September 2015) for automating the exchange of user identity information between identity domains. SCIM 2.0 enables automatic provisioning and deprovisioning of user accounts in a PPM tool from a central identity provider (Okta, Azure AD, Google Workspace). OpenProject implements SCIM for Enterprise/Cloud editions; any enterprise-grade PPM tool should support SCIM for user lifecycle management at scale.

**OData v4 (OASIS Standard)**
- URL: https://www.odata.org/
- Open Data Protocol, standardized by OASIS, is a REST-based protocol for querying and manipulating data over HTTP in JSON or XML. It is the de facto integration standard for Microsoft Dynamics 365 and SAP, and is used by Microsoft Project for the Web (via Dataverse OData APIs) and Planview Portfolios for ERP financial data synchronization. A PPM tool integrating with enterprise ERP systems (SAP, Dynamics, Workday) will encounter OData as the integration mechanism for budget and financial data exchange.

**JSON:API v1.1 Specification**
- URL: https://jsonapi.org/
- A specification for building APIs in JSON, finalized September 2022. Defines a standardized format for API requests and responses with top-level data, relationships, and links structures, and implements HATEOAS (Hypermedia As The Engine Of Application State) principles. OpenProject's API v3 is explicitly HATEOAS-based; this approach improves API discoverability and reduces client-side coupling, relevant for a PPM API that external BI and integration tools must consume reliably.

---

### Data Model & API Specifications

**OpenAPI Specification 3.1.0**
- URL: https://spec.openapis.org/oas/v3.1.0
- The industry-standard format for describing RESTful APIs in YAML or JSON, enabling automatic code generation, interactive documentation (Swagger UI, Redoc), and contract testing. OpenAPI 3.1 achieves full compatibility with JSON Schema Draft 2020-12. OpenProject documents its API v3 using OpenAPI 3.1; the spec is accessible at `/api/v3/spec.yml` on any OpenProject instance. Any new PPM tool should publish an OpenAPI 3.1 spec for its REST API.

**JSON Schema Draft 2020-12**
- URL: https://json-schema.org/specification
- The standard for describing and validating JSON document structure. Used natively within OpenAPI 3.1 for request/response schema definitions. Relevant for defining the PPM data model for projects, portfolios, resources, budgets, and work packages in a machine-validatable, tool-agnostic format.

**ANSI/EIA-748 — Earned Value Management Systems (EVMS) Standard**
- URL: https://www.sae.org/standards/eia748d-earned-value-management-systems
- Published by SAE International (formerly EIA), this is the US government standard for earned value management. Defines 32 guidelines that an EVMS must satisfy, covering planning, scheduling, budgeting, accounting, analysis, and reporting. Required for US federal and defense contracts. PPM tools targeting these markets (Oracle Primavera P6 is the incumbent) must implement cost performance index (CPI) and schedule performance index (SPI) calculations per ANSI/EIA-748. This standard is not relevant for general commercial PPM but is essential for government and capital project markets.

---

### Security & Authentication Standards

**OAuth 2.0 (RFC 6749) and OpenID Connect 1.0**
- URL: https://oauth.net/2/ and https://openid.net/connect/
- Industry-standard protocols for authorization and authentication respectively. OAuth 2.0 defines secure token-based API authorization; OpenID Connect extends OAuth 2.0 with user identity and SSO. All major PPM tools (Oracle Primavera P6 EPPM, Planview, Wrike, Smartsheet) use OAuth 2.0 for API authentication. Any new PPM tool should implement OAuth 2.0 (Authorization Code Grant with PKCE for browser-based clients) for its API and support OpenID Connect for enterprise SSO.

**SAML 2.0**
- URL: https://wiki.oasis-open.org/security/FrontPage
- OASIS standard (2005) for XML-based federated identity and SSO. Remains the dominant enterprise federation standard for applications built before 2015 and is required by many large enterprise procurement policies. OpenProject supports SAML 2.0 SSO in Enterprise and Cloud editions. Enterprise-grade PPM tools should support SAML 2.0 alongside OIDC to satisfy procurement requirements in regulated industries and government.

**OWASP Application Security Guidelines**
- URL: https://owasp.org/
- OWASP Top 10 and OWASP ASVS (Application Security Verification Standard) provide widely referenced security requirements for web applications. Relevant throughout PPM tool development, particularly for: secure handling of PII (employee time records, resource assignments); API authentication and authorization (preventing insecure direct object references across multi-tenant portfolio data); and audit logging for compliance.

**GDPR (EU General Data Protection Regulation)**
- URL: https://gdpr.eu/
- EU regulation governing personal data processing. PPM tools store PII for employees and contractors (names, time records, resource assignments, performance data). GDPR requires data protection by design and by default, lawful basis for data processing, data subject rights (access, erasure), and Data Processing Agreements with all sub-processors. OpenProject's EU-native architecture and GDPR-by-design positioning is a competitive differentiator in European markets; any PPM tool targeting EU customers must implement these requirements.

---

### MCP Server Specifications

**Model Context Protocol (MCP) — Agentic AI Foundation / Linux Foundation**
- URL: https://modelcontextprotocol.io/specification/2025-11-25
- Open standard (introduced by Anthropic, November 2024; donated to AAIF/Linux Foundation, December 2025) for standardizing how AI systems integrate with external tools, systems, and data sources. By May 2026 the ecosystem has over 10,000 active public MCP servers and 97 million monthly SDK downloads. Wrike has implemented an MCP Server enabling AI tools (Microsoft Copilot, Claude) to access and interact with Wrike data via MCP. An AI-native PPM tool should expose an MCP server to allow LLM-based agents to query portfolio health, create work packages, update resource assignments, and run what-if scenarios — enabling natural-language portfolio intelligence without custom API integration.

---

## Similar Products — Developer Documentation & APIs

### OpenProject
- **Description:** The leading open-source PPM tool with REST API, HATEOAS architecture, and OpenAPI 3.1 specification. Full portfolio, project, work package, resource, and time tracking data is accessible via API.
- **API Documentation:** https://www.openproject.org/docs/api/
- **OpenAPI Spec:** Available at `/api/v3/spec.yml` and `/api/v3/spec.json` on any instance; interactive explorer at `/api/docs`
- **SDKs/Libraries:** No official SDK; the API is consumed directly via HTTP; community libraries exist for Python and Ruby
- **Developer Guide:** https://www.openproject.org/docs/api/introduction/
- **Additional APIs:** BCF REST API for BIM project management (https://www.openproject.org/docs/api/bcf-rest-api/); SCIM API for user provisioning (RFC 7643/7644)
- **Standards:** REST/JSON, OpenAPI 3.1, HATEOAS/JSONAPI, SCIM 2.0
- **Authentication:** OAuth 2.0, API key (Bearer token)

### Oracle Primavera P6 EPPM
- **Description:** Industry-standard capital project PPM for construction, energy, aerospace, and government. REST API exposes projects, activities, resources, baselines, EVM data, and resource assignments.
- **API Documentation (Release 26):** https://docs.oracle.com/en/industries/construction-engineering/primavera-p6-project/26/rest-api/
- **API Documentation (Release 25):** https://docs.oracle.com/cd/G18294_01/English/Integration_Documentation/rest_api/index.html
- **Web Services Programming Guide:** https://docs.oracle.com/cd/G18294_01/English/Integration_Documentation/p6_eppm_web_services_programming/102895.htm
- **SDKs/Libraries:** Java and JavaScript HTTP libraries; cURL; no official SDK
- **Standards:** REST/JSON, OAuth 2.0 (Bearer token), SOAP (legacy web services also available)
- **Authentication:** OAuth 2.0 token (generated via Basic authentication); Bearer token scheme

### Microsoft Project for the Web / Planner (via Microsoft Graph)
- **Description:** Microsoft's next-generation cloud PPM integrated with Microsoft 365 and Copilot AI. Project data is accessible via Microsoft Graph API and Dataverse OData API.
- **API Documentation:** https://learn.microsoft.com/en-us/graph/use-the-api
- **Graph API Developer Centre:** https://developer.microsoft.com/en-us/graph
- **Dataverse OData:** Microsoft Dynamics 365 OData endpoint; Project for the Web data lives in Dataverse tables accessible via OData v4
- **SDKs/Libraries:** Microsoft Graph SDK for JavaScript, Python, Java, C#, Go, PHP — https://learn.microsoft.com/en-us/graph/sdks/sdks-overview
- **Standards:** REST/JSON, OData v4, OpenAPI, OAuth 2.0 / Microsoft Entra ID (Azure AD)
- **Authentication:** OAuth 2.0 via Microsoft Entra ID; personal access tokens for development
- **Note:** Full programmatic CRUD for Project for the Web tasks and portfolios is available through Dataverse OData rather than Graph API; Graph API coverage of Project data is limited as of 2026

### Planview Portfolios (Formerly Planview Enterprise One)
- **Description:** Enterprise-grade strategic portfolio management platform. REST API provides access to portfolios, projects, resources, financial data, and work packages.
- **API Documentation:** Available via Planview Customer Success Portal (authentication required); Swagger/OpenAPI explorer at `https://<account>.pvcloud.com/<server>/swagger/index.html`
- **API Overview:** https://apitracker.io/a/planview
- **SDKs/Libraries:** No official SDK; API consumed via HTTP with OAuth token; Power Automate and Azure Data Factory connectors available for data pipeline integration
- **Standards:** REST/JSON, OAuth 2.0
- **Authentication:** OAuth 2.0; access token fetched via client credentials grant for server-to-server integration

### Jira (Atlassian)
- **Description:** The dominant software development issue tracker. A PPM tool integrating with software delivery portfolios must consume Jira's API to pull work items, sprints, epics, and velocity data into portfolio health views.
- **API Documentation (Cloud v3):** https://developer.atlassian.com/cloud/jira/platform/rest/v3/intro/
- **API Documentation (Software):** https://developer.atlassian.com/cloud/jira/software/rest/
- **SDKs/Libraries:** Jira REST Java Client (JRJC) for Java; community libraries for Python (jira), JavaScript (@atlassian/jira-rest-client); official Forge platform SDK for app development
- **Developer Guide:** https://developer.atlassian.com/cloud/jira/platform/
- **Standards:** REST/JSON, OpenAPI, OAuth 2.0
- **Authentication:** OAuth 2.0 (3LO for user-context); API tokens (Basic auth with base64 encoding) for server-to-server

### Azure DevOps (Microsoft)
- **Description:** Microsoft's software delivery platform. A PPM tool tracking software project portfolios integrates with Azure DevOps to pull work items, pipelines, and delivery metrics.
- **API Documentation:** https://learn.microsoft.com/en-us/rest/api/azure/devops/?view=azure-devops-rest-7.2
- **SDKs/Libraries:** azure-devops-node-api (Node.js/TypeScript); azure-devops-python-api (Python); .NET client libraries — https://learn.microsoft.com/en-us/azure/devops/integrate/
- **Developer Guide:** https://learn.microsoft.com/en-us/azure/devops/integrate/how-to/call-rest-api?view=azure-devops
- **Standards:** REST/JSON, OAuth 2.0 / Microsoft Entra ID; Personal Access Tokens for development
- **Authentication:** Microsoft Entra ID (recommended for production); Personal Access Tokens; service principals and managed identities for CI/CD automation

### Smartsheet
- **Description:** Spreadsheet-familiar work management platform with portfolio dashboards and REST API. Relevant as an integration source for organizations tracking project data in Smartsheet sheets.
- **API Documentation:** https://developers.smartsheet.com/api/smartsheet/introduction
- **OpenAPI Reference:** https://developers.smartsheet.com/api/smartsheet/openapi
- **SDKs/Libraries:** Official SDKs for Python, Java, Node.js/JavaScript, and C# — https://developers.smartsheet.com/
- **Developer Guide:** https://developers.smartsheet.com/api/smartsheet/guides/getting-started
- **Standards:** REST/JSON, OpenAPI
- **Authentication:** API access token (Bearer); OAuth 2.0 for third-party app integrations

### Wrike
- **Description:** Work management and project tracking platform with portfolio views. REST API provides access to folders (portfolios), tasks, projects, and resource management. Wrike has also launched an MCP server for AI agent integration.
- **API Documentation:** https://developers.wrike.com/
- **SDKs/Libraries:** Community .NET client (Taviloglu.Wrike.ApiClient on GitHub); official documentation focuses on REST/HTTP; 400+ native connectors via Wrike Integrate
- **Developer Guide:** https://developers.wrike.com/overview/
- **Standards:** REST/JSON, OAuth 2.0; MCP Server available for AI agent integration
- **Authentication:** OAuth 2.0; API tokens for personal integrations

### Celoxis
- **Description:** Mid-market PPM platform with REST API covering projects, tasks, resources, budgets, and custom reports. Good reference for mid-market PPM API surface.
- **API Documentation:** https://celoxis.atlassian.net/wiki/x/33ndBg
- **API Endpoint:** `https://app.celoxis.com/psa/api/v2/`
- **SDKs/Libraries:** No official SDK; REST/HTTP with API key authentication; Pipedream integration platform connectors available
- **Standards:** REST/JSON
- **Authentication:** Personal access token (API key); obtained from user account API Access Token page

---

## Notes

**Emerging standard — MCP as PPM integration layer:** The rapid growth of Model Context Protocol (10,000+ public servers, 97M monthly SDK downloads as of 2026) means that exposing a PPM MCP server is becoming an expected integration pattern for AI-native tools. Wrike's MCP server is the first PPM-category implementation; an AI-native PPM tool building MCP-first would gain an early-mover advantage in AI agent integration.

**Data model convergence around ISO 21500 family:** ISO 21500/21502/21503/21504/21505 provide a coherent conceptual model for portfolio → programme → project → work package hierarchy that closely maps to the data models of OpenProject, Planview, and Oracle Primavera P6. Aligning a new PPM tool's core data model to this standard family would ease integration with existing enterprise governance processes and improve procurement prospects in regulated industries.

**OData for ERP integration:** Any PPM tool requiring bi-directional budget synchronization with SAP or Microsoft Dynamics must implement OData v4 client capabilities. This is not optional for enterprise market penetration — CFO-level PPM use cases depend on ERP financial data flowing into portfolio dashboards.

**ANSI/EIA-748 gap:** No open-source PPM tool currently implements EVM per ANSI/EIA-748. This represents a niche but high-value opportunity for capital project markets (construction, defense, government) where EVM compliance is a contract requirement and Oracle Primavera P6 currently has a near-monopoly.

**BCF API for AEC markets:** The buildingSMART BIM Collaboration Format (BCF) REST API, supported by OpenProject, is a niche but important integration standard for architecture, engineering, and construction (AEC) organizations managing BIM-linked project portfolios. Implementing BCF API support would open the AEC vertical market.
