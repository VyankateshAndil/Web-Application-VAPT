# 🌐 Web Application VAPT

## 📌 Project Overview

This repository documents a **Vulnerability Assessment and Penetration Testing (VAPT)** project performed on a web application in a cybersecurity testing environment using Kali Linux.

The assessment focused on identifying potential security weaknesses through reconnaissance, website enumeration, technology fingerprinting, automated vulnerability assessment, manual penetration testing, controlled exploitation, and network traffic analysis.

The project also includes vulnerability risk assessment, supporting screenshots, and remediation recommendations to improve the security of the application.

**Project Title:** Vulnerability Assessment and Penetration Testing (VAPT) on a Web Application

**Project Domain:** Cybersecurity

**Testing Environment:** Kali Linux

**Target Application:** Web Application

---

# 🎯 Objectives

- Identify security vulnerabilities in the web application
- Analyze the potential impact of discovered vulnerabilities
- Perform manual penetration testing under authorized conditions
- Validate potential security weaknesses using appropriate testing techniques
- Assess vulnerability severity using CVSS where applicable
- Document findings with supporting screenshots and evidence
- Provide recommendations to mitigate identified security risks

---

# 🛠 Tools Used

| **Tool** | **Purpose** |
|:---|:---|
| Nmap | Port Scanning and Service Enumeration |
| Whois | Domain Registration Information |
| nslookup | DNS Information Gathering |
| WhatWeb | Web Technology Fingerprinting |
| Wappalyzer | Technology Stack Identification |
| BuiltWith | Web Technology Identification |
| Gobuster | Directory and Resource Enumeration |
| Burp Suite | HTTP Request Interception and Manual Testing |
| Nikto | Web Server Vulnerability Scanning |
| SQLMap | SQL Injection Testing |
| Nessus Essentials | Vulnerability Assessment |
| Acunetix | Web Application Vulnerability Scanning |
| Wireshark | Network Traffic and Packet Analysis |
| Firefox | Web Application Testing |
| FoxyProxy | Proxy Configuration |
| Kali Linux | Penetration Testing Environment |

---

# 🔍 Vulnerabilities and Security Testing

## 1️⃣ SQL Injection (SQLi)

- Tested the online banking login form for SQL injection weaknesses
- Submitted SQL injection payloads during manual testing
- Examined authentication bypass behavior
- Captured HTTP requests and responses using Burp Suite
- Used Burp Intruder to test multiple payload variations
- Reviewed SQL injection findings reported by Acunetix
- Evaluated potential database access and credential security risks
- Recommended prepared statements, parameterized queries, and input validation

## 2️⃣ Cross-Site Scripting (XSS)

- Tested application inputs using script-based payloads
- Examined application responses to submitted input
- Used Burp Suite Intruder to test multiple payload variations
- Documented the observed parser response and potential XSS risk
- Considered the security implications of untrusted input being reflected by the application
- Recommended output encoding, appropriate input sanitization, and Content Security Policy

## 3️⃣ Authentication Testing

- Evaluated the application's login mechanism
- Reviewed weak password and default credential risks
- Considered password complexity requirements
- Reviewed password reset and account lockout controls
- Considered multi-factor authentication as a security measure
- Recommended stronger authentication policies and secure session management

## 4️⃣ Sensitive Data Exposure

- Captured network traffic using Wireshark
- Applied HTTP traffic filtering to examine login requests
- Analyzed GET and POST requests associated with authentication
- Examined the HTTP stream and observed credentials transmitted in plaintext
- Documented the potential risk of network-level credential interception
- Recommended HTTPS/TLS enforcement and disabling plaintext HTTP access to login endpoints

## 5️⃣ Security Misconfiguration

- Scanned the web server using Nikto
- Reviewed potential missing security headers
- Examined server version disclosure
- Reviewed directory listing and outdated software concerns
- Considered weak SSL configuration warnings
- Recommended secure server configuration, software updates, and appropriate security headers

## 6️⃣ Directory and Resource Enumeration

- Used Gobuster to discover potentially accessible directories and files
- Examined common paths such as `/admin`, `/login`, `/uploads`, `/backup`, and `/config`
- Reviewed potentially exposed application resources
- Considered the security implications of publicly accessible directories
- Recommended restricting access to sensitive resources

## 7️⃣ SSL/TLS Security Review

- Reviewed SSL/TLS-related security observations included in the assessment
- Considered HTTPS availability and TLS versions
- Examined potential risks associated with weak cipher suites and certificate configuration
- Recommended secure TLS configuration and disabling outdated protocols

---

# ⚙️ Methodology

The assessment followed the nine phases documented in the project report.

## Phase 1: Planning and Authorization

- Defined the testing scope
- Identified the target URL or IP address
- Prepared the testing environment
- Installed the required tools
- Considered authorization and testing requirements

## Phase 2: Information Gathering (Reconnaissance)

- Collected target IP address and domain information
- Reviewed DNS records
- Identified web server technologies and programming languages
- Examined available information about frameworks and databases
- Identified open ports and running services

**Tools Used:** Nmap, Whois, nslookup, WhatWeb, Wappalyzer

## Phase 3: Website Enumeration

- Discovered potentially accessible directories and files
- Examined possible backup files
- Checked for administrative panels
- Reviewed potentially exposed configuration resources

**Tools Used:** Gobuster and other enumeration techniques documented in the report

## Phase 4: Fingerprinting

- Identified web server technologies
- Examined programming languages and frameworks
- Reviewed the technology stack
- Considered database and operating system information

**Tools Used:** WhatWeb, Wappalyzer, BuiltWith

## Phase 5: Vulnerability Assessment

- Performed web server vulnerability scanning using Nikto
- Reviewed vulnerability findings from Nessus Essentials
- Examined web application scanner findings from Acunetix
- Reviewed potential security weaknesses and severity classifications
- Documented relevant scanner evidence

## Phase 6: Manual Penetration Testing

- Tested authentication mechanisms
- Examined SQL injection weaknesses
- Intercepted and analyzed HTTP requests using Burp Suite
- Used Burp Intruder to test SQL injection and XSS payload variations
- Captured and analyzed network traffic using Wireshark
- Reviewed SSL/TLS-related security observations

## Phase 7: Exploitation

- Evaluated identified weaknesses through controlled testing
- Examined evidence associated with potential exploitation
- Documented relevant requests, responses, and screenshots
- Considered the potential impact of identified vulnerabilities

## Phase 8: Risk Assessment

- Evaluated vulnerability severity
- Considered the potential impact on confidentiality, integrity, and availability
- Reviewed CVSS scores where applicable
- Identified remediation priorities based on risk

## Phase 9: Remediation

- Recommended corrective actions for identified weaknesses
- Suggested secure coding practices
- Recommended improvements to authentication and session security
- Suggested security header and server configuration improvements
- Documented remediation recommendations in the report

---

# 📊 Risk Assessment

The report includes vulnerability severity classifications and a risk assessment table.

| **Vulnerability** | **CVSS Score Shown in Report** | **Risk Level Shown in Report** |
|:---|:---:|:---|
| SQL Injection | 9.8 | Critical |
| Stored XSS | 8.8 | High |
| Broken Authentication | 8.1 | High |
| IDOR | 7.5 | High |
| File Upload | 8.6 | High |
| Missing Security Headers | 4.3 | Medium |
| Directory Listing | 3.7 | Low |

These scores and classifications reproduce the values displayed in the uploaded report; they are not independent verification of each finding.

---

# 🛡️ Remediation Recommendations

## SQL Injection

- Use prepared statements
- Implement parameterized queries
- Validate user inputs
- Avoid dynamically constructing SQL queries using untrusted input

## Cross-Site Scripting (XSS)

- Encode application output appropriately
- Sanitize untrusted input where necessary
- Deploy a suitable Content Security Policy

## Broken Authentication

- Enforce strong password policies
- Enable multi-factor authentication where appropriate
- Implement secure session management
- Apply suitable login attempt restrictions

## File Upload Security

- Restrict allowed file types
- Verify MIME types and file content
- Scan uploaded files for malicious content
- Store uploads outside the publicly accessible web root where possible

## Security Headers

- Configure Content-Security-Policy
- Enable Strict-Transport-Security when HTTPS is correctly configured
- Configure X-Frame-Options where appropriate
- Configure X-Content-Type-Options
- Set a suitable Referrer-Policy

## Sensitive Data Protection

- Enforce HTTPS/TLS for authentication traffic
- Disable plaintext HTTP access to login endpoints
- Protect credentials and other sensitive information
- Avoid exposing sensitive data in application responses and logs

---

# 📄 Reporting Approach

Each vulnerability assessment includes:

- Vulnerability Description
- Testing Objective and Methodology
- Tools Used
- Supporting Screenshots
- HTTP Request and Response Evidence, where available
- Proof of Concept (PoC), where demonstrated
- Impact Analysis
- CVSS Score and Severity Classification, where applicable
- Remediation Recommendations

---

# 📁 Repository Structure

```text
Web-Application-VAPT/
│
├── recon/
│   └── reconnaissance-results/
│
├── enumeration/
│   └── directory-and-service-results/
│
├── exploitation/
│   └── authorized-testing-evidence/
│
├── screenshots/
│   └── proof-of-findings/
│
├── reports/
│   └── VAPT-Report.pdf
│
└── README.md
```

---

# 🚀 Key Learning Outcomes

- Practical understanding of web application VAPT
- Experience with reconnaissance and information gathering
- Knowledge of port scanning and service enumeration
- Familiarity with web technology fingerprinting
- Hands-on exposure to Burp Suite and SQL injection testing
- Understanding of XSS and authentication security testing
- Experience reviewing automated vulnerability scanner results
- Network traffic analysis using Wireshark
- Understanding of security misconfiguration and sensitive data exposure
- Risk assessment and remediation planning
- Professional penetration testing report writing

---

# ⚖️ Disclaimer

This project is intended for educational purposes and authorized security testing only.

Security testing must be conducted exclusively on systems for which appropriate permission has been obtained. All tools and techniques must be used responsibly and in accordance with applicable laws and authorization requirements.

---

# 👨‍💻 Author

**Vyankatesh Andil**

Cybersecurity Enthusiast | VAPT | Web Application Security
