---
title: "NN-2019:1-01 - Stored XSS in field name data model"
source: "https://security.nozominetworks.com/NN-2019:1-01/"
author:
published:
created: 2026-06-10
description: "Nozomi Networks incident response portal contains security bulletins about Nozomi Networks products."
tags:
  - "clippings"
---
[

![](https://security.nozominetworks.com/static/489ee5c405a5e6d55699eb112eefe7ae/a1c7a/logo-psirt.webp)

](https://security.nozominetworks.com/)

## Stored XSS in field name data model

[CSAF](https://security.nozominetworks.com/csaf/2019/nn-2019_1-01.json)

| Advisory ID | NN-2019:1-01 |
| --- | --- |
| Topic | Stored XSS in field name data model |
| CWE Impact | CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting') |
| Issue date | 2019-11-11 |
| Affects | Guardian, CMC < v19.0.4 |
| CVE Name(s) | NA |
| CVSS Details | CVSS:4.0/AV:N/AC:L/AT:N/PR:H/UI:P/VC:H/VI:L/VA:N/SC:N/SI:N/SA:N   CVSS:3.1/AV:N/AC:L/PR:H/UI:N/S:C/C:H/I:L/A:N |
| CVSS Score | 6.9 (CVSS v4.0)   7.6 (CVSS v3.1) |
| CVE Risk Level | Medium (CVSS v4.0)   High (CVSS v3.1) |
| Risk Level for Nozomi customers | Medium |

## Summary

An attacker with admin access to the appliance can inject malicious code that will later be executed by another legitimate users. This allows an attacker to perform unauthorized actions on behalf of legitimate users. JavaScript injection was possible using the field name when adding new column to the data model section. The injected code will then be executed in the environment section under e.g. asset view.

## Impact

Guardian/CMC starting before v19.0.4 are affected.

## Affected Products

Guardian, CMC < v19.0.4

## Workarounds and Mitigations

Not required

## Solutions

Upgrade to v19.0.4

## Modification History

2019-11-11: Initial revision

2023-09-04: Minor updates to format and metadata to improve the CSAF implementation

2023-11-13: Migrated to CSAF VEX format

2023-11-16: CSAF vers improvements

2024-05-20: Added CVSS v4.0 scoring where applicable

## Related Links

## Acknowledgements

We thank the following parties for their efforts:

- Jonas Becker of Deloitte GmbH for finding this bug

#### Contact

Nozomi Networks Product Security team can be reached at [prodsec@nozominetworks.com](mailto:prodsec@nozominetworks.com).  
More contact details on the [PSIRT page](https://security.nozominetworks.com/psirt/).

Navigated to Stored XSS in field name data model