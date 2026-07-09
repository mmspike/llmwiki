# HTML Injection

---

## Overview
**HTML Injection** is a type of web vulnerability where an attacker injects malicious **HTML code** into a web application. This code is then rendered in the browser of a victim, potentially leading to **phishing attacks**, **open redirects**, or other malicious activities. Unlike **Cross-Site Scripting (XSS)**, HTML Injection typically does not involve the execution of JavaScript but can still be exploited to deceive users or manipulate web content.

---

## How It Works
1. **Injection Point**: An attacker identifies an input field or parameter in a web application that does not properly validate or sanitize user input.
2. **Malicious Input**: The attacker submits HTML tags (e.g., `<script>`, `<img>`, `<a>`) as input.
3. **Storage**: The malicious HTML is stored in the application's database or backend system (Stored HTML Injection).
4. **Rendering**: When a victim accesses the affected page or feature, the injected HTML is rendered in their browser.
5. **Exploitation**: The attacker can use this to perform actions such as:
   - **Phishing**: Displaying fake login forms or deceptive content.
   - **Open Redirects**: Redirecting users to malicious websites.
   - **Session Hijacking**: Stealing session cookies or credentials (if combined with JavaScript).

---

## Types of HTML Injection
1. **Stored HTML Injection**: The malicious HTML is permanently stored on the server and rendered when accessed by users. This is the most common type in web applications.
2. **Reflected HTML Injection**: The malicious HTML is included in a URL or input field and reflected back to the user in the response. This requires the victim to click on a specially crafted link.
3. **DOM-Based HTML Injection**: The malicious HTML is injected into the Document Object Model (DOM) of a webpage, typically through JavaScript manipulation.

---

## Real-World Examples
- [[NN-2026:5-01 - HTML injection in Users in Guardian_CMC before 26.1.0]]: HTML injection in the Users functionality of Guardian-CMC.
- [[NN-2026:6-01 - HTML injection in Schedule Restore Archive in Guardian_CMC before 26.1.0]]: HTML injection in the Schedule Restore Archive functionality.
- [[NN-2026:7-01 - HTML injection in Smart Polling in Guardian_CMC before 26.1.0]]: HTML injection in Smart Polling.

---

## Impact
- **Phishing Attacks**: Attackers can create fake forms or pages to steal user credentials.
- **Open Redirects**: Users can be redirected to malicious websites without their knowledge.
- **Defacement**: Attackers can modify the appearance of a webpage to display misleading or malicious content.
- **Session Hijacking**: If combined with JavaScript, attackers can steal session cookies or other sensitive data.

---

## Mitigation Strategies
1. **Input Validation**: Validate all user inputs to ensure they conform to expected formats and do not contain malicious HTML tags.
2. **Output Encoding**: Encode user inputs before rendering them in the browser to prevent HTML tags from being interpreted as code.
3. **Content Security Policy (CSP)**: Implement CSP headers to restrict the sources of executable scripts and other resources.
4. **Use Secure Frameworks**: Utilize web application frameworks that automatically handle input validation and output encoding (e.g., React, Angular, Django).
5. **Regular Audits**: Conduct regular security audits and penetration testing to identify and fix HTML injection vulnerabilities.

---

## Related Concepts
- [[Stored XSS]]
- [[CWE-79]]
- [[Guardian-CMC]]
- [[Nozomi Networks]]

---

## References
- [OWASP: HTML Injection](https://owasp.org/www-community/attacks/HTML_Injection)
- [CWE-79: Improper Neutralization of Input During Web Page Generation](https://cwe.mitre.org/data/definitions/79.html)