# Intrinsically Safe WiFi Board vs Explosion-Proof Wireless Equipment

An intrinsically safe WiFi board and a complete explosion-proof wireless device solve different engineering problems. Intrinsic safety limits electrical and thermal energy under defined normal and fault conditions. Flameproof equipment contains a possible internal ignition within an engineered enclosure. A board approval does not automatically certify the finished tablet, terminal, gateway, or IIoT device.

## When to Use Each Approach

| Requirement | Intrinsically safe WiFi board | Complete explosion-proof device |
| --- | --- | --- |
| Typical role | Component inside an OEM terminal, tablet, or gateway | Field AP, bridge, router, or DTU |
| Design boundary | Board, host, power, interfaces, antenna, and enclosure | Defined certified assembly and approved accessories |
| OEM flexibility | High, within controlled design limits | Deployed in its approved configuration |
| Main responsibility | System integration, evidence, and final certification | Correct selection, installation, and maintenance |

A board-level design is suitable when the OEM controls the complete hardware and can manage RF testing, thermal validation, software support, production change control, and system certification. If the project only needs plant WiFi coverage, an approved complete access point is usually the clearer network element.

## OEM Integration Checklist

- Define the destination country, certification scheme, Zone or Division, gas or dust group, temperature requirement, equipment protection level, and ambient range.
- Specify supply voltage, peak current, fault-energy limits, isolation, grounding, battery protection, and external interfaces.
- Define WiFi generation, bands, AP or client mode, antenna type and gain, enclosure material, cable path, regulatory domain, and radio coexistence.
- Confirm the host processor, operating system, kernel or SDK, driver ownership, update method, credential storage, calibration, and vulnerability-management plan.
- Prototype the production enclosure and test radiated performance, receiver behavior, coexistence, and temperature under representative traffic and fault conditions.
- Obtain the exact certificate, schedule, controlled drawings, permitted interfaces, approved RF arrangement, integration instructions, and change-notification process.

Do not assume simultaneous AP/client, repeater, mesh, or roaming support unless the exact hardware and software documents confirm it. Do not infer the finished device's temperature class from a board operating-temperature specification.

## Source and Contact

- Canonical article: [Intrinsically Safe WiFi Board vs Explosion-Proof Wireless Equipment](https://www.mxcomm.cn/support/technical-share/4008.html)
- MAXON: [https://www.mxcomm.cn](https://www.mxcomm.cn)
- Engineering inquiries: [info@maxonc.com](mailto:info@maxonc.com)

