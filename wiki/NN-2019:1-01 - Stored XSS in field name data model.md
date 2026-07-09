# NN-2019:1-01 - Stored XSS in field name data model

**Source**: [Nozomi Networks Security Bulletin](https://security.nozominetworks.com/NN-2019:1-01/)
**CSAF**: [Link](https://security.nozominetworks.com/csaf/2019/nn-2019_1-01.json)
**Advisory ID**: NN-2019:1-01
**Issue Date**: 2019-11-11

---

## Overview
A **Stored XSS (Cross-Site Scripting)** vulnerability was discovered in the **field name data model** of **Guardian-CMC** versions before **v19.0.4**. This vulnerability allows an attacker with **admin access** to inject malicious JavaScript code into the field name when adding a new column to the data model section. The injected code is later executed in the environment section (e.g., asset view) by legitimate users, enabling unauthorized actions on their behalf.

---

## Key Details
| Attribute | Value |
| --- | --- |
| **CWE Impact** | [CWE-79]([[CWE-79]]) - Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting') |
| **Affected Products** | Guardian, CMC < v19.0.4 |
| **CVSS Score** | 6.9 (CVSS v4.0), 7.6 (CVSS v3.1) |
| **Risk Level** | Medium (CVSS v4.0), High (CVSS v3.1) |
| **CVSS Vector (v4.0)** | CVSS:4.0/AV:N/AC:L/AT:N/PR:H/UI:P/VC:H/VI:L/VA:N/SC:N/SI:N/SA:N |
| **CVSS Vector (v3.1)** | CVSS:3.1/AV:N/AC:L/PR:H/UI:N/S:C/C:H/I:L/A:N |

---

## Impact
- An attacker with **admin access** can inject malicious JavaScript code.
- The injected code is executed when legitimate users interact with the **environment section** (e.g., asset view).
- This allows the attacker to perform **unauthorized actions** on behalf of legitimate users.

---

## Affected Products
- **Guardian** (versions before v19.0.4)
- **CMC** (versions before v19.0.4)

---

## Solutions
- **Upgrade** to **v19.0.4** or later to mitigate the vulnerability.

---

## Workarounds and Mitigations
- No workarounds are required. Upgrading to the latest version is the recommended solution.

---

## Related Concepts
- [[Stored XSS]]
- [[CWE-79]]
- [[Guardian-CMC]]
- [[Nozomi Networks]]

---

## Modification History
- **2019-11-11**: Initial revision
- **2023-09-04**: Minor updates to format and metadata to improve CSAF implementation
- **2023-11-13**: Migrated to CSAF VEX format
- **2023-11-16**: CSAF version improvements
- **2024-05-20**: Added CVSS v4.0 scoring where applicable

---

## Acknowledgements
- **Jonas Becker** of Deloitte GmbH for discovering and reporting this vulnerability.

---

## Contact
- **Nozomi Networks Product Security Team**: [prodsec@nozominetworks.com](mailto:prodsec@nozominetworks.com)
- **PSIRT Page**: [Nozomi Networks PSIRT](https://security.nozominetworks.com/psirt/)