# Industrial Wireless Access Points: How They Work and How to Select One

An industrial wireless access point connects permitted Wi-Fi clients to a wired network in factories and other operational environments. Selecting one requires matching client and application requirements with the installation environment, radio coverage, power, interfaces, security and management.

This MAXON technical guide covers AP operation, network roles, selection criteria and selected MAXON models.

Original page: https://www.mxcomm.cn/support/technical-share/4011.html

## How an industrial AP works

An AP advertises one or more service set identifiers (SSIDs), supports client authentication and association, manages radio access, and forwards traffic between wireless clients and the wired distribution network.

In 802.11 infrastructure mode, stations associate with an AP. Multiple AP cells can connect through a distribution system to serve a larger site. A compatible wireless controller may provide centralized configuration and monitoring where supported.

### Example OT network architecture

```text
Wi-Fi-capable HMIs, cameras, AGVs and handheld terminals
                         |
                        Wi-Fi
                         |
                         v
                  Industrial AP
                         |
                  Wired connection
                         |
                         v
             Ethernet / fiber-backed switches
                         |
              Network access policies
                         |
                         v
       Controllers / SCADA / historians / monitoring

Wired PLC or machine --> Wireless client device
                                  |
                                 Wi-Fi
                                  |
                                  v
                           Industrial AP
```

A PLC should not be assumed to have a native Wi-Fi interface. A wired machine may require a separate device operating in client mode.

VLANs and access policies can separate OT equipment, maintenance access, video and corporate traffic. Verify the required capabilities across the selected APs, switches and other network equipment.

Client association and roaming depend on the actual client hardware and configuration. Physical proximity alone does not determine which AP a terminal uses or whether a handoff meets application requirements.

## Industrial AP versus office AP

The practical distinction is the documented operating and installation envelope. Industrial deployments may involve dust, water exposure, temperature changes, vibration, electrical transients, outdoor mounting or specialized power arrangements.

| Selection area | Typical office consideration | Industrial engineering check |
| --- | --- | --- |
| Environment | Indoor coverage and placement | Enclosure, temperature, exposure and mounting limits |
| Power | Availability of PoE | Required PoE standard, supply budget and installed cabling |
| Interfaces | Required Ethernet speed | WAN/LAN speeds, connectors, surge protection and any fiber interface |
| Antennas | Internal or external antennas | Pattern, mounting position, obstructions and client radio capability |
| Mobility | Movement between rooms | Application continuity along vehicle and terminal handoff paths |
| Management | Local or cloud management | Compatibility with OT policy, controllers and operational tools |
| Security | Required wireless security mode | Authentication, segmentation, credentials, logging and firmware maintenance |
| Compliance | Market approval | Permitted radio, antenna, frequency, power and installation configuration |

IP68 addresses ingress protection under defined test conditions. It does not establish chemical resistance, hazardous-location approval, vibration tolerance or complete suitability for an industrial installation.

## Operating modes

Operating modes describe different network roles. Availability depends on the exact model and firmware.

| Role | Function | Selection check |
| --- | --- | --- |
| Access point mode | Connects wireless clients to the wired LAN | Client compatibility, security and capacity under the intended traffic load |
| Client mode | Connects a wired machine or device segment to an existing WLAN | Downstream device support, forwarding behavior and upstream AP compatibility |
| Wireless bridge mode | Links Ethernet segments across a wireless path | Supported point-to-point or point-to-multipoint topology, antennas and link requirements |
| Router mode | Routes traffic between IP networks | Required Layer 3 functions and interfaces |
| Controller-managed AP | Receives configuration and monitoring through a compatible controller | Controller compatibility and behavior during loss of management connectivity |

Routing is not inherent to every AP. Some devices also offer repeater operation; confirm the implementation before selecting a device for that role.

## Wi-Fi generation and radio configuration

### Wi-Fi 5 and Wi-Fi 6

Wi-Fi 5 can remain appropriate for established 802.11ac client fleets and moderate throughput requirements. Wi-Fi 6 introduces mechanisms such as OFDMA that can improve airtime use with compatible clients and suitable conditions.

Select around the client fleet, traffic demand, interference, channel plan and equipment lifecycle. A listed peak PHY rate is a physical-layer figure, not measured application throughput or a reliability guarantee.

### Frequency bands

- **2.4 GHz:** Can provide useful reach and legacy compatibility, but has fewer non-overlapping channels and often faces substantial interference.
- **5 GHz:** Offers more channel-planning flexibility; propagation and available channels depend on deployment conditions and location.
- **Tri-band:** Does not automatically mean 6 GHz support. It may describe 2.4 GHz plus two 5 GHz radios, or a combination including 6 GHz.

Verify the frequency table and radio configuration. For proposed 6 GHz operation, obtain the applicable target-market requirements for device class, power, channels, antennas and any coordination obligations.

## Antennas and coverage

Match the antenna pattern to the physical RF path. Omnidirectional antennas can suit local coverage zones. Directional antennas focus energy toward a corridor, yard, remote structure or bridge endpoint.

Evaluate antenna gain, mounting height, cable loss, transmit power, client capability and applicable EIRP limits. Metal racks, machinery, moving vehicles, walls and stored goods can change the usable path.

Use an RF survey and link budget for the proposed antenna and power configuration. Include cell boundaries, channel reuse, interference and movement through coverage areas. A published distance cannot establish coverage for a different installation.

## Security and management

WLAN security requires coordination across clients, access points, switches and management systems. Confirm:

- Authentication and WPA options supported by the actual client fleet.
- Credential lifecycle and management access controls.
- VLAN configuration and the access policies governing traffic between segments.
- Logging, monitoring and firmware update procedures.
- Required standalone web, SNMP or controller interfaces.
- Controller compatibility and recovery behavior where applicable.

Continue firmware maintenance and lifecycle monitoring after commissioning. Do not assume identical security or management features across a product family.

## Selection checklist

Connect each requirement to a documented specification or a planned acceptance test.

- [ ] Record indoor or outdoor location, ingress exposure, heating, condensation, corrosion, vibration and mounting requirements.
- [ ] Inventory client Wi-Fi generations, bands, antennas, security support and roaming behavior.
- [ ] Define concurrent connections, traffic types, upstream demand and application latency requirements.
- [ ] Plan coverage cells, interference assessment, channel reuse, antenna placement and link margin.
- [ ] Check WAN/LAN speeds, copper or fiber interfaces, PoE standard or DC input, cable distance and surge protection.
- [ ] Confirm management interfaces, authentication, logs and update procedures.
- [ ] Define recovery requirements, redundancy, any required watchdog function and spare strategy.
- [ ] Obtain current datasheets, hardware and firmware versions, regulatory documents, relevant test reports and the approved bill of materials.

## Selected MAXON models

> 资料说明：以下型号参数来自所供已批准稿；WAN/LAN速率及PoE标准采用用户明确修正，未独立核验。选型前仍需核对当前数据表及硬件、固件版本。接入数量和PHY速率不代表实际业务性能。

### Radio, interfaces and power

| Model | Supplied radio configuration | Listed maximum PHY rate | Interfaces and power |
| --- | --- | --- | --- |
| [MX6022A-MI6](https://www.mxcomm.cn/products/industrial-wireless/industrial-wireless-access-point/3908.html) | Wi-Fi 6; dual-band; 2×2 MIMO | 1773.5 Mbps | 2.5 Gbps WAN and LAN; 802.3bt PoE++ |
| [MX6023A-ME8](https://www.mxcomm.cn/products/industrial-wireless/industrial-wireless-access-point/3854.html) | Wi-Fi 6; tri-band; 2×2 and 4×4 MIMO listed | 6573.5 Mbps aggregate | 2.5 Gbps WAN and LAN; 802.3bt PoE++ |
| [MD5012A-ME5](https://www.mxcomm.cn/products/industrial-wireless/industrial-wireless-access-point/3881.html) | Wi-Fi 5; dual-band; 2×2 MIMO | 1167 Mbps | 1 Gbps WAN and LAN; 802.3at PoE+ |
| [MX5012A-MI6](https://www.mxcomm.cn/products/industrial-wireless/industrial-wireless-access-point/3853.html) | Wi-Fi 5; dual-band; 2×2 MIMO | 1167 Mbps | 1 Gbps WAN and LAN; 802.3at PoE+ |

### Other listed features and documentation checks

| Model | Features listed in the supplied draft | Confirm before selection |
| --- | --- | --- |
| MX6022A-MI6 | Built-in 6 dBi omnidirectional antenna; IP68; −40 to 70°C; AP and client modes | Environmental rating conditions and required power budget |
| MX6023A-ME8 | IP68; point-to-point and point-to-multipoint relay bridge functions | Frequency allocation, MIMO by radio, antennas, temperature range and power budget |
| MD5012A-ME5 | AP and client modes; fat and fit AP support; up to 128 accesses listed | Management compatibility, access-limit definition, antennas and environmental ratings |
| MX5012A-MI6 | SFP interface listed in the source article; IP68; bridge and routing modes | SFP availability and compatibility, antennas, temperature range and firmware mode support |

The specified PoE standard does not establish power consumption, PoE class or the required supply budget. Obtain those details for the exact model and installation.

Aggregate radio rates do not represent throughput available to a single client. The MD5012A-ME5 access figure also does not establish capacity for 128 simultaneously active devices under a particular workload.

> 待核实事项：所供原文指出MX6023A-MI6存在相互冲突的射频描述和峰值速率，因此未纳入比较。原文将MX6522A-ME8描述为5G路由CPE，本指南也未将其列为常规工业AP。MX5012A-MI6的SFP信息保留为来源列示项，实际配置需进一步确认。

## Deployment validation

Validate the installed network using representative clients and applications under normal operating conditions.

| Validation area | What to evaluate |
| --- | --- |
| RF conditions | Coverage, signal quality and interference while machinery, vehicles and normal traffic are active |
| Application traffic | Latency, packet loss, sustained traffic and congestion behavior with the intended workload |
| Mobility | Planned handoff paths using actual AGV, mobile robot and handheld radios and applications |
| Recovery | Client reconnection and controller failover where applicable |
| Power and installation | Power delivery, mounting, cabling and exposure within documented limits |
| Operations | Management visibility and monitoring integration |

These are proposed checks, not reported test results. Acceptance criteria should come from the site's application requirements.

Control or safety-related systems require the site's formal engineering and risk process. Deterministic operation, fail-safe behavior and suitability for a safety function require system-level evidence and any necessary approvals.

## Frequently asked questions

### How does an AP differ from a wireless router?

An AP primarily connects Wi-Fi clients to a wired LAN. A wireless router forwards traffic between IP networks and may also provide WAN, firewall, NAT and AP functions. Verify the exact model's interfaces and operating modes.

### Can an industrial wireless access point serve as a bridge?

Some models support wireless bridge mode. Confirm the topology and firmware support, then evaluate antennas, line of sight, link budget, channels, traffic requirements and regional radio limits.

### How many clients can an industrial WiFi access point support?

Capacity depends on the model, workload and RF conditions. Request both the maximum association value and performance evidence for comparable traffic, bands, channel widths and client behavior.

### Is IP68 sufficient for every industrial installation?

No. Corrosion, chemicals, vibration, sunlight exposure, hazardous locations and mounting conditions need separate consideration and supporting documentation.

### Should an existing installation move from Wi-Fi 5 to Wi-Fi 6?

Assess client compatibility, traffic density, lifecycle and validated application performance. Wi-Fi 6 can provide efficiency benefits with compatible clients; Wi-Fi 5 may remain suitable for established equipment. Both require a site-specific radio plan.

## MAXON resources and contact

For product selection, prepare the installation environment, client list, traffic requirements, coverage map, mobility routes, power supply, uplink interfaces, management requirements and target deployment market.

- [Original technical article](https://www.mxcomm.cn/support/technical-share/4011.html)
- [MAXON industrial wireless access point portfolio](https://www.mxcomm.cn/products/industrial-wireless/industrial-wireless-access-point.html)
- Website: https://www.mxcomm.cn
- Email: [info@maxonc.com](mailto:info@maxonc.com)
