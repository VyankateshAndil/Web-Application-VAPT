# 🌐 Web Application VAPT

## 📌 Project Overview

This repository documents an end-to-end **Web Application Vulnerability Assessment and Penetration Testing (VAPT)** performed on a deliberately vulnerable web application. The assessment focused on identifying, exploiting, and documenting security weaknesses aligned with the **OWASP Top 10** security risks.

**Target Application:**
Artist Vulnweb

---

# 🎯 Objectives

* Perform structured web application security testing
* Identify OWASP Top 10 vulnerabilities
* Exploit vulnerabilities in a controlled lab environment
* Assess risk using CVSS scoring
* Provide remediation recommendations

---

# 🛠 Tools Used

| Tool       | Purpose                             |
| ---------- | ----------------------------------- |
| Burp Suite | Web Proxy & Request Interception    |
| Nmap       | Port Scanning & Service Enumeration |
| SQLMap     | Automated SQL Injection Testing     |
| Hydra      | Brute Force Testing                 |
| Nikto      | Web Server Scanning                 |
| Kali Linux | Penetration Testing Environment     |

---

# 🔍 Vulnerabilities Identified

## 1️⃣ SQL Injection (SQLi)

* Extracted database information using manual and automated techniques
* Identified improper input validation
* Mapped related CVEs where applicable
* Assigned CVSS severity ratings

---

## 2️⃣ Cross-Site Scripting (XSS)

* Demonstrated reflected and stored XSS attacks
* Showed impact on session hijacking and user manipulation

---

## 3️⃣ Cross-Site Request Forgery (CSRF)

* Exploited missing anti-CSRF protections
* Demonstrated unauthorized state-changing requests

---

## 4️⃣ Command Injection

* Executed operating system commands through unsanitized input fields
* Demonstrated the impact of insecure input validation

---

# 📊 Risk Assessment

* Vulnerabilities classified as **Low / Medium / High**
* CVE references included where applicable
* CVSS scoring applied to determine severity
* Business impact analysis documented

---

# 📄 Reporting Approach

Each vulnerability assessment includes:

* Vulnerability Description
* Proof of Concept (PoC)
* Impact Analysis
* CVSS Score
* Remediation Recommendations
* Supporting Screenshots

---

# 📁 Repository Structure

```text
Web-Application-VAPT/
│
├── recon/
├── exploitation/
├── screenshots/
├── reports/
└── README.md
```

---

# 🚀 Key Learning Outcomes

* Practical understanding of OWASP Top 10 vulnerabilities
* Hands-on web application exploitation techniques
* Risk-based vulnerability assessment
* Professional penetration testing report writing
* Exposure to real-world web application attack methodologies

---

# ⚖️ Disclaimer

This project was conducted strictly in a controlled laboratory environment for educational and ethical purposes only.

No unauthorized systems were tested.

---

# 👨‍💻 Author

**Vyankatesh Andil**

Cybersecurity Enthusiast | VAPT | Web Application Security
