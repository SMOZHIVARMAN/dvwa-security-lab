# 🛡️ Damn Vulnerable Web Application (DVWA) – Ubuntu Setup

![DVWA](https://img.shields.io/badge/DVWA-Security%20Lab-green)
![Linux](https://img.shields.io/badge/OS-Ubuntu-orange)
![Apache](https://img.shields.io/badge/Web%20Server-Apache-red)
![PHP](https://img.shields.io/badge/PHP-8.x-blue)
![MySQL](https://img.shields.io/badge/Database-MySQL%208-informational)
![Status](https://img.shields.io/badge/Status-Working%20Setup-success)

---

## 📌 Overview

**Damn Vulnerable Web Application (DVWA)** is a deliberately insecure PHP/MySQL web application designed to help **students, developers, and security professionals** learn and practice common web vulnerabilities in a **legal and controlled environment**.

This repository provides a **tested and MySQL-8 compatible installation guide** for setting up DVWA on **Ubuntu Linux**.

> ⚠️ **Educational use only. Do NOT expose DVWA to the internet.**

---

## 🧱 Tech Stack

| Component | Technology |
|---------|-----------|
| OS | Ubuntu 20.04 / 22.04 / 24.04 |
| Web Server | Apache2 |
| Backend | PHP |
| Database | MySQL 8 |
| Application | DVWA |

---

## 📋 Prerequisites

- Ubuntu Linux
- Internet connection
- `sudo` privileges
- Git installed

---

## 🚀 Installation Guide

### 🔹 Step 1: Update System
```bash
sudo apt update && sudo apt upgrade -y

```
###
### 🔹 Step 2: Install Apache
```
sudo apt install apache2 -y
```
### 🔹 Verify:
```
http://localhost
```

### 🔹 Step 3: Install MySQL
```
sudo apt install mysql-server -y
```

### 🔹 Secure MySQL:

```
sudo mysql_secure_installation
```

## 🔹 Recommended options:

- Password policy: LOW

- Remove anonymous users: Yes

- Disallow remote root login: Yes

- Remove test database: Yes

- Reload privileges: Yes

### 🔹 Step 4: Create DVWA Database & User
```
sudo mysql
```
```
CREATE DATABASE dvwa;
CREATE USER 'dvwa'@'localhost' IDENTIFIED BY 'dvwa';
GRANT ALL PRIVILEGES ON dvwa.* TO 'dvwa'@'localhost';
FLUSH PRIVILEGES;
EXIT;
```
### 🔹 Step 5: Install PHP & Required Extensions
```
sudo apt install php libapache2-mod-php php-mysqli php-gd php-xml php-mbstring -y
```

### 🔹Restart Apache:
```
sudo systemctl restart apache2
```
### 🔹 Step 6: Remove Default Apache Page
```
sudo mv /var/www/html/index.html /var/www/html/index.html.bak
```
### 🔹 Step 7: Clone DVWA Repository
```
cd /var/www/html
````
```
sudo git clone https://github.com/digininja/DVWA.git
```
### 🔹 Step 8: Set Permissions
```
sudo chown -R www-data:www-data /var/www/html/DVWA
sudo chmod -R 755 /var/www/html/DVWA
sudo chmod -R 777 /var/www/html/DVWA/config
sudo chmod -R 777 /var/www/html/DVWA/hackable/uploads
```
### 🔹 Step 9: Configure DVWA
```
cd /var/www/html/DVWA/config
```
```
sudo cp config.inc.php.dist config.inc.php
sudo nano config.inc.php
```

### 🔹 Set

```
$_DVWA['db_server']   = '127.0.0.1';
$_DVWA['db_database'] = 'dvwa';
$_DVWA['db_user']     = 'dvwa';
$_DVWA['db_password'] = 'dvwa';
$_DVWA['default_security_level'] = 'low';
```

### 🔹 Step 10: Enable Required PHP Settings:

```
sudo nano /etc/php/*/apache2/php.ini
```

### 🔹 Ensure:
```
allow_url_fopen = On
allow_url_include = On
display_errors = On
```

### 🔹 Restart Apache:
```
sudo systemctl restart apache2
```
### 🔹 Step 11: MySQL 8 Compatibility Fix (IMPORTANT)

### 🔹 Edit:
```
sudo nano /var/www/html/DVWA/dvwa/includes/DBMS/MySQL.php
```

### 🔹Remove IF NOT EXISTS from:
```
ALTER TABLE users ADD role VARCHAR(20) DEFAULT 'user';
ALTER TABLE users ADD COLUMN account_enabled TINYINT(1) DEFAULT 1;
```

### 🔹 Restart Apache:
```
sudo systemctl restart apache2
```
### 🔹 Step 12: Initialize DVWA Database

- open:
```
http://localhost/DVWA/setup.php
```

- Click:
```
Create / Reset Database
```
### 🔹 Step 13: Login
```
URL: http://localhost/DVWA/login.php
Username: admin
Password: password
```
### 🔹 Step 14: Set Security Level

- Navigate to DVWA Security

- Set level to Low

- Click Submit


## ✅ Installation Successful

DVWA is now fully configured and operational.

## 🧪 Vulnerabilities Available

- SQL Injection

- Blind SQL Injection

- XSS (Reflected, Stored, DOM)

- Command Injection

- File Upload

- CSRF

- Brute Force

- Authentication Bypass

- CSP Bypass

## 🔐 Security Disclaimer

- Run DVWA only on localhost or isolated VMs

- Never deploy on public servers

- Intended strictly for learning and testing

## 📚 Learning Outcomes

- Web application security fundamentals

- OWASP Top 10 vulnerabilities

- Secure coding awareness

- Ethical hacking techniques

## 📝 License

DVWA is open-source and provided for **educational purposes only**.