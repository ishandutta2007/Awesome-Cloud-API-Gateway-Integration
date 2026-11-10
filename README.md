# Awesome-Cloud-API-Gateway-Integration

# Top Cloud API Gateway & Integration Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on API Traffic Management, Security Policy Enforcement & Service Connectivity*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud API Gateway & Integration**. These tools provide the entry point for API traffic—handling authentication, rate limiting, request transformation, and routing to backend services across cloud and hybrid environments. They are the control plane for API security, observability, and lifecycle management.

**Examples** include Freshworks API Gateway, Kong Gateway, AWS API Gateway, Apigee, Tyk, Azure API Management, Gravitee.io, MuleSoft Anypoint, Traefik, and WSO2 API Manager (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted API gateways, open-source management planes, and community-maintained proxies—ideal for platform engineers, API architects, and developers building transparent, vendor-neutral traffic management without per-request cloud billing surprises.

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Freshworks API Gateway](https://www.freshworks.com/)** | API access layer for Freshworks products (Freshdesk, Freshservice, Freshsales). Provides programmatic access to tickets, contacts, and workflow automation. API access is included in every product plan; rate limits scale with tier (100/min on Starter up to 500/min on Enterprise for Freshservice) [citation:1][citation:11]. | Freshdesk from $19/agent/month; Freshsales from $9/user/month (annual billing) [citation:1] | Freshdesk free for 1–2 agents for 6 months; Freshsales free plan for up to 3 users; 14–21 day free trials [citation:1] |
| **[Kong Gateway (Konnect)](https://konghq.com/)** | Cloud-native API gateway available as self-hosted Enterprise or managed Konnect. Konnect uses per-gateway subscription with 1M included requests/month, then per-million overages. AI Gateway and MCP features ride within Plus/Enterprise envelopes. Self-hosted TCO typically 30–60% above base subscription in year one [citation:2][citation:12]. | Self-hosted Enterprise: ~$40K–$80K/year (small deployments); Konnect: per-gateway subscription + overage [citation:2] | No permanent free tier for Konnect; self-hosted Kong OSS is free (MPL-2.0); Konnect trial available via sales |
| **[AWS API Gateway](https://aws.amazon.com/api-gateway/)** | Fully managed API gateway for REST, HTTP, and WebSocket APIs. Pay-per-request with no minimum fees. HTTP APIs at ~$1.00/million requests (first 300M); REST APIs at ~$3.50/million. Optional caching and data transfer billed separately [citation:13]. | $1.00/million HTTP API calls (first 300M); $3.50/million REST API calls | **New AWS customers**: 1M API calls/month for 12 months (HTTP, REST, and WebSocket each); $200 Free Tier credits for new accounts from July 2025 [citation:13] |
| **[Apigee (Google Cloud)](https://cloud.google.com/apigee)** | Google Cloud's enterprise API management platform with gateway, analytics, developer portal, and API monetization. Pay-as-you-go available alongside subscription plans; gateway nodes billed per-minute, analytics per-request, networking separately. 60-day evaluation plan available [citation:4][citation:14]. | Pay-as-you-go: gateway nodes per-minute + analytics per-request; Subscription: quote-only | 60-day free evaluation plan; no permanent free tier for production [citation:14] |
| **[Tyk](https://tyk.io/)** | Open-core API gateway (MPL-2.0 for gateway) with Dashboard, Developer Portal, and multi-data-center bridge as paid components. Core is usage-based; Professional is flat-priced unlimited. Hybrid mode keeps gateways in your cluster with Tyk Cloud control plane [citation:5][citation:15]. | Core: usage-based (quoted); Professional: flat unlimited (quoted); no public list prices [citation:5] | **48-hour fully-featured Tyk Cloud trial** (no credit card); Tyk Gateway OSS is free forever (MPL-2.0) [citation:15] |
| **[Azure API Management](https://azure.microsoft.com/en-us/products/api-management/)** | Microsoft's API gateway and management service with Consumption, Developer, Basic, Standard, Premium, and v2 tiers. Consumption tier has no fixed cost—billed per request beyond threshold. Self-hosted gateway available for hybrid deployments [citation:6]. | Consumption: pay-per-execution; Basic: from ~$0.07/hour (~$51/month) [citation:6] | Consumption tier: first 1M requests/month free (Azure free grant applies); Developer tier for evaluation (no SLA) |
| **[Gravitee.io](https://www.gravitee.io/)** | Open-core API management supporting REST, SOAP, and event-driven APIs (Kafka, MQTT). Planet tier at $2,500/month for one production gateway. AI features (LLM, MCP, A2A proxies) are Enterprise add-ons [citation:7]. | Planet: $2,500/month (1 production + 1 non-production gateway, 1 module); Galaxy/Universe: custom [citation:7] | No free tier for managed platform; Gravitee OSS components available under Apache 2.0; demo via sales |
| **[MuleSoft Anypoint](https://www.mulesoft.com/)** | Enterprise iPaaS and API management platform. vCore-based pricing; typical contract minimums in mid-five to low-six figures annually. Implementation services typically 20–40% of first-year software cost [citation:8]. | Quote-only (median ~$68,695/year per Vendr data) [citation:8] | 30-day free trial available; no free tier |
| **[Traefik Hub](https://traefik.io/)** | Kubernetes-native API gateway built on open-source Traefik Proxy (MIT). Hub adds WAF, advanced auth (OAuth2, OIDC, OPA), multi-cluster management, and centralized control plane. AI/MCP Gateway sold as add-on [citation:9]. | Quote-only (all commercial tiers gated behind sales contact) [citation:9] | **30-day free trial** for API Gateway tier; Traefik Proxy OSS is free forever (MIT) [citation:9] |
| **[WSO2 API Manager](https://wso2.com/api-manager/)** | Fully open-source (Apache 2.0) API management suite with control plane, gateway, and developer portal. SaaS Pay-As-You-Go from $119/month for up to 10 managed interfaces and 10M gateway events. Self-hosted Enterprise custom-priced [citation:10]. | Pay-As-You-Go: from $119/month (10 interfaces, 10M events); Enterprise: custom [citation:10] | **30-day free trial**: 5 managed interfaces, 1M gateway events, 1 hybrid gateway, 1 developer portal [citation:10] |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Kong Gateway (OSS)](https://github.com/Kong/kong)** | [![Stars](https://img.shields.io/github/stars/Kong/kong?style=social&color=white)](https://github.com/Kong/kong/stargazers) | The most widely deployed open-source API gateway. Lua/OpenResty-based with a rich plugin ecosystem for auth, rate limiting, logging, and transformation. Enterprise adds RBAC, SSO, and MCP proxy [citation:2]. |
| **[Traefik Proxy](https://github.com/traefik/traefik)** | [![Stars](https://img.shields.io/github/stars/traefik/traefik?style=social&color=white)](https://github.com/traefik/traefik/stargazers) | Cloud-native reverse proxy and load balancer (MIT). Auto-discovers services from Kubernetes, Docker, and Consul. Hub commercial tier adds WAF, advanced auth, and centralized management [citation:9]. |
| **[Tyk Gateway](https://github.com/TykTechnologies/tyk)** | [![Stars](https://img.shields.io/github/stars/TykTechnologies/tyk?style=social&color=white)](https://github.com/TykTechnologies/tyk/stargazers) | Open-source API gateway (MPL-2.0). Dashboard, Developer Portal, and MDCB are paid components. Supports REST, GraphQL, TCP, and UDP; MCP Gateway implements 2025-11-25 MCP revision [citation:5]. |
| **[Apache APISIX](https://github.com/apache/apisix)** | [![Stars](https://img.shields.io/github/stars/apache/apisix?style=social&color=white)](https://github.com/apache/apisix/stargazers) | High-performance cloud-native API gateway built on NGINX + etcd. Rich plugin ecosystem for auth, rate-limiting, observability, and traffic splitting. Apache 2.0 licensed. |
| **[Gravitee API Management (OSS)](https://github.com/gravitee-io/gravitee-api-management)** | [![Stars](https://img.shields.io/github/stars/gravitee-io/gravitee-api-management?style=social&color=white)](https://github.com/gravitee-io/gravitee-api-management/stargazers) | Apache-2.0 open-core API management covering HTTP and event-driven APIs (Kafka, MQTT, webhooks). AI/LLM features are Enterprise add-ons [citation:7]. |
| **[WSO2 API Manager](https://github.com/wso2/product-apim)** | [![Stars](https://img.shields.io/github/stars/wso2/product-apim?style=social&color=white)](https://github.com/wso2/product-apim/stargazers) | Fully open-source (Apache 2.0) API management suite with gateway, publisher, and developer portal. Self-hosted free to run; support/updates via subscription [citation:10]. |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[KrakenD](https://github.com/krakend/krakend-ce)** | [![Stars](https://img.shields.io/github/stars/krakend/krakend-ce?style=social&color=white)](https://github.com/krakend/krakend-ce/stargazers) | Ultra-fast stateless API gateway in Go with declarative configuration. Aggregates multiple backend services into a single API endpoint without writing code. |
| **[Apache Camel](https://github.com/apache/camel)** | [![Stars](https://img.shields.io/github/stars/apache/camel?style=social&color=white)](https://github.com/apache/camel/stargazers) | Integration framework with 300+ connectors (REST, JMS, file, cloud). Can be used to build custom API integration flows as a complement or alternative to a dedicated gateway. |
| **[Envoy Gateway](https://github.com/envoyproxy/gateway)** | [![Stars](https://img.shields.io/github/stars/envoyproxy/gateway?style=social&color=white)](https://github.com/envoyproxy/gateway/stargazers) | Kubernetes-native gateway built on Envoy Proxy, implementing the Gateway API specification. CNCF project with strong community backing. |

**Frameworks for building custom systems**: Combine **Kong OSS** or **Apache APISIX** for API routing and policy enforcement, **Traefik Proxy** for Kubernetes-native ingress, and **Apache Camel** for integration flow orchestration—creating a fully self-hosted API gateway stack with no per-request cloud billing.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- API gateways handle authentication tokens and route all API traffic; enforce least-privilege policies, rate limiting, and audit logging.
- Cloud gateway pricing models (per-request, per-node, per-gateway) vary dramatically; model total cost based on actual traffic volume and required enterprise features before committing.

---

**Made for platform engineers, API architects, DevOps teams, and developers building traffic management infrastructure.**  
Let's make API gateway integration more open, observable, and cost-transparent.
