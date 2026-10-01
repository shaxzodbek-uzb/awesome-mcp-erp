# Awesome MCP ERP [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of Model Context Protocol (MCP) servers, agents, and production patterns for business software — ERP, CRM, accounting, e-commerce, and vertical SaaS.

[Model Context Protocol](https://modelcontextprotocol.io) lets AI agents call real systems through typed tools. Most MCP lists are horizontal and bury business systems in a sub-section, or stop at infrastructure. This one is the opposite: a focused, opinionated catalog of **business-domain MCP servers** (the systems companies actually run on) plus the **multi-tenant auth, consent, observability, and build patterns** you need to put them into production.

Entries are real, maintained, and documented projects, each with a one-line note on what it does. Vendor-published (official) servers are described as such. Suggestions are welcome — open a pull request.

## Contents

- [ERP](#erp)
- [CRM & Sales](#crm--sales)
- [Accounting & Finance](#accounting--finance)
- [E-commerce & Payments](#e-commerce--payments)
- [Vertical SaaS](#vertical-saas)
- [Agents over Business MCP](#agents-over-business-mcp)
- [Multi-Tenant & OAuth 2.1 Auth](#multi-tenant--oauth-21-auth)
- [Scopes, Consent & RBAC](#scopes-consent--rbac)
- [Audit, Observability & Compliance](#audit-observability--compliance)
- [Building a Production MCP Server](#building-a-production-mcp-server)
- [Reference Architectures & Case Studies](#reference-architectures--case-studies)
- [Specs, Standards & Further Reading](#specs-standards--further-reading)

## ERP

*MCP servers that connect agents to ERP systems and their documents, records, and reports.*

- [NetSuite AI Connector Service](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/article_7200233106.html) - Official Oracle NetSuite MCP service connecting external AI clients to NetSuite data and workflows under the account's role-based security, with prebuilt and custom tools.
- [SAP/mdk-mcp-server](https://github.com/SAP/mdk-mcp-server) - Official SAP MCP server for AI-assisted development of SAP Mobile Development Kit (MDK) applications, providing project context, templates, best-practice guidelines, and CLI access.
- [D365FO-claude-connector](https://github.com/zhound420/D365FO-claude-connector) - MCP server for Microsoft Dynamics 365 Finance & Operations exposing OData metadata discovery, querying, aggregation, and guarded write operations with production write-blocking.
- [dsvantien/netsuite-mcp-server](https://github.com/dsvantien/netsuite-mcp-server) - MCP server bridging IDE clients to NetSuite's AI Connector Service via OAuth 2.0 with PKCE, exposing SuiteQL queries, reports, saved searches, and record operations.
- [Frappe Assistant Core](https://github.com/buildswithpaul/Frappe_Assistant_Core) - MCP server installed as a Frappe app that exposes ERPNext documents, search, reports, workflows, and analytics to LLMs within the authenticated user's permissions.
- [mcp-abap-adt (fr0ster)](https://github.com/fr0ster/mcp-abap-adt) - MCP server for SAP ABAP development via ADT, with CRUD on ABAP artifacts, where-used/dependency analysis, and transport management across ECC, S/4HANA, and BTP ABAP Cloud.
- [mcp-business-central](https://github.com/knowall-ai/mcp-business-central) - MCP server for Microsoft Dynamics 365 Business Central that performs CRUD operations on entities such as customers, contacts, sales orders, and invoices through the v2.0 API with OData filtering.
- [mcp-server-odoo](https://github.com/ivnvxd/mcp-server-odoo) - MCP server for Odoo ERP that lets AI assistants search, read, create, update, and delete records via XML-RPC with API-key or username/password auth.
- [erpipe-org/mcp-odoo](https://github.com/erpipe-org/mcp-odoo) - MCP server turning an Odoo 16+ database into 41 tools with approval-token gated writes, live metadata validation, per-instance routing for multi-instance estates, XML-RPC and JSON-2 transports, and optional OAuth 2.1.
- [rakeshgangwar/erpnext-mcp-server](https://github.com/rakeshgangwar/erpnext-mcp-server) - TypeScript MCP server that connects AI assistants to ERPNext through the Frappe REST API, exposing documents as resources plus tools to query, create, update, submit, cancel, and run reports.

## CRM & Sales

*MCP servers for CRM and sales platforms — contacts, companies, deals, pipelines, and activities.*

- [FirstSales MCP](https://developer.firstsales.io/agents/mcp-server) - Official hosted FirstSales CRM MCP for retrieving contacts, deals, lists and workflows, and creating contacts in an approved workspace via Streamable HTTP and OAuth with PKCE; requires an eligible paid plan.
- [HubSpot MCP Server](https://developers.hubspot.com/ai-tools/mcp) - Official HubSpot MCP server (npm @hubspot/mcp-server) giving agents read/write access to CRM contacts, companies, deals, tickets, and engagements.
- [Salesforce DX MCP Server](https://github.com/salesforcecli/mcp) - Official Salesforce MCP server exposing 60+ tools for reading and managing Salesforce orgs, metadata, data, code analysis, and LWC development.
- [Zoho MCP](https://www.zoho.com/mcp/) - Official Zoho MCP platform connecting AI agents to Zoho CRM and other Zoho apps via standardized tools and data models.
- [attio-mcp-server (kesslerio)](https://github.com/kesslerio/attio-mcp-server) - Community MCP server for Attio CRM covering deals, tasks, lists, people, companies, records, and notes through consolidated operations.
- [hubspot-mcp (shinzo-labs)](https://github.com/shinzo-labs/hubspot-mcp) - Community MCP server implementing the HubSpot CRM API with companies, contacts, deals, engagements, associations, and batch operations.
- [mcp-crm (nxt3d)](https://github.com/nxt3d/mcp-crm) - Standalone TypeScript/SQLite MCP server providing self-contained CRM tools for contacts, interaction history, todos, and data export.
- [mcp-pipedrive (iamsamuelfraga)](https://github.com/iamsamuelfraga/mcp-pipedrive) - Community MCP server for Pipedrive CRM exposing 100+ tools across deals, contacts, organizations, activities, and files.
- [mcp-server-salesforce (tsmztech)](https://github.com/tsmztech/mcp-server-salesforce) - Community MCP server for Salesforce with SOQL/SOSL queries, object and field management, Apex execution, and debug log access.
- [twenty-crm-mcp-server (mhenry3164)](https://github.com/mhenry3164/twenty-crm-mcp-server) - Community MCP server for the open-source Twenty CRM with CRUD operations, dynamic schema discovery, and search across people, companies, tasks, and notes.

## Accounting & Finance

*MCP servers for accounting, bookkeeping, payments-adjacent, and financial-data platforms.*

- [Intuit QuickBooks Online MCP Server](https://github.com/intuit/quickbooks-online-mcp-server) - Official Intuit MCP server exposing QuickBooks Online as 145 tools across 29 entity types and 11 financial reports with OAuth 2.0.
- [Plaid AI Coding Toolkit](https://github.com/plaid/ai-coding-toolkit) - Official Plaid toolkit with a sandbox MCP server providing mock data generation, documentation search, sandbox tokens, and webhook simulation.
- [Xero Agent Toolkit](https://github.com/XeroAPI/xero-agent-toolkit) - Official Xero collection of example AI agents (LangChain, OpenAI Agents SDK, Google ADK) built on the Xero MCP server in Python and TypeScript.
- [Xero MCP Server](https://github.com/XeroAPI/xero-mcp-server) - Official Xero MCP server for contacts, invoices, payments, accounts, payroll, and financial reports via OAuth2 custom connections.
- [beancount-mcp](https://github.com/StdioA/beancount-mcp) - MCP server for the Beancount plaintext-accounting ledger that runs BQL queries and submits new transactions to the ledger file.
- [beanquery-mcp](https://github.com/vanto/beanquery-mcp) - Experimental MCP server that lets assistants query and analyze Beancount ledgers using Beancount Query Language via the beanquery tool.

## E-commerce & Payments

*MCP servers for online stores, marketplaces, and payment processors.*

- [BigCommerce Storefront MCP](https://www.bigcommerce.com/blog/storefront-mcp/) - Official BigCommerce Storefront MCP server letting AI agents search the catalog, build carts, and generate checkout URLs for guest shopping.
- [PayPal MCP Server](https://github.com/paypal/paypal-mcp-server) - Official PayPal MCP server with tools for invoicing, payments, refunds, disputes, subscriptions, shipment tracking, and transaction reporting.
- [Shopify Dev MCP](https://shopify.dev/docs/apps/build/ai-toolkit) - Official Shopify developer MCP server providing access to Shopify docs, API schemas, and code-validation tools for building apps.
- [Shopify Storefront MCP](https://shopify.dev/docs/apps/build/storefront-mcp) - Official per-store Shopify MCP server exposing catalog search, cart, checkout, and store-policy tools for AI shopping agents.
- [Square MCP Server](https://github.com/square/square-mcp-server) - Official Square MCP server bridging AI assistants to the Square Connect API for payments, customers, orders, items, and bookings.
- [Stripe Agent Toolkit (MCP)](https://github.com/stripe/ai) - Official Stripe toolkit exposing payment, billing, and knowledge-base operations to AI agents over MCP, plus a hosted server at mcp.stripe.com.
- [GeLi2001/shopify-mcp](https://github.com/GeLi2001/shopify-mcp) - Community MCP server for the Shopify Admin API to manage products, orders, and customers from MCP hosts like Claude and Cursor.
- [SGFGOV/medusa-mcp](https://github.com/SGFGOV/medusa-mcp) - Community MCP server for the Medusa JS SDK to automate store data, inventory, and admin operations on a Medusa e-commerce backend.
- [techspawn/woocommerce-mcp-server](https://github.com/techspawn/woocommerce-mcp-server) - Community MCP server for WooCommerce covering products, orders, customers, shipping, taxes, coupons, and reports via the WordPress REST API.

## Vertical SaaS

*MCP servers for industry-specific business software — healthcare, hospitality, education, real estate, and logistics.*

- [AWS HealthLake MCP Server](https://github.com/awslabs/mcp/tree/main/src/healthlake-mcp-server) - Provides 11 FHIR tools for full CRUD and advanced search operations against Amazon HealthLake datastores.
- [Repliers MCP Server](https://github.com/Repliers-io/mcp-server) - MCP server giving agents real-time access to MLS listings and market statistics via the Repliers real-estate API.
- [UPS MCP Server](https://github.com/UPS-API/ups-mcp) - Official MCP server for UPS APIs providing shipment tracking and address validation tools.
- [WSO2 FHIR MCP Server](https://github.com/wso2/fhir-mcp-server) - Exposes any HL7 FHIR server or API as an MCP server, letting agents search, retrieve, and analyze clinical resources with SMART-on-FHIR auth and FHIRPath filtering.
- [Canvas LMS MCP Server (vishalsachdev)](https://github.com/vishalsachdev/canvas-mcp) - MCP server for Canvas LMS with 90+ tools and agent skills for students and educators, including privacy-first anonymization of student data.
- [Guesty MCP Server](https://github.com/DLJRealty/guesty-mcp-server) - Connects MCP clients to a Guesty short-term-rental property-management account with 43 tools for reservations, guest messaging, pricing, financials, and calendars.
- [Lodgify MCP Server](https://github.com/Fast-Transients/lodgify-mcp-server) - MCP server for the Lodgify vacation-rental API exposing tools to manage properties, bookings, and calendar availability.
- [The Momentum FHIR MCP Server](https://github.com/the-momentum/fhir-mcp-server) - MCP server enabling LLM agents to perform full CRUD operations on FHIR healthcare resources through a standardized tool suite.

## Agents over Business MCP

*Frameworks and SDKs for building agents that orchestrate business MCP servers.*

- [Claude Agent SDK (Python)](https://github.com/anthropics/claude-agent-sdk-python) - Anthropic's Python SDK for building Claude agents that connect to external and in-process MCP servers via stdio, HTTP, and SDK transports.
- [Claude Agent SDK — Connect to external tools with MCP](https://code.claude.com/docs/en/agent-sdk/mcp) - Official Anthropic guide for connecting Claude agents to business MCP servers, with worked examples for GitHub, PostgreSQL, and Slack tools.
- [LangChain MCP Adapters](https://github.com/langchain-ai/langchain-mcp-adapters) - Official adapter that converts MCP server tools into LangChain/LangGraph agent tools, with a MultiServerMCPClient for multiple servers.
- [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) - OpenAI's framework for multi-agent workflows with first-class MCP support via stdio, streamable HTTP, SSE, and hosted MCP tools.
- [Pydantic AI](https://github.com/pydantic/pydantic-ai) - Type-safe Python agent framework with an MCP client for connecting agents to local and remote MCP tool servers.
- [Vercel AI SDK — MCP Tools](https://ai-sdk.dev/docs/ai-sdk-core/mcp-tools) - Official Vercel AI SDK guide for wiring agents to MCP servers and converting MCP capabilities into AI SDK tools over HTTP, SSE, and stdio.

## Multi-Tenant & OAuth 2.1 Auth

*Securing business MCP servers for multi-tenant use with OAuth 2.1, PKCE, and dynamic client registration.*

- [Auth0 — Auth for MCP](https://auth0.com/ai/docs/mcp/intro/overview) - Auth0 guide for implementing the MCP authorization spec with Auth0 as the OAuth 2.1/OIDC authorization server, including token issuance, validation, and dynamic client registration.
- [FastMCP — Authentication](https://gofastmcp.com/servers/auth/authentication) - Documentation for FastMCP's server-side auth: TokenVerifier/JWT validation, OAuthProxy for upstream providers without DCR (GitHub, Google, Azure, AWS), remote OAuth with DCR-capable IdPs, and MultiAuth composition.
- [MCP Authorization Specification](https://modelcontextprotocol.io/specification/draft/basic/authorization) - Official MCP spec defining the OAuth 2.1 authorization flow for HTTP transports, including PKCE, RFC 9728 protected-resource metadata, RFC 8707 resource indicators, token audience validation, and step-up scope challenges.
- [modelcontextprotocol/ext-auth](https://github.com/modelcontextprotocol/ext-auth) - Official repository of optional MCP authorization extensions (Enterprise-Managed Authorization, Client Credentials OAuth) that layer additional auth mechanisms on top of the core protocol.
- [Scalekit — OAuth authorization server for MCP](https://docs.scalekit.com/authenticate/mcp/quickstart/) - Scalekit guide for adding an OAuth 2.1 authorization server to an MCP server, covering dynamic client registration, protected-resource metadata, Bearer-token validation, and scope-based tool authorization.
- [Stytch — Remote MCP Server authorization](https://stytch.com/docs/connected-apps/guides/mcp-auth-overview) - Vendor guide for securing a remote MCP server with Stytch as the OAuth 2.1 IdP, covering PKCE, dynamic client registration, protected-resource and authorization-server metadata, and JWT access-token validation.
- [WorkOS AuthKit — MCP authorization](https://workos.com/docs/authkit/mcp) - Vendor guide for using WorkOS AuthKit/Connect as the OAuth 2.1 authorization server for an MCP server, covering JWT token validation, metadata discovery, and Client ID Metadata Documents.

## Scopes, Consent & RBAC

*Scoping tool access, gating execution, and capturing user consent with fine-grained authorization.*

- [Auth0 FGA: Control Access to MCP Tools (Quickstart)](https://auth0.com/ai/docs/mcp/get-started/secure-mcp-server-with-auth0-fga) - Official Auth0 guide for securing an MCP server with Auth0 FGA, using ReBAC with roles, groups, and temporal access to gate which tools an authenticated agent may call.
- [cerbos/cerbos-fastmcp](https://github.com/cerbos/cerbos-fastmcp) - FastMCP middleware that authorizes every MCP tool call, prompt request, and resource query against Cerbos policies, controlling both tool visibility and execution without modifying server code.
- [MCP Elicitation Specification](https://modelcontextprotocol.io/specification/draft/client/elicitation) - Official MCP spec section defining elicitation, the mechanism by which a server pauses a tool call to request structured input or user consent (form and URL modes) with client-side approve/decline/cancel controls.
- [OpenFGA: Authorization for MCP Servers](https://openfga.dev/docs/modeling/agents/mcp-authorization) - Official OpenFGA guide for modeling fine-grained, relationship-based control over which MCP tools an agent can invoke, covering public vs restricted tools, temporal grants, and ListObjects-based tool filtering.
- [Permit MCP Gateway](https://docs.permit.io/permit-mcp-gateway/) - Drop-in proxy between MCP clients and servers that adds identity-aware authorization, consent-based delegation, deny-by-default tool access, and an audit trail without changing existing servers.
- [permitio/permit-fastmcp](https://github.com/permitio/permit-fastmcp) - FastMCP middleware that intercepts MCP requests and validates each tool call against Permit.io RBAC/ABAC policies before execution, with tool arguments exposed as policy attributes.

## Audit, Observability & Compliance

*Tracing, auditing, and monitoring agent and MCP activity in production.*

- [MCP Logging Utility (spec)](https://modelcontextprotocol.io/specification/2025-06-18/server/utilities/logging) - Official MCP specification for structured server-to-client log notifications, a basis for auditing tool activity.
- [OpenTelemetry GenAI Semantic Conventions](https://opentelemetry.io/docs/specs/semconv/gen-ai/) - Vendor-neutral standard for naming and structuring GenAI and agent spans, metrics, and events.
- [Arize Phoenix](https://github.com/Arize-ai/phoenix) - Open-source AI observability and evaluation platform with OpenTelemetry-based tracing for LLM and agent applications.
- [Helicone](https://github.com/Helicone/helicone) - Open-source platform that logs, monitors, and tracks the cost of LLM requests through a proxy or async logging.
- [Langfuse](https://github.com/langfuse/langfuse) - Open-source LLM engineering platform for tracing, evaluating, and monitoring agents and their MCP tool calls.
- [OpenInference](https://github.com/Arize-ai/openinference) - OpenTelemetry semantic conventions and auto-instrumentation libraries for tracing LLM, agent, and tool-call activity.
- [OpenLLMetry](https://github.com/traceloop/openllmetry) - OpenTelemetry-based instrumentation that emits traces and metrics for LLM and agent calls to any OTel-compatible backend.
- [Pydantic Logfire](https://github.com/pydantic/logfire) - Observability SDK from the Pydantic team with OpenTelemetry tracing for Python apps, LLM calls, and MCP servers.

## Building a Production MCP Server

*SDKs, frameworks, and tooling for building and testing production MCP servers.*

- [Laravel MCP](https://laravel.com/docs/13.x/mcp) - Official Laravel team package for building MCP servers from Laravel apps, with tools, prompts, resources, and OAuth 2.1 via Passport or token auth via Sanctum.
- [MCP C# SDK](https://github.com/modelcontextprotocol/csharp-sdk) - Official C#/.NET SDK for MCP servers and clients, maintained in collaboration with Microsoft.
- [MCP Go SDK (official)](https://github.com/modelcontextprotocol/go-sdk) - Official Go SDK for MCP servers and clients, maintained in collaboration with Google, with a stable v1 API.
- [MCP Inspector](https://github.com/modelcontextprotocol/inspector) - Official visual testing and debugging tool for MCP servers, with a React web UI, a CLI mode for automation, and support for stdio/SSE/Streamable HTTP transports.
- [MCP Python SDK](https://github.com/modelcontextprotocol/python-sdk) - Official Python SDK for building MCP servers and clients, with tools, resources, prompts, and stdio/Streamable HTTP transports.
- [MCP Rust SDK (rmcp)](https://github.com/modelcontextprotocol/rust-sdk) - Official Rust SDK (rmcp crate) for MCP servers and clients built on the tokio async runtime, with procedural macros for tool definitions.
- [MCP Transports Specification](https://modelcontextprotocol.io/specification/2025-06-18/basic/transports) - Official MCP specification for stdio and Streamable HTTP transports, covering session management, resumability, and origin-validation security requirements for production deployments.
- [MCP TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk) - Official TypeScript SDK for MCP servers and clients on Node.js, Bun, and Deno, including stdio/Streamable HTTP transports and OAuth helpers.
- [FastMCP](https://github.com/PrefectHQ/fastmcp) - Pythonic framework for building MCP servers and clients that generates schemas and validation from typed Python functions, with server composition, OpenAPI integration, and built-in testing.
- [mcp-go (mark3labs)](https://github.com/mark3labs/mcp-go) - Community Go implementation of MCP with resources, tools, prompts, session management, and stdio/SSE/HTTP transports.

## Reference Architectures & Case Studies

*Engineering write-ups and case studies on running MCP and agents against business systems at scale.*

- [Block's Playbook for Designing MCP Servers](https://engineering.block.xyz/blog/blocks-playbook-for-designing-mcp-servers) - Block engineering blog distilling production lessons from 60+ internal MCP servers, covering workflow-first tool design, token-budget management, and OAuth-based authentication.
- [Code execution with MCP: Building more efficient agents (Anthropic)](https://www.anthropic.com/engineering/code-execution-with-mcp) - Anthropic engineering pattern for scaling agents across many MCP servers by presenting tools as code APIs with progressive, on-demand tool discovery to cut context/token costs.
- [Deploying Model Context Protocol (MCP) servers on Amazon ECS (AWS)](https://aws.amazon.com/blogs/containers/deploying-model-context-protocol-mcp-servers-on-amazon-ecs/) - AWS Containers blog walkthrough of a three-tier agent/MCP architecture on Amazon ECS with Fargate, Service Connect, Express Mode load balancing, private subnets, and streamable HTTP transport.
- [Introducing Atlassian's Remote Model Context Protocol (MCP) Server](https://www.atlassian.com/blog/announcements/remote-mcp-server) - Atlassian engineering announcement of its vendor-hosted remote MCP server for Jira and Confluence, with OAuth authentication and enforcement of existing permission boundaries.
- [MCP Demo Day: How 10 leading AI companies built MCP servers on Cloudflare](https://blog.cloudflare.com/mcp-demo-day/) - Cloudflare case-study roundup of production remote MCP servers shipped by Stripe, Block, Atlassian, PayPal, Asana, Linear, Intercom, Sentry, Webflow, and Anthropic.
- [Scaling MCP adoption: Cloudflare's enterprise reference architecture](https://blog.cloudflare.com/enterprise-mcp/) - Cloudflare reference architecture for enterprise MCP, covering remote servers on custom domains, Access-based auth, MCP server portals, DLP/policy enforcement, and AI Gateway token budgets.
- [Unlocking the power of Model Context Protocol (MCP) on AWS](https://aws.amazon.com/blogs/machine-learning/unlocking-the-power-of-model-context-protocol-mcp-on-aws/) - AWS Machine Learning blog on enterprise MCP integration patterns with Amazon Bedrock, IAM-based access control, and Streamable HTTP transport for horizontal scaling.
- [production-grade-mcp-agentic-system](https://github.com/FareedKhan-dev/production-grade-mcp-agentic-system) - Runnable reference implementation of a production MCP server: OAuth 2.1 with PKCE and JWKS validation, multi-tenant isolation via PostgreSQL row-level security, structured audit logs on a single trace id, plus circuit breakers, rate limiting and Prometheus/Jaeger wiring.

## Specs, Standards & Further Reading

*Specifications, standards, and background reading.*

- [Introducing the Model Context Protocol](https://www.anthropic.com/news/model-context-protocol) - Anthropic's announcement introducing MCP as an open standard for connecting AI to external systems.
- [MCP Registry](https://github.com/modelcontextprotocol/registry) - Official community-driven registry and REST API for discovering published MCP servers.
- [MCP Security Best Practices](https://modelcontextprotocol.io/docs/tutorials/security/security_best_practices) - Official MCP guidance on token handling, confused-deputy risks, and securing servers for production.
- [Model Context Protocol Specification](https://modelcontextprotocol.io/specification/2025-06-18) - The official MCP specification defining the protocol, transports, and authorization model.
- [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) - Official collection of reference MCP server implementations and a showcase of community servers.
- [OAuth 2.1 Authorization Framework (draft)](https://datatracker.ietf.org/doc/html/draft-ietf-oauth-v2-1) - The IETF OAuth 2.1 draft that the MCP authorization model builds on.
- [RFC 7591: OAuth 2.0 Dynamic Client Registration](https://datatracker.ietf.org/doc/html/rfc7591) - Lets MCP clients register with an authorization server at runtime without manual configuration.
- [RFC 8414: OAuth 2.0 Authorization Server Metadata](https://datatracker.ietf.org/doc/html/rfc8414) - Standard discovery document for OAuth authorization-server endpoints used in the MCP auth flow.
- [RFC 8707: Resource Indicators for OAuth 2.0](https://datatracker.ietf.org/doc/html/rfc8707) - Binds access tokens to a specific MCP server audience to prevent token reuse across services.
- [RFC 9728: OAuth 2.0 Protected Resource Metadata](https://datatracker.ietf.org/doc/html/rfc9728) - Defines the protected-resource metadata document MCP servers expose for authorization-server discovery.
- [Awesome MCP Servers](https://github.com/punkpeye/awesome-mcp-servers) - Broad horizontal catalog of MCP servers across all domains, complementary to this business-focused list.

## Contributing

Contributions are welcome! Read the [contribution guidelines](contributing.md) first, then open a pull request. Every entry must be a real, maintained, documented project relevant to MCP and business software.
