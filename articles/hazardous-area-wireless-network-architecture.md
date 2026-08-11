# Hazardous-Area Wireless Network Architecture for Industrial Sites

A hazardous-area wireless network should separate four decisions: safety qualification, field connectivity, transport, and OT-system integration. An access point provides local WiFi, a wireless bridge extends Ethernet between locations, a cellular router supplies IP backhaul, and a DTU carries focused telemetry. No single device replaces site classification, RF engineering, security design, or exact-certificate review.

## Functional Architecture

```text
Field clients and sensors
        |
Explosion-proof AP / client / DTU
        |
Ethernet, fiber, wireless bridge, or cellular transport
        |
Industrial switch and security boundary
        |
SCADA, historian, NMS, or cloud monitoring
```

The physical design may include separate safety zones, fiber isolation, redundant rings, point-to-point bridges, private cellular service, and segmented WLANs. Assign an owner and acceptance test to every boundary.

## Design Sequence

1. Obtain the site dossier: Zone or Division, gas or dust group, temperature requirement, equipment protection level, ambient range, certification scheme, and environmental conditions.
2. Identify each field function: worker WiFi, fixed camera, PLC/RTU data, remote telemetry, mobile equipment, or site-to-site backhaul.
3. Select the transport medium based on consequence, availability, capacity, distance, installation cost, and lifecycle.
4. Define VLANs, routing, firewall policy, identity, management access, logging, time synchronization, configuration backup, and update control.
5. Perform predictive RF design and an on-site survey using representative clients and traffic.
6. Verify failover, recovery, alarm handling, and maintenance access before acceptance.

## Device Roles

| Device | Primary function | Key design question |
| --- | --- | --- |
| Explosion-proof AP | Local WLAN coverage | Which clients, bands, roaming, and airtime load? |
| Explosion-proof bridge | Point-to-point or point-to-multipoint Ethernet | Is the path clear and is fade margin adequate? |
| 4G/5G router | Routed cellular IP connectivity | Which carrier, bands, VPN, firewall, and failover? |
| DTU | Focused serial or telemetry transport | Which protocol, payload, polling, and reconnect behavior? |

Fibre may be preferable for high-criticality or high-capacity paths. A wireless bridge can be useful where trenching is difficult or as a diverse backup. WiFi and 5G address different client and backhaul needs; compare device ecosystems, coverage, spectrum, latency, security, and operator dependence.

## Source and Contact

- Canonical article: [Hazardous-Area Wireless Network Architecture for Industrial Sites](https://www.mxcomm.cn/support/technical-share/4006.html)
- MAXON: [https://www.mxcomm.cn](https://www.mxcomm.cn)
- Architecture review: [info@maxonc.com](mailto:info@maxonc.com)

