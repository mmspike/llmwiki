# CWE-79: Improper Neutralization of Input During Web Page Generation

---

## Overview
**CWE-79**, officially titled **"Improper Neutralization of Input During Web Page Generation"**, is a **Common Weakness Enumeration (CWE)** entry that describes a class of vulnerabilities where an application fails to properly **sanitize or neutralize user-supplied input** before including it in web page output. This weakness is the root cause of **Cross-Site Scripting (XSS)** and **HTML Injection** vulnerabilities.

---

## Description
When an application includes **untrusted data** in a web page without proper validation, encoding, or escaping, attackers can inject **malicious scripts or HTML** into the page. These scripts execute in the context of the victim's browser, allowing attackers to:
- Steal sensitive data (e.g., session cookies, credentials).
- Perform actions on behalf of the victim.
- Deface or manipulate web content.
- Redirect users to malicious sites.

---

## Common Attack Vectors
1. **Stored XSS**: Malicious input is stored on the server (e.g., in a database) and later retrieved and rendered in the browser.
   - Example: [[NN-2019:1-01 - Stored XSS in field name data model]]
2. **Reflected XSS**: Malicious input is included in a URL or input field and reflected back to the user in the response.
3. **DOM-Based XSS**: Malicious input is injected into the Document Object Model (DOM) of a webpage, typically through JavaScript manipulation.
4. **HTML Injection**: Malicious HTML tags are injected into a webpage, leading to phishing or redirect attacks.
   - Examples: 
     - [[NN-2026:5-01 - HTML injection in Users in Guardian_CMC before 26.1.0]]
     - [[NN-2026:6-01 - HTML injection in Schedule Restore Archive in Guardian_CMC before 26.1.0]]
     - [[NN-2026:7-01 - HTML injection in Smart Polling in Guardian_CMC before 26.1.0]]

---

## Impact
- **Data Theft**: Attackers can steal sensitive information such as session cookies, credentials, or personal data.
- **Session Hijacking**: Attackers can impersonate users by stealing session tokens.
- **Defacement**: Attackers can modify the appearance of a webpage to display malicious or misleading content.
- **Phishing**: Attackers can create fake login forms or redirect users to malicious sites.
- **Malware Distribution**: Attackers can inject scripts that download and execute malware on the victim's machine.

---

## Mitigation Strategies
1. **Input Validation**: Validate all user inputs to ensure they conform to expected formats and do not contain malicious scripts or HTML tags.
2. **Output Encoding**: Encode user inputs before rendering them in the browser. Use context-aware encoding (e.g., HTML, JavaScript, CSS, URL) to prevent scripts from being executed.
3. **Content Security Policy (CSP)**: Implement CSP headers to restrict the sources of executable scripts and other resources.
4. **Use Secure Frameworks**: Utilize web application frameworks that automatically handle input validation and output encoding (e.g., React, Angular, Django, Ruby on Rails).
5. **HTTP-Only Cookies**: Use HTTP-only flags for cookies to prevent JavaScript from accessing them.
6. **Regular Audits**: Conduct regular security audits and penetration testing to identify and fix CWE-79 vulnerabilities.

---

## Example Code Snippets
### Vulnerable Code (PHP)
```php
<?php
// Vulnerable: User input is directly included in the HTML output
$userInput = $_GET['input'];
echo "<div>$userInput</div>";
?>
```

### Fixed Code (PHP)
```php
<?php
// Fixed: User input is HTML-encoded before output
$userInput = $_GET['input'];
echo "<div>" . htmlspecialchars($userInput, ENT_QUOTES, 'UTF-8') . "</div>";
?>
```

---

## Related Concepts
- [[HTML Injection]]
- [[Stored XSS]]
- [[Guardian-CMC]]
- [[Nozomi Networks]]

---

## References
- [CWE-79: Improper Neutralization of Input During Web Page Generation](https://cwe.mitre.org/data/definitions/79.html)
- [OWASP: XSS Prevention Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html)
- [OWASP: Testing for XSS](https://owasp.org/www-project-web-security-testing-guide/latest/4-Web_Application_Security_Testing/07-Input_Validation_Testing/06.1-Testing_for_Reflected_Cross_Site_Scripting)
- [PortSwigger: XSS Labs](https://portswigger.net/web-security/cross-site-scripting)