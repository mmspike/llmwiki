# Stored XSS

---

## Overview
**Stored XSS (Cross-Site Scripting)**, also known as **Persistent XSS**, is a type of **XSS vulnerability** where malicious scripts are **permanently stored** on the target server (e.g., in a database, comment field, or forum post). When a victim accesses the affected page, the malicious script is **retrieved from the server** and executed in their browser. This allows attackers to perform actions on behalf of the victim, such as stealing session cookies, defacing websites, or redirecting users to malicious sites.

---

## How It Works
1. **Injection**: An attacker identifies a vulnerable input field (e.g., a comment box, user profile, or data model field) and injects malicious JavaScript code.
2. **Storage**: The malicious script is stored on the server, typically in a database or file system.
3. **Retrieval**: When a victim accesses the affected page, the server retrieves the stored script and includes it in the HTML response.
4. **Execution**: The victim's browser executes the malicious script in the context of the vulnerable website, allowing the attacker to perform actions on behalf of the victim.

---

## Key Characteristics
- **Persistence**: The malicious script remains on the server until it is manually removed or the vulnerability is patched.
- **High Impact**: Can affect all users who visit the vulnerable page, including administrators.
- **Stealthy**: Attackers can use obfuscation techniques to hide the malicious script from casual inspection.

---

## Real-World Examples
- [[NN-2019:1-01 - Stored XSS in field name data model]]: Stored XSS vulnerability in the field name data model of Guardian/CMC, allowing attackers with admin access to inject malicious JavaScript.

---

## Impact
- **Session Hijacking**: Stealing session cookies to impersonate users.
- **Account Takeover**: Performing actions on behalf of the victim, such as changing passwords or making unauthorized transactions.
- **Defacement**: Modifying the appearance of a webpage to display malicious content.
- **Keylogging**: Capturing keystrokes to steal sensitive information.
- **Phishing**: Redirecting users to fake login pages to steal credentials.

---

## Mitigation Strategies
1. **Input Validation**: Validate all user inputs to ensure they conform to expected formats and do not contain malicious scripts.
2. **Output Encoding**: Encode user inputs before rendering them in the browser to prevent scripts from being executed.
3. **Content Security Policy (CSP)**: Implement CSP headers to restrict the sources of executable scripts and other resources.
4. **Use Secure Frameworks**: Utilize web application frameworks that automatically handle input validation and output encoding (e.g., React, Angular, Django).
5. **Regular Audits**: Conduct regular security audits and penetration testing to identify and fix Stored XSS vulnerabilities.

---

## Stored XSS vs. Other XSS Types
| Type | Persistence | Execution Context | Example |
| --- | --- | --- | --- |
| **Stored XSS** | Permanent (stored on server) | Victim's browser | Malicious comment on a forum |
| **Reflected XSS** | Temporary (in URL or input) | Victim's browser | Malicious link in an email |
| **DOM-Based XSS** | Temporary (in DOM) | Victim's browser | Client-side script manipulation |

---

## Related Concepts
- [[HTML Injection]]
- [[CWE-79]]
- [[Guardian/CMC]]
- [[Nozomi Networks]]

---

## References
- [OWASP: Stored XSS](https://owasp.org/www-community/attacks/xss#stored-xss)
- [CWE-79: Improper Neutralization of Input During Web Page Generation](https://cwe.mitre.org/data/definitions/79.html)