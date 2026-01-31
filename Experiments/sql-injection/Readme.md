# 💉 SQL Injection – DVWA

## 🎯 Objective
To demonstrate **SQL Injection vulnerability** in Damn Vulnerable Web Application (DVWA) and understand how improper input validation can allow attackers to manipulate database queries.

---

## 🧪 Environment

| Component | Details |
|---------|---------|
| Application | DVWA |
| Vulnerability | SQL Injection |
| Security Level | Low |
| OS | Ubuntu Linux |
| Web Server | Apache |
| Database | MySQL |
| Browser | Firefox / Chrome |

---

## 📌 Vulnerability Description

**SQL Injection** is a web security vulnerability that allows an attacker to interfere with the SQL queries that an application makes to its database.  
It can allow attackers to:
- Bypass authentication
- Access sensitive data
- Modify or delete database records

---

## 🛠️ Steps Performed

1. Open DVWA in browser:
http://localhost/DVWA


2. Login using:
Username: admin
Password: password


3. Set **DVWA Security Level → Low**

4. Navigate to:
DVWA → SQL Injection


5. Enter the payload in the **User ID** input field.

6. Click **Submit**.

---

## 💉 Payload Used

```sql
' OR '1'='1
```
## 📸 Screenshots

### Screenshots of the attack and output are available in the screenshots/ folder:

- sql-injection.png

## 🔍 Observation
- The application returned all user records instead of a single user.

- Input was directly concatenated into the SQL query.

- No input validation or prepared statements were used.

## ⚠️ Impact
- If exploited in a real application, SQL Injection can lead to:

- Unauthorized access to database

- Exposure of usernames and passwords

- Data manipulation or deletion

- Complete database compromise

## 🛡️ Mitigation
- To prevent SQL Injection:

- Use prepared statements / parameterized queries

- Apply proper input validation

- Use least privilege database accounts

- Avoid dynamic SQL queries

## 📚 OWASP Reference

- **OWASP Top 10 – Injection**

- **CWE-89: Improper Neutralization of Special Elements used in an SQL Command**

## ✅ Conclusion
The SQL Injection vulnerability was successfully demonstrated in DVWA at Low security level.
This experiment highlights the importance of secure coding practices when interacting with databases.

## ⚠️ Disclaimer
This experiment was performed only on DVWA, a deliberately vulnerable application, for educational purposes.
No real systems were harmed.


---

