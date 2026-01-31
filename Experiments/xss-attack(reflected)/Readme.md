# 🔁 Reflected Cross-Site Scripting (XSS) – DVWA

## 🎯 Objective
To demonstrate **Reflected Cross-Site Scripting (XSS)** vulnerability in Damn Vulnerable Web Application (DVWA) and understand how malicious scripts can be reflected back to the user via server responses.

---

## 🧪 Environment

| Component | Details |
|----------|---------|
| Application | DVWA |
| Vulnerability | Reflected XSS |
| Security Level | Low |
| OS | Ubuntu Linux |
| Web Server | Apache |
| Database | MySQL |
| Browser | Firefox / Chrome |

---

## 📌 Vulnerability Description

**Reflected XSS** is a type of Cross-Site Scripting vulnerability where:
- User input is sent to the **server**
- The server reflects the input back in the **HTTP response**
- Malicious scripts are executed immediately in the victim’s browser

Unlike Stored XSS:
- The payload is **not stored** in the database
- The attack requires user interaction (clicking a link or submitting input)

---

## 🛠️ Steps Performed

1. Open DVWA in browser:
http://localhost/DVWA


2. Login using:
Username: admin
Password: password


3. Set **DVWA Security Level → Low**

4. Navigate to:
DVWA → XSS (Reflected)


5. Enter the payload in the **input field**.

6. Click **Submit**.

---

## 💉 Payload Used

```html
<script>alert('Reflected XSS')</script>
```
### Alternative payload:
```html
<img src=x onerror=alert('XSS')>
```
## 📸 Screenshots
Screenshots showing the reflected payload execution are available in the screenshots/ folder:

- payload.png

- alert.png

## 🔍 Observation
- User input was sent to the server without sanitization.

- The server reflected the input directly in the response.

- The browser executed the injected JavaScript code.

## ⚠️ Impact
- If exploited in a real-world application, Reflected XSS can:

- Execute malicious JavaScript in user browsers

- Steal cookies and session tokens

- Perform phishing attacks

- Redirect users to malicious websites

## 🛡️ Mitigation
- To prevent Reflected XSS:

- Validate and sanitize all user input

- Encode output before rendering in HTML

- Use frameworks with built-in XSS protection

- Implement Content Security Policy (CSP)

## 📚 OWASP Reference
- OWASP Top 10 – Cross-Site Scripting (XSS)

- CWE-79: Improper Neutralization of Input During Web Page Generation

- OWASP XSS Prevention Cheat Sheet

## ✅ Conclusion
The Reflected XSS vulnerability was successfully demonstrated in DVWA at Low security level.
This experiment highlights the risks of reflecting untrusted user input in server responses without proper encoding.

## ⚠️ Disclaimer
This experiment was performed only on DVWA, a deliberately vulnerable application, for educational purposes.
No real systems were attacked or harmed.


---
