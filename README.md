# frp (frp)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

frp is an open-source fast reverse proxy that exposes services running behind a NAT or firewall to the public internet. Both the server (frps) and the client (frpc) include built-in HTTP admin APIs that operators can use to inspect runtime status, manage proxies and visitors, hot-reload configuration, and scrape Prometheus metrics.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/frp/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/frp/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Access:** Open Source

## Tags

- NAT Traversal
- Reverse Proxy
- Tunneling
- Open Source

## Timestamps

- **Created:** 2026-03-27
- **Modified:** 2026-05-19

## APIs

### frp Server Admin API

The frp server admin API is the HTTP control plane exposed by frps on its dashboard web server. It returns version and traffic information for the server, lists connected clients, lists and inspects active proxies of any type, returns daily traffic counters per proxy, and lets operators clear proxies that are offline. The API is secured with HTTP Basic auth using the dashboard user and password configured in the frps webServer block.

- **Human URL:** [https://gofrp.org/en/docs/features/common/server-dashboard/](https://gofrp.org/en/docs/features/common/server-dashboard/)
- **Base URL:** `http://localhost:7500`

#### Tags

- NAT Traversal
- Reverse Proxy
- Server Admin
- Dashboard

#### Properties

- [Documentation](https://gofrp.org/en/docs/features/common/server-dashboard/)
- [OpenAPI](openapi/frp-server-admin-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/frp-server-admin-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/frp-server-admin-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### frp Client Admin API

The frp client admin API is the HTTP control plane exposed by frpc on its local web server. It supports hot-reloading the proxy and visitor configuration, stopping the running client, returning the active config, replacing the active config, querying per-proxy and per-visitor status, and (when a configuration store is enabled) listing, creating, updating, and deleting persisted proxy and visitor definitions. The API is secured with HTTP Basic auth using the user and password configured in the frpc webServer block.

- **Human URL:** [https://gofrp.org/en/docs/reference/client-configures/](https://gofrp.org/en/docs/reference/client-configures/)
- **Base URL:** `http://127.0.0.1:7400`

#### Tags

- NAT Traversal
- Reverse Proxy
- Client Admin
- Configuration

#### Properties

- [Documentation](https://gofrp.org/en/docs/reference/client-configures/)
- [OpenAPI](openapi/frp-client-admin-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/frp-client-admin-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/frp-client-admin-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://gofrp.org/)
- [Documentation](https://gofrp.org/en/docs/)
- [Getting Started](https://gofrp.org/en/docs/setup/)
- [Source Code](https://github.com/fatedier/frp)
- [Issues](https://github.com/fatedier/frp/issues)
- [Releases](https://github.com/fatedier/frp/releases)
- [License](https://github.com/fatedier/frp/blob/master/LICENSE)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
