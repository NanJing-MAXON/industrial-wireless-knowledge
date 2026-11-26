# Industrial WiFi Module Bring-up: A Linux and OpenWrt Checklist

The [MAXON article](https://www.mxcomm.cn/support/technical-share/4031.html) explains the engineering context for this checklist.

Use this checklist to identify the first failing layer in an embedded WiFi integration. Keep the module revision and software image fixed while collecting evidence. Change one variable at a time.

## Record the configuration

- [ ] Exact module model, hardware revision and PCIe device ID
- [ ] Host CPU, carrier-board revision and power/reset arrangement
- [ ] OS release, kernel, OpenWrt target or vendor SDK revision
- [ ] Driver, firmware and board-data versions
- [ ] Required AP/station roles, bands and target deployment country
- [ ] Antenna-port mapping and final enclosure configuration

A chipset family name or a connector match does not establish support for this complete combination.

## Follow the first failing layer

| Observation | Next check | Evidence to retain |
|---|---|---|
| Device absent from PCIe | Power, reset, clock, lane mapping and host controller | Full boot log and hardware measurements |
| Device present, no driver bound | Device ID support and kernel configuration | PCIe ID, driver version and probe messages |
| Driver probes, firmware fails | Requested filenames and compatible software package | Exact error and installed file versions |
| Radio initialization fails | Hardware-specific board data and calibration requirements | Board revision and requested board-data ID |
| Radio exists, service fails | Supported interface combinations and userspace settings | Interface list and AP/station service log |
| Link works, application fails | Traffic, host load, recovery and network configuration | Repeatable workload and time-aligned logs |

## Collect read-only diagnostics

Run only the commands available on your target image. Some embedded images do not include pciutils or iw; missing tools do not prove a hardware fault.

```sh
uname -a
lspci -nnk
dmesg
lsmod
ip link
iw dev
iw phy
# OpenWrt system log, when available:
logread
```

Retain the full boot sequence. A final interface error can be a consequence of an earlier firmware or board-data failure. Remove passwords, tokens and other sensitive information before sharing logs.

## Control the OpenWrt build

Treat the OpenWrt release, kernel ABI, target architecture, driver package, firmware and board data as one tested configuration. Record vendor SDK changes separately. Do not install a package from a similar-looking release and assume it matches the running kernel.

Use the module supplier's supported package for the exact hardware revision. Do not copy calibration or board data from an unrelated module, or force channels that the intended configuration does not support.

## Validate the product after bring-up

- [ ] Exercise the AP or station modes the product actually needs.
- [ ] Test sustained traffic in both directions and required client loads.
- [ ] Check reboot, link loss, radio reset and image-upgrade recovery.
- [ ] Confirm country configuration, permitted bands and channel widths.
- [ ] Repeat relevant tests in the final enclosure and operating environment.

For a MAXON compatibility review, provide the module revision, host CPU, kernel or SDK, required modes, target countries and complete boot log. The checklist is an integration aid, not a declaration that every MAXON module supports every Linux or OpenWrt release.

## Module selection and support

Review the [MAXON industrial WiFi module range](https://www.mxcomm.cn/products/industrial-wireless/wifi-module.html) for your project, then request the documents for the exact model and revision. Visit [MAXON](https://www.mxcomm.cn) or contact info@maxonc.com.
