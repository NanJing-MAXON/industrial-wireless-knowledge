# Explosion-Proof Wireless Bridge Design for Long-Range Industrial Links

A long-range explosion-proof wireless bridge must pass both hazardous-area and RF-link reviews. Distance alone cannot approve the link. The same bridge can behave very differently across an open pipeline corridor and a dense refinery because terrain, structures, interference, antenna placement, weather, and maintenance conditions change the link budget.

## Point-to-Point Link Record

For each link, document:

- path profile and antenna heights;
- line of sight and Fresnel-zone clearance;
- frequency, channel width, and channel plan;
- transmit power, cable loss, connector loss, and antenna gain;
- regional EIRP limit;
- receiver sensitivity at the intended modulation;
- calculated receive level and fade margin;
- rain, heat, seasonal, and vegetation conditions;
- interference sources and spectrum observations;
- alignment method, mounting strength, and maintenance access.

## Basic Link-Budget Relationship

```text
Received power = transmit power
               + transmit antenna gain
               - transmit-side losses
               - path loss
               + receive antenna gain
               - receive-side losses

Fade margin = received power - receiver sensitivity
```

Use values for the exact band, channel width, modulation, antenna, cable, and regulatory domain. Do not use a chipset theoretical maximum as installed product performance.

## Deployment Workflow

1. Confirm the exact bridge model and installed accessories against the hazardous-area certificate.
2. Survey both endpoints and the complete path, including future construction and vegetation.
3. Select antenna height and directivity to maintain clearance and reject interference.
4. Calculate the link at the required modulation, not only at the most robust low-rate mode.
5. Verify EIRP and permitted channels for the installation country.
6. Align with measured receive level and record final azimuth, elevation, mounting, and readings.
7. Test application throughput, latency, packet loss, failover, and recovery under representative load.
8. Define periodic inspection for alignment, fasteners, seals, entries, corrosion, cables, and enclosure condition.

For critical or high-capacity routes, compare the bridge with fiber and consider redundancy. Point-to-multipoint systems require an airtime and hidden-node review in addition to individual path calculations.

## Source and Contact

- Canonical article: [Explosion-Proof Wireless Bridge Design for Long-Range Industrial Links](https://www.mxcomm.cn/support/technical-share/4003.html)
- MAXON: [https://www.mxcomm.cn](https://www.mxcomm.cn)
- Link-design support: [info@maxonc.com](mailto:info@maxonc.com)

