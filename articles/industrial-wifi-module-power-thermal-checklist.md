# Industrial WiFi Module Power and Thermal Review Checklist

The [MAXON article](https://www.mxcomm.cn/support/technical-share/4033.html) explains the engineering context for this checklist.

Review the supply path and heat path under the same defined workload. Average current and room-temperature association are incomplete inputs for a production design.

This checklist deliberately contains no universal voltage, current or temperature limit. Obtain those values for the exact module and revision.

## Build the power path from source to module

| Element | Question for the design review |
|---|---|
| Input source | What voltage range and transient conditions must the system tolerate? |
| Converter | Can it supply the required peaks while retaining its own thermal margin? |
| Planes and traces | What drop appears at the module during the intended load? |
| Connector | Are contact resistance, pin current and assembly conditions controlled? |
| Decoupling | Do values, placement and return paths follow the integration guidance? |
| Reset and enable | Do sequencing and timing meet the host and module requirements? |

Measure at the module supply connection, not only at the bench supply. Capture startup, warm reset, repeated reboot and representative transmit/receive activity. Correlate the supply trace with logs so a reset or lost interface has a useful time reference.

## Define the heat path

Document how heat reaches the carrier board, a spreader, surrounding air or the enclosure. Check contact area, tolerances, clearance and mounting pressure.

Do not assume a shield can be used as a heatsink contact. Confirm the permitted mechanical interface with the module documentation. An improvised thermal pad can create electrical or mechanical problems even if the surface feels cooler.

A sealed enclosure's internal temperature can differ from ambient room temperature. Include nearby processors, cellular radios and converters in the test configuration.

## Select application workloads

- [ ] Idle associated, to establish the reference behavior
- [ ] Sustained transmit and sustained receive
- [ ] Bidirectional traffic at required channel widths
- [ ] Required AP client load or gateway packet processing
- [ ] Concurrent radios where the chosen configuration supports and needs them
- [ ] Intended enclosure orientation and operating environment

Use project requirements to choose the duration and acceptance limits. Do not transfer a limit from another module merely because the WiFi generation is the same.

## Keep a synchronized result record

Record supply voltage, current, available temperature sensors, local internal temperature, throughput, packet loss, host load, throttling, resets and recovery. Retain measurement locations and methods.

A design may lose traffic performance before a hard reset occurs. Reviewing logs alongside electrical and thermal measurements helps distinguish a cooling issue from a software or host-capacity limit.

## Information for a MAXON review

Provide the exact module, power schematic, carrier-board layout, enclosure, planned mounting, intended traffic and target internal temperature. Request the current model-specific electrical and mechanical guidance before freezing regulator capacity or the cooling arrangement.

The objective is a reproducible result for the complete product, not a power figure inferred from a WiFi 6 or WiFi 7 label.

## Module selection and support

Review the [MAXON industrial WiFi module range](https://www.mxcomm.cn/products/industrial-wireless/wifi-module.html) for your project, then request the documents for the exact model and revision. Visit [MAXON](https://www.mxcomm.cn) or contact info@maxonc.com.
