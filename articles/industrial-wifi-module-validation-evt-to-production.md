# Industrial WiFi Module Validation Matrix: EVT to Production

The [MAXON article](https://www.mxcomm.cn/support/technical-share/4032.html) explains the engineering context for this checklist.

A useful test record connects a requirement to a controlled configuration, a measured result and a release decision. A single "WiFi connected" result cannot serve as the complete validation record.

## Define the configuration before testing

Record the module and carrier-board revisions, host platform, antennas, RF cables, enclosure, driver, firmware and board data. Include the country setting, band, channel width, operating role, peer device and traffic profile.

Set pass criteria before collecting results. Keep the raw logs even when a summary passes.

## Use a different question at each stage

| Stage | Decision | Evidence to collect |
|---|---|---|
| EVT | Can this architecture work? | Enumeration, initialization, early RF checks and representative traffic |
| DVT | Does the production-intent design meet its requirements? | RF, OTA, sustained traffic, environmental and recovery results |
| PVT | Can manufacturing reproduce the validated design? | Fixture repeatability, programming, configuration control and traceability |
| Production screening | Is this unit assembled and configured correctly? | Fast checks for the defects the production process needs to detect |

The project defines the test scope. These stages are a planning structure, not a certificate or a universal set of pass limits.

## Keep RF and system tests separate

Conducted measurements help isolate radio behavior through a defined RF connection. Over-the-air testing includes the antenna, cable routing, enclosure and orientation. A favorable conducted result does not establish the radiated behavior of the finished product.

For application traffic, record protocol, direction, peer, signal conditions, channel width and duration. Measure latency, packet loss and recovery where they matter to the application, not just peak throughput. Retain host CPU load and relevant logs to identify a host or wired-network bottleneck.

## Exercise failures deliberately

- [ ] Interrupt power and record startup recovery.
- [ ] Remove the AP or client connection and measure application recovery.
- [ ] Restart the host and radio separately where supported.
- [ ] Exercise the intended configuration's congested-channel and regulatory events.
- [ ] Check recovery from an invalid configuration without losing the service procedure.
- [ ] Run the required workload long enough to observe thermal and memory behavior.

Plan disruptive testing on a controlled test setup, not a live customer network.

## Suggested result-record fields

| Field group | Retained information |
|---|---|
| Identity | Test ID, owner, requirement and acceptance criterion |
| Configuration | Hardware, software, antennas, enclosure and country setting |
| Method | Instruments, peer, traffic profile, environment and duration |
| Result | Raw logs, measurements, pass/fail decision and observed faults |
| Follow-up | Corrective change, retest reference and release approver |

Production screening should follow the defects and process risks established during validation. It cannot replace design validation merely because it runs on every unit.

For a MAXON sample-validation discussion, share the candidate module, host, software stack, required modes, target bands and acceptance criteria. Request the available model-specific integration and test-mode documentation before committing to fixture design.

## Module selection and support

Review the [MAXON industrial WiFi module range](https://www.mxcomm.cn/products/industrial-wireless/wifi-module.html) for your project, then request the documents for the exact model and revision. Visit [MAXON](https://www.mxcomm.cn) or contact info@maxonc.com.
