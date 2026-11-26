# DBDC or Single-band WiFi: An Industrial Gateway Decision Checklist

The [MAXON article](https://www.mxcomm.cn/support/technical-share/4035.html) explains the engineering context for this checklist.

Start by writing down which wireless roles must run at the same time. A list of supported frequency bands does not describe concurrent behavior.

## Distinguish the architectures

| Architecture | What to verify |
|---|---|
| Single-band | The one operating band and its supported roles |
| Selectable dual-band | Which band can be selected and whether switching interrupts service |
| DBDC | The exact pair of bands that can operate concurrently |
| Tri-band-capable design | Both the supported bands and the number/pairs that may be active together |

DBDC means dual-band dual-concurrent. It describes concurrent operation; it is not a guarantee of doubled application throughput or automatic failover.

## Map the network roles

Write a role map before requesting a model:

| Project role | Required information |
|---|---|
| Local client access | Band, AP role, client population and application traffic |
| Wireless backhaul | Band, station/other supported role, peer and traffic direction |
| Concurrent operation | Which roles and band pairs must work at the same time |
| Host forwarding | Interface, CPU capacity and routing/bridging arrangement |
| Field deployment | Country, antennas, enclosure and environmental requirements |

A gateway serving one group on 2.4 GHz while maintaining another link on 5 GHz is a candidate for concurrent operation. The selected hardware and software must explicitly support the requested role combination.

## Check the integration costs

- [ ] Obtain the simultaneous band pairs for the exact module revision.
- [ ] Verify radio-chain and antenna-port allocation.
- [ ] Evaluate antenna isolation and filtering with both radios active.
- [ ] Test host interface and packet-processing capacity.
- [ ] Measure power and thermal behavior under concurrent traffic.
- [ ] Confirm driver, firmware and interface-combination support.
- [ ] Validate the target country's permitted radio configuration.

Testing one radio at a time can miss interaction between the active transmit and receive paths. Retain simultaneous-load results in addition to single-radio measurements.

## When single-band deserves comparison

A product using one planned band may not need the integration work of concurrent radios. Compare the available single-band design when antenna space, power, cooling or software complexity is constrained.

This is a design comparison, not a claim that every single-band module consumes less power than every DBDC module. Use exact-model data and the intended workload.

## Validate the intended benefit

Measure end-to-end application performance with the required roles active. Record peer devices, traffic direction, host load, channel conditions and recovery behavior. Do not add two PHY rates together and present the result as measured throughput.

For MAXON module selection, provide the required band pairs, concurrent AP/station roles, traffic, antenna plan, host interface and enclosure constraints. Ask for confirmation of the exact supported configuration before selecting a model.

## Module selection and support

Review the [MAXON industrial WiFi module range](https://www.mxcomm.cn/products/industrial-wireless/wifi-module.html) for your project, then request the documents for the exact model and revision. Visit [MAXON](https://www.mxcomm.cn) or contact info@maxonc.com.
