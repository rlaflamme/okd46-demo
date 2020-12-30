# DNS Resolver

## General Settings

### General DNS Resolver Options
- Enable DNS resolver
- Enable DNSSEC Support
- Register DHCP leases in the DNS Resolver
- Register DHCP static mappings in the DNS Resolver

### Custom Options

```
server:
local-data: "etcd-server-ssl._tcp.lab.okd.local.    86400     IN    SRV     0    10    2380    etcd-0.lab."
local-data: "etcd-server-ssl._tcp.lab.okd.local.    86400     IN    SRV     0    10    2380    etcd-1.lab."
local-data: "etcd-server-ssl._tcp.lab.okd.local.    86400     IN    SRV     0    10    2380    etcd-2.lab."
local-zone: "apps.lab.okd.local" redirect
local-data: "apps.lab.okd.local IN A 10.10.1.50"
local-data-ptr: "10.10.1.10 okd4-bootstrap.lab.okd.local"
local-data-ptr: "10.10.1.20 okd4-control-plane-1.lab.okd.local"
local-data-ptr: "10.10.1.21 okd4-control-plane-2.lab.okd.local"
local-data-ptr: "10.10.1.22 okd4-control-plane-3.lab.okd.local"
local-data-ptr: "10.10.1.30 okd4-compute-1.lab.okd.local"
local-data-ptr: "10.10.1.31 okd4-compute-2.lab.okd.local"
local-data-ptr: "10.10.1.50 api.lab.okd.local"
local-data-ptr: "10.10.1.50 api-int.lab.okd.local"
```

### Host Overrides

|Host|Parent domain of host|IP return for host|Description|
|-|-|-|-|
|api|lab.okd.local|10.10.1.50|Load Balancer IP|
|api-int|lab.okd.local|10.10.1.50|Load Balancer IP|
|apps|lab.okd.local|10.10.1.50|Load Balancer IP|
|etcd-0|lab.okd.local|10.10.1.20|alias for etcd's control-plane-1|
|etcd-1|lab.okd.local|10.10.1.21|alias for etcd's control-plane-2|
|etcd-2|lab.okd.local|10.10.1.22|alias for etcd's control-plane-3|
|okd4-bootstrap|lab.okd.local|10.10.1.10|bootstrap host|
|okd4-compute-1|lab.okd.local|10.10.1.30|compute-1|
|okd4-compute-2|lab.okd.local|10.10.1.30|compute-2|
|okd4-control-plane-1|lab.okd.local|10.10.1.20|control-plane-1|
|okd4-control-plane-2|lab.okd.local|10.10.1.21|control-plane-2|
|okd4-control-plane-3|lab.okd.local|10.10.1.22|control-plane-3|

## Advanced Settings
- Defaults (Leave as-is)

## Access Lists

|Access List Name|Action|
|-|-|
|WAN PASS|allow|

