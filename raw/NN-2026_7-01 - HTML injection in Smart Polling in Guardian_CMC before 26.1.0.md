---
title: "NN-2026:7-01 - HTML injection in Smart Polling in Guardian/CMC before 26.1.0"
source: "https://security.nozominetworks.com/NN-2026:7-01/"
author:
published:
created: 2026-06-08
description: "Nozomi Networks incident response portal contains security bulletins about Nozomi Networks products."
tags:
  - "clippings"
---
[

![](https://security.nozominetworks.com/static/489ee5c405a5e6d55699eb112eefe7ae/a1c7a/logo-psirt.webp)

](https://security.nozominetworks.com/)

## HTML injection in Smart Polling in Guardian/CMC before 26.1.0

[CSAF](https://security.nozominetworks.com/csaf/2026/nn-2026_7-01.json)

| Advisory ID | NN-2026:7-01 |
| --- | --- |
| Topic | HTML injection in Smart Polling in Guardian/CMC before 26.1.0 |
| CWE Impact | CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting') |
| Issue date | 2026-05-19 |
| Affects | Guardian, CMC < v26.1.0 |
| CVE Name(s) | CVE-2025-40904 |
| CVSS Details | CVSS:4.0/AV:N/AC:L/AT:N/PR:L/UI:P/VC:L/VI:L/VA:L/SC:L/SI:L/SA:L   CVSS:3.1/AV:N/AC:L/PR:L/UI:R/S:C/C:L/I:L/A:L |
| CVSS Score | 5.1 (CVSS v4.0)   6.5 (CVSS v3.1) |
| CVE Risk Level | Medium (CVSS v4.0)   Medium (CVSS v3.1) |
| Risk Level for Nozomi customers | Medium |

## Summary

A Stored HTML Injection vulnerability was discovered in the Smart Polling functionality due to improper validation of an input parameter.

## Impact

An authenticated user with limited privileges can push malicious remote strategies containing HTML tags through the sync. When a victim views the affected remote strategy in the Smart Polling functionality, the injected HTML renders in their browser, enabling phishing and possibly open redirect attacks. Full XSS exploitation and direct information disclosure are prevented by the existing input validation and Content Security Policy configuration.

## Affected Products

Guardian, CMC < v26.1.0

## Workarounds and Mitigations

Review all enabled sensors and disallow or delete untrusted ones.

## Solutions

Upgrade to v26.1.0 or later.

## Modification History

2026-05-19: Initial revision

## Related Links

[Mitre CVE entry](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2025-40904)

## Acknowledgements

We thank the following parties for their efforts:

- Stefano Libero, Andrea Palanca of Nozomi Networks Product Security team for finding this issue during an internal investigation

#### Contact

Nozomi Networks Product Security team can be reached at [prodsec@nozominetworks.com](mailto:prodsec@nozominetworks.com).  
More contact details on the [PSIRT page](https://security.nozominetworks.com/psirt/).

Navigated to HTML injection in Smart Polling in Guardian/CMC before 26.1.0