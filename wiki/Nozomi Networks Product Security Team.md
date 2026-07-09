# Nozomi Networks Product Security Team

---

## Overview
The **Nozomi Networks Product Security Team** is a dedicated group within **Nozomi Networks** responsible for **identifying, investigating, and mitigating security vulnerabilities** in the company's products, including **Guardian**, **CMC (Central Management Console)**, and **Vantage**. The team plays a critical role in ensuring the security and resilience of Nozomi Networks' solutions, which are widely used in **Operational Technology (OT)** and **Industrial Control Systems (ICS)** environments.

---

## Responsibilities
1. **Vulnerability Research**: Proactively identify and analyze security vulnerabilities in Nozomi Networks' products.
2. **Incident Response**: Investigate and respond to security incidents and vulnerability reports from external researchers or customers.
3. **Security Bulletins**: Publish **security bulletins** to inform customers and the public about vulnerabilities, their impact, and remediation steps.
4. **Coordinated Disclosure**: Collaborate with external researchers, customers, and industry partners to ensure responsible disclosure of vulnerabilities.
5. **Product Hardening**: Work with development teams to **fix vulnerabilities** and improve the security posture of Nozomi Networks' products.
6. **Threat Intelligence**: Monitor emerging threats and vulnerabilities in the OT/ICS space and provide guidance to customers.

---

## Notable Contributions
The team has been instrumental in identifying and mitigating several high-profile vulnerabilities in Nozomi Networks' products. Below are some examples of their work:

### 2026
- **HTML Injection Vulnerabilities in Guardian/CMC v26.1.0**:
  - [[NN-2026:5-01 - HTML injection in Users in Guardian/CMC before 26.1.0]]: Discovered by **Stefano Libero** and **Andrea Palanca** during an internal investigation. This vulnerability allowed attackers to create malicious users with HTML tags in their usernames.
  - [[NN-2026:6-01 - HTML injection in Schedule Restore Archive in Guardian/CMC before 26.1.0]]: Discovered by **Stefano Libero** and **Andrea Palanca**. Attackers could define malicious restore schedules containing HTML tags.
  - [[NN-2026:7-01 - HTML injection in Smart Polling in Guardian/CMC before 26.1.0]]: Discovered by **Stefano Libero** and **Andrea Palanca**. Attackers with limited privileges could push malicious remote strategies containing HTML tags.

### 2019
- **Stored XSS in Guardian/CMC v19.0.4**:
  - [[NN-2019:1-01 - Stored XSS in field name data model]]: Reported by **Jonas Becker** of Deloitte GmbH. This vulnerability allowed attackers with admin access to inject malicious JavaScript code into the field name data model.

---

## Team Members
The Nozomi Networks Product Security Team includes security researchers, engineers, and analysts with expertise in **OT/ICS security**, **vulnerability research**, and **incident response**. Notable members mentioned in security bulletins include:
- **Stefano Libero**: Security researcher involved in discovering multiple HTML injection vulnerabilities in Guardian/CMC.
- **Andrea Palanca**: Security researcher who collaborated with Stefano Libero on identifying HTML injection vulnerabilities.

---

## How to Report Vulnerabilities
Nozomi Networks encourages **responsible disclosure** of security vulnerabilities. Researchers and customers can report vulnerabilities to the Product Security Team via:
- **Email**: [prodsec@nozominetworks.com](mailto:prodsec@nozominetworks.com)
- **PSIRT Portal**: [Nozomi Networks PSIRT](https://security.nozominetworks.com/psirt/)

---

## Coordinate Disclosure Policy
Nozomi Networks follows a **coordinated vulnerability disclosure (CVD)** policy to ensure that vulnerabilities are addressed responsibly and transparently. The policy includes:
1. **Acknowledgement**: The team acknowledges receipt of vulnerability reports within a specified timeframe.
2. **Investigation**: The team investigates the reported vulnerability and works with the reporter to validate the issue.
3. **Remediation**: The team develops and tests fixes for the vulnerability.
4. **Disclosure**: The team publishes a **security bulletin** with details of the vulnerability, its impact, and remediation steps. The reporter is acknowledged for their contribution (if they wish to be).

---

## Related Concepts
- [[Nozomi Networks]]
- [[Guardian/CMC]]
- [[HTML Injection]]
- [[Stored XSS]]
- [[CWE-79]]

---

## References
- [Nozomi Networks PSIRT](https://security.nozominetworks.com/psirt/)
- [Nozomi Networks Security Bulletins](https://security.nozominetworks.com/)
- [Nozomi Networks Official Website](https://www.nozominetworks.com/)