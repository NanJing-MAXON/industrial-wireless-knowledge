# WiFi Module Compliance: An OEM Document-Review Checklist

The [MAXON article](https://www.mxcomm.cn/support/technical-share/4034.html) explains the engineering context for this checklist.

A module's compliance records must be matched to the exact host configuration and target market. This checklist helps organize that review. It is not an authorization to market a product or a substitute for a qualified laboratory's assessment.

## Establish the identity of the module

- [ ] Exact model, suffix and hardware revision
- [ ] Manufacturer and relevant authorization or document identifiers
- [ ] Covered bands and operating modes
- [ ] Document issue dates and current revision
- [ ] OEM integration instructions and available test reports

A document for a related module is not evidence for the part on the bill of materials.

## Compare the module conditions with the host

| Review item | Information to compare |
|---|---|
| Antenna system | Type, gain, cable, connector, installation and separation conditions |
| Radio configuration | Bands, power settings, firmware and country configuration |
| Host assembly | Enclosure, mounting, power arrangement and digital interfaces |
| Other radios | Co-located transmitters and intended simultaneous operation |
| User information | Product label, installation instructions and operating restrictions |
| Traceability | Production revision, software release and change-control record |

Identify any mismatch before committing the enclosure, antenna or labeling design. Give the laboratory the whole configuration, including the radios intended to operate together.

## Keep the evidence categories distinct

FCC radio authorization, EU conformity assessment, Wi-Fi interoperability certification and substance-compliance records address different questions. A RoHS or REACH record is not a radio approval.

For US projects, review the exact authorization and integration conditions. For EU projects, determine the applicable requirements for the finished radio equipment and retain the supporting technical documentation. Do not treat a module-level document as a blanket final-product approval.

The current official starting points are [47 CFR 15.212](https://www.ecfr.gov/current/title-47/chapter-I/subchapter-A/part-15/subpart-C/section-15.212) and the [European Commission's RED guidance](https://single-market-economy.ec.europa.eu/sectors/electrical-and-electronic-engineering-industries-eei/radio-equipment-directive-red_en). These sources do not establish the certification status of any particular MAXON model.

## Control changes after the review

Reopen the review when the project changes antennas, cables, enclosure, co-located radios, power configuration, country settings or firmware behavior relevant to radio operation.

Retain the original condition, the proposed change, the responsible reviewer and the resulting decision. A replacement component that fits mechanically can still alter the evidence required for the final product.

## Prepare a specific document request

Send MAXON the exact candidate module, target countries, product description, antenna configuration, host, other radios and operating modes. Request the current documents that cover that model and revision.

This technical note does not claim that every MAXON module holds FCC authorization, CE documentation or any other certification. Confirm the scope of the selected model's records before copying a statement into an OEM datasheet or sales page.

## Module selection and support

Review the [MAXON industrial WiFi module range](https://www.mxcomm.cn/products/industrial-wireless/wifi-module.html) for your project, then request the documents for the exact model and revision. Visit [MAXON](https://www.mxcomm.cn) or contact info@maxonc.com.
