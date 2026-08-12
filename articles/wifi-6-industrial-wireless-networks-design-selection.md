# WiFi 6 for Industrial Wireless Networks: Design and Product Selection

WiFi 6 is the Wi-Fi Alliance name for IEEE 802.11ax. Its main industrial value is more efficient airtime use when many active devices share the same channels. PLC messages, operator tablets, cameras, sensors, AGVs, and robots may all compete for airtime in one factory network.

WiFi 6 gives the access point better scheduling tools. It does not remove interference, poor antenna placement, insufficient backhaul, or roaming delays.

## How WiFi 6 Changes Radio Operation

### OFDMA

Orthogonal Frequency Division Multiple Access divides a channel into resource units that an access point can assign to different clients during the same transmission opportunity. This can help when many terminals exchange short, frequent packets. The benefit depends on access-point scheduling, client support, and traffic patterns.

### Uplink and Downlink MU-MIMO

Multi-User MIMO allows a compatible access point to communicate with multiple clients through separate spatial streams. WiFi 6 supports multi-user operation in both directions. Clients still share spectrum, and performance depends on the RF environment, antenna system, peer capability, and scheduler.

### BSS Coloring

BSS Coloring marks frames from different basic service sets. Compatible devices can distinguish their own network from overlapping networks and make better spatial-reuse decisions. It cannot correct excessive co-channel energy or poorly defined cell boundaries.

### Target Wake Time

Target Wake Time allows compatible clients to negotiate scheduled wake periods. It can reduce radio-on time for battery-powered devices, but battery life still depends on firmware, retries, traffic, and the application cycle.

### 1024-QAM

WiFi 6 supports 1024-QAM under suitable signal conditions. Near the edge of a cell, the client normally falls back to a lower modulation and coding scheme. Maximum PHY rate is therefore neither a coverage figure nor an application-throughput guarantee.

## WiFi 5 and WiFi 6 in Industrial Networks

| Engineering factor | WiFi 5 (802.11ac) | WiFi 6 (802.11ax) |
| --- | --- | --- |
| Main standard-level bands | 5 GHz; some MAXON platforms use separate 2.4 and 5 GHz radios | 2.4 GHz and 5 GHz; 6 GHz is available through WiFi 6E products |
| Multi-user access | Downlink MU-MIMO on supported systems | Uplink and downlink MU-MIMO plus OFDMA |
| Highest standard modulation | 256-QAM | 1024-QAM |
| Dense-network mechanisms | Conventional contention and channel planning | OFDMA, BSS Coloring, and improved multi-user scheduling |
| Typical decision | Proven platforms and moderate workloads | New dense or capacity-sensitive deployments |

A validated WiFi 5 link may remain the lower-risk option for modest telemetry. WiFi 6 becomes more useful as the number of active clients, bidirectional traffic, or airtime contention increases.

## Application Design Rules

- AGVs and AMRs require planned cell overlap, verified client roaming behavior, and packet-loss testing during handoff.
- Cameras require measured uplink capacity under concurrent load.
- PLC and sensor traffic requires latency, jitter, and packet-delivery tests during the busiest operating period.
- Outdoor bridges require line of sight, Fresnel-zone clearance, a link budget, and a channel plan.
- Hazardous areas require the correct protection method, exact-model documentation, and approved installation accessories.

The radio generation is only one part of the system. Topology, antennas, channel reuse, wired uplinks, power, security, and commissioning determine the finished network.

## MAXON WiFi 6 Product Starting Points

### Access Points

The current MAXON industrial wireless range includes WiFi 6 access points for factory, outdoor, and mobile-equipment networks. MX6022 and MX6023 series models are candidates for general industrial coverage. Select the exact suffix because frequency, interfaces, and enclosure details vary.

For hazardous locations, the MX821-1F is listed as a dual-band 802.11ax explosion-proof access point with a maximum aggregate PHY rate of 1773.5 Mbps and AP/Client modes. Verify the site classification, certificate scope, antennas, and accessories before procurement.

### Embedded Modules

| Module | Confirmed radio configuration | Host interface | Initial design use |
| --- | --- | --- | --- |
| ME6922 FD | QCN9024, 2.4/5 GHz DBDC, 2x2 MIMO | Mini PCIe form factor with PCIe 3.0 | Dual-band embedded AP or gateway |
| ME6924 FD | QCN9024, 2.4/5 GHz DBDC, recorded 2x2 MIMO | Mini PCIe form factor with PCIe 3.0 | Dual-band industrial equipment |
| MX6924 F5 | QCN9024, 5 GHz, 4x4 MIMO | M.2 E-key with PCIe 3.0 | 5 GHz high-capacity design |
| MX6974 F5 | QCN9074, 5 GHz, 4x4 MIMO | M.2 E-key with PCIe 3.0 | 5 GHz industrial AP or gateway |

These are hardware starting points. Confirm the exact driver, host CPU, kernel, firmware, power budget, thermal path, antenna layout, regulatory domain, model suffix, and hardware revision.

## Network Qualification Checklist

1. Record associated clients and the number active at peak load.
2. Separate control traffic, video, voice, and bulk data in the capacity model.
3. Define mobility routes, roaming interruption, latency, jitter, and packet-loss limits.
4. Survey 2.4 GHz and 5 GHz noise and existing channel use.
5. Calculate access-point cell size, channel reuse, and wired-uplink capacity.
6. Confirm that the clients support the WiFi 6 functions planned for the network.
7. Test with representative clients during the busiest operating condition.

A bench test with one nearby client verifies basic integration. It does not qualify the production network.

## Source and Contact

- Canonical article: [WiFi 6 for Industrial Wireless Networks: Features, Design Tradeoffs and Product Selection](https://www.mxcomm.cn/support/technical-share/3999.html)
- MAXON: [https://www.mxcomm.cn](https://www.mxcomm.cn)
- Project and module inquiries: [info@maxonc.com](mailto:info@maxonc.com)

