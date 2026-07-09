# NN-2026:6-01 - HTML injection in Schedule Restore Archive in Guardian/CMC before 26.1.0

**Source**: [Nozomi Networks Security Bulletin](https://security.nozominetworks.com/NN-2026:6-01/)
**CSAF**: [Link](https://security.nozominetworks.com/csaf/2026/nn-2026_6-01.json)
**Advisory ID**: NN-2026:6-01
**Issue Date**: 2026-05-19

---

## Overview
A **Stored HTML Injection** vulnerability was discovered in the **Schedule Restore Archive functionality** of **Guardian/CMC** versions before **v26.1.0**. This vulnerability arises due to **improper validation of an input parameter**, allowing an authenticated user with **administrative privileges** to define a malicious restore schedule containing **HTML tags**. When a victim views the affected schedule, the injected HTML renders in their browser, enabling **phishing** and **open redirect attacks**.

---

## Key Details
| Attribute | Value |
| --- | --- |
| **CWE Impact** | [CWE-79]([[CWE-79]]) - Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting') |
| **Affected Products** | Guardian, CMC < v26.1.0 |
| **CVE Name** | [CVE-2025-40903](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2025-40903) |
| **CVSS Score** | 4.8 (CVSS v4.0), 5.9 (CVSS v3.1) |
| **Risk Level** | Medium (CVSS v4.0), Medium (CVSS v3.1) |
| **CVSS Vector (v4.0)** | CVSS:4.0/AV:N/AC:L/AT:N/PR:H/UI:P/VC:L/VI:L/VA:L/SC:L/SI:L/SA:L |
| **CVSS Vector (v3.1)** | CVSS:3.1/AV:N/AC:L/PR:H/UI:R/S:C/C:L/I:L/A:L |

---

## Impact
- An authenticated user with **administrative privileges** can define a malicious restore schedule containing HTML tags.
- When a victim **views the affected schedule**, the injected HTML renders in their browser.
- This enables **phishing** and **open redirect attacks**.
- **Full XSS exploitation** and **direct information disclosure** are prevented by existing input validation and **Content Security Policy (CSP)** configuration.

---

## Affected Products
- **Guardian** (versions before v26.1.0)
- **CMC** (versions before v26.1.0)

---

## Solutions
- **Upgrade** to **v26.1.0** or later to mitigate the vulnerability.

---

## Workarounds and Mitigations
- Use **internal firewall features** to limit access to the web management interface.
- **Review all accounts** with administrative access and delete unnecessary ones.

---

## Related Concepts
- [[HTML Injection]]
- [[CWE-79]]
- [[Guardian/CMC]]
- [[Nozomi Networks]]

---

## Modification History
- **2026-05-19**: Initial revision

---

## Related Links
- [Mitre CVE Entry](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2025-40903)

---

## Acknowledgements
- **Stefano Libero** and **Andrea Palanca** of the [Nozomi Networks Product Security Team]([[Nozomi Networks Product Security Team]]) for discovering this issue during an internal investigation.

---

## Contact
- **Nozomi Networks Product Security Team**: [prodsec@nozominetworks.com](mailto:prodsec@nozominetworks.com)
- **PSIRT Page**: [Nozomi Networks PSIRT](https://security.nozominetworks.com/psirt/)