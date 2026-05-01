# frp (frp)

frp is an open-source fast reverse proxy that exposes services running behind a NAT or firewall to the public internet. Both the server (frps) and the client (frpc) include built-in HTTP admin APIs that operators can use to inspect runtime status, manage proxies and visitors, hot-reload configuration, and scrape Prometheus metrics.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/frp/refs/heads/main/apis.yml)

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
- **Modified:** 2026-04-28

## APIs

### frp Server Admin API

The frp server admin API is the HTTP control plane exposed by frps on its dashboard web server. It returns version and traffic information for the server, lists connected clients, lists and inspects active proxies of any type, returns daily traffic counters per proxy, and lets operators clear proxies that are offline. The API is secured with HTTP Basic auth using the dashboard user and password configured in the frps webServer block.

**Human URL:** https://gofrp.org/en/docs/features/common/server-dashboard/

**Base URL:** `http://localhost:7500`

#### Tags

- NAT Traversal, Reverse Proxy, Server Admin, Dashboard

#### Properties

- [Documentation](https://gofrp.org/en/docs/features/common/server-dashboard/)
- [OpenAPI](openapi/frp-server-admin-api-openapi.yml)

### frp Client Admin API

The frp client admin API is the HTTP control plane exposed by frpc on its local web server. It supports hot-reloading the proxy and visitor configuration, stopping the running client, returning the active config, replacing the active config, querying per-proxy and per-visitor status, and (when a configuration store is enabled) listing, creating, updating, and deleting persisted proxy and visitor definitions. The API is secured with HTTP Basic auth using the user and password configured in the frpc webServer block.

**Human URL:** https://gofrp.org/en/docs/reference/client-configures/

**Base URL:** `http://127.0.0.1:7400`

#### Tags

- NAT Traversal, Reverse Proxy, Client Admin, Configuration

#### Properties

- [Documentation](https://gofrp.org/en/docs/reference/client-configures/)
- [OpenAPI](openapi/frp-client-admin-api-openapi.yml)

## Artifacts

| Type | File | Description |
|------|------|-------------|
| OpenAPI | [openapi/frp-server-admin-api-openapi.yml](openapi/frp-server-admin-api-openapi.yml) | frps dashboard admin API |
| OpenAPI | [openapi/frp-client-admin-api-openapi.yml](openapi/frp-client-admin-api-openapi.yml) | frpc local admin API |

## Common Properties

- [Website](https://gofrp.org/)
- [Documentation](https://gofrp.org/en/docs/)
- [GettingStarted](https://gofrp.org/en/docs/setup/)
- [SourceCode](https://github.com/fatedier/frp)
- [Issues](https://github.com/fatedier/frp/issues)
- [Releases](https://github.com/fatedier/frp/releases)
- [License](https://github.com/fatedier/frp/blob/master/LICENSE)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
