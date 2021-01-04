# DHCP Server

## Interface OKD

### General Options
- Enable DHCP server on OKD interface
- Subnet: 10.10.1.0
- Subnet mask: 255.255.255.0
- Available range: 10.10.1.1 - 10.1.1.254
- Range:

     |From|To|
     |-|-|
     |10.10.1.100|10.1.1.254|

### DHCP Static Mappings for this Interface

|Static ARP|MAC address|IP address|Hostname|
|-|-|-|-|
|[x]|6a:7b:d0:7f:5f:e0|10.10.1.10|okd4-bootstrap|
|[x]|76:c4:8d:d2:1c:4b|10.10.1.20|okd4-control-plane-1|
|[x]|22:2f:f7:24:d5:f6|10.10.1.21|okd4-control-plane-2|
|[x]|ce:c2:9d:a6:6d:f2|10.10.1.22|okd4-control-plane-3|
|[x]|a2:ea:17:4c:80:11|10.10.1.30|okd4-compute-1|
|[x]|c2:5f:7e:9d:e9:b9|10.10.1.31|okd4-compute-2|
|[x]|d2:fe:f4:bb:62:9d|10.10.1.50|okd4-services|

