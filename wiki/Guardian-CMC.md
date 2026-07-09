# Guardian-CMC

---

## Overview
**Guardian-CMC** refers to the **Nozomi Networks' product suite** for **industrial cybersecurity**, specifically designed to protect **Operational Technology (OT)** and **Industrial Control Systems (ICS)** environments. The suite includes:

1. **Guardian**: A platform for **real-time monitoring, threat detection, and asset visibility** in OT and ICS networks.
2. **Central Management Console (CMC)**: A centralized management interface for **configuring, monitoring, and managing** multiple Guardian instances.

---

## Key Features
- **Asset Discovery**: Automatically identifies and inventories all devices and systems in the OT/ICS network.
- **Threat Detection**: Uses **signature-based and anomaly-based detection** to identify cyber threats, malware, and suspicious activities.
- **Vulnerability Management**: Scans for known vulnerabilities in OT/ICS devices and provides remediation guidance.
- **Network Monitoring**: Monitors network traffic for unusual patterns or behaviors that may indicate a cyber attack.
- **Compliance Reporting**: Generates reports to help organizations comply with industry regulations and standards (e.g., NERC CIP, IEC 62443).
- **Centralized Management (CMC)**: Allows administrators to manage multiple Guardian instances from a single console, simplifying deployment and maintenance.

---

## Use Cases
- **Industrial Control Systems (ICS)**: Protects critical infrastructure such as power plants, water treatment facilities, and manufacturing plants.
- **Operational Technology (OT)**: Secures OT networks in industries like oil and gas, chemical, and transportation.
- **Enterprise OT Security**: Provides visibility and security for OT environments in large enterprises.

---

## Security Vulnerabilities
Nozomi Networks regularly publishes **security bulletins** to address vulnerabilities in Guardian-CMC. Below are some notable examples:

### Stored XSS Vulnerabilities
- [[NN-2019:1-01 - Stored XSS in field name data model]]: A **Stored XSS** vulnerability in the field name data model, affecting Guardian/CMC versions before **v19.0.4**. Attackers with admin access could inject malicious JavaScript code, which would be executed by legitimate users.

### HTML Injection Vulnerabilities
- [[NN-2026:5-01 - HTML injection in Users in Guardian_CMC before 26.1.0]]: HTML injection in the **Users functionality**, affecting versions before **v26.1.0**. Attackers could create malicious users with HTML tags in their usernames, leading to phishing or redirect attacks.
- [[NN-2026:6-01 - HTML injection in Schedule Restore Archive in Guardian_CMC before 26.1.0]]: HTML injection in the **Schedule Restore Archive functionality**, affecting versions before **v26.1.0**. Attackers could define malicious restore schedules with HTML tags.
- [[NN-2026:7-01 - HTML injection in Smart Polling in Guardian_CMC before 26.1.0]]: HTML injection in the **Smart Polling functionality**, affecting versions before **v26.1.0**. Attackers with limited privileges could push malicious remote strategies containing HTML tags.

---

## Affected Versions and Solutions
| Vulnerability | Affected Versions | Solution |
| --- | --- | --- |
| Stored XSS in field name data model | Guardian, CMC < v19.0.4 | Upgrade to v19.0.4 or later |
| HTML injection in Users | Guardian, CMC < v26.1.0 | Upgrade to v26.1.0 or later |
| HTML injection in Schedule Restore Archive | Guardian, CMC < v26.1.0 | Upgrade to v26.1.0 or later |
| HTML injection in Smart Polling | Guardian, CMC < v26.1.0 | Upgrade to v26.1.0 or later |

---

## Mitigation Strategies
1. **Upgrade to Latest Version**: Always upgrade Guardian-CMC to the latest version to mitigate known vulnerabilities.
2. **Limit Access**: Restrict access to the web management interface using **internal firewalls** and **access controls**.
3. **Review User Accounts**: Regularly review all accounts with administrative access and delete unnecessary ones.
4. **Monitor for Suspicious Activity**: Use Guardian's monitoring capabilities to detect and respond to unusual network traffic or behaviors.
5. **Implement CSP**: Configure **Content Security Policy (CSP)** headers to restrict the execution of unauthorized scripts.

---

## Related Concepts
- [[Nozomi Networks]]
- [[HTML Injection]]
- [[Stored XSS]]
- [[CWE-79]]
- [[Nozomi Networks Product Security Team]]

---

## References
- [Nozomi Networks Official Website](https://www.nozominetworks.com/)
- [Nozomi Networks Security Bulletins](https://security.nozominetworks.com/)
- [Nozomi Networks PSIRT](https://security.nozominetworks.com/psirt/)
- [Guardian Product Page](https://www.nozominetworks.com/products/guardian/)
- [CMC Product Page](https://www.nozominetworks.com/products/central-management-console/)