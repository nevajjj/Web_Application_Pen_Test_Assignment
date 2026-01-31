# Web Application Penetration Testing Report – Kiwi.com

## 📌 Overview
This repository contains a **web application penetration testing report** conducted under an **authorized bug bounty program and academic scope** as part of a Diploma in Cybersecurity & Digital Forensics.

The assessment focuses on identifying security weaknesses across multiple Kiwi.com subdomains, with an emphasis on **authentication, session management, security headers, and web misconfigurations**, following industry-standard methodologies and OWASP guidelines.

All testing was performed using **dedicated test accounts**, **non-destructive techniques**, and within defined scope and rate limits.

---

## 🎯 Scope of Assessment

| Domain | Purpose |
|------|--------|
| `www.kiwi.com` | Main customer-facing web application |
| `auth.skypicker.com` | Authentication & token management API |
| `tequila.kiwi.com` | B2B platform (publicly accessible components only) |
| `jobs.kiwi.com` | Recruitment and careers website |

---

## 🧪 Methodology

The penetration testing followed a structured approach:

### 1. Reconnaissance
- Technology stack identification
- DNS and subdomain enumeration
- WAF detection
- Port and service scanning

### 2. Automated Testing
- Security header analysis
- Vulnerable dependency checks
- Parameter discovery and fuzzing
- SSL/TLS configuration testing
- Web spidering and crawling

### 3. Manual Testing
- Authentication and session handling analysis
- Token lifecycle and refresh behavior
- Access control validation
- Parameter manipulation
- CORS and CSP validation
- Input validation and injection testing

Testing aligned with **OWASP Top 10** and real-world attack scenarios.

---

## 🚨 Key Findings (High-Level)

### 🔴 Critical / High Risk
- **Session Hijacking via Reusable Authentication Tokens**
- **Refresh Token Replay Behavior**

### 🟠 Medium Risk
- **Cross-Origin Resource Sharing (CORS) Misconfiguration**
- **Missing Content Security Policy (CSP)**

### 🟢 Informational / Defense-in-Depth
- Security header inconsistencies
- Cookie attribute hardening opportunities

> Each finding includes **impact assessment**, **proof of concept**, **CVSS scoring**, and **remediation recommendations** in the report.

---

## 🧠 OWASP Top 10 Coverage

| Category | Identified |
|--------|-----------|
| Broken Access Control | ✅ |
| Security Misconfiguration | ✅ |
| Identification & Authentication Failures | ✅ |
| Injection | ❌ |
| Cryptographic Failures | ❌ |
| SSRF | ❌ |

---

## 🛠 Tools Used

- Burp Suite
- OWASP ZAP
- Nmap
- WafW00f
- Nikto
- FFuF / Wfuzz
- ParamSpider
- Retire.js
- SSLScan
- Amass
- DNSDumpster
- curl

---

## ⚠️ Ethical & Legal Disclaimer

All testing documented in this repository was conducted:
- Under **explicit authorization**
- Using **test accounts**
- In accordance with **bug bounty rules of engagement**
- For **educational and security research purposes only**

This repository **does not promote or condone unauthorized testing or exploitation**.

---


## 📄 Report

The full penetration testing report is available in this repository:

📁 `Assignment 2 - Pentesting Report.docx`

---

## 📚 References
- OWASP Top 10 (2021)
- CVSS v3.1 Scoring Guidelines
- Kiwi.com Bug Bounty Program Rules
