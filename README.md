# 🔐 DVWA — Web Application Penetration Testing

> **Security assessment and penetration testing laboratory on Damn Vulnerable Web Application (DVWA).**

![Cybersecurity](https://img.shields.io/badge/Domain-Cybersecurity-orange)
![Web Security](https://img.shields.io/badge/Focus-Web%20Application%20Security-black)
![Kali Linux](https://img.shields.io/badge/Environment-Kali%20Linux-blue)
![DVWA](https://img.shields.io/badge/Target-DVWA-red)

---

## 📌 Overview

This project presents a **web application penetration testing assessment** conducted against **Damn Vulnerable Web Application (DVWA)** in an isolated local laboratory environment.

The objective was to understand, identify and technically exploit common web application vulnerabilities while analyzing their underlying causes through **PHP source-code review**.

The assessment combines:

* 🔎 Dynamic security testing
* 💥 Vulnerability exploitation
* 🧪 Proofs of Concept (PoC)
* 🔬 PHP source-code analysis
* 🛡️ Security control evaluation
* 🔧 Remediation and defense-in-depth recommendations

The assessment covers several security levels of DVWA and demonstrates how different security mechanisms can be bypassed or strengthened.

---

## 🎯 Objectives

The main objectives of this project were to:

* Identify and map web application vulnerabilities.
* Understand how common attacks work in practice.
* Intercept and manipulate HTTP requests.
* Develop and reproduce exploitation scenarios.
* Evaluate the effectiveness of security controls.
* Analyze vulnerable PHP implementations.
* Identify the root causes of vulnerabilities.
* Compare vulnerable and hardened implementations.
* Propose appropriate remediation measures.
* Develop practical skills in web application penetration testing.

---

## 🧪 Scope

| Parameter                | Description                            |
| ------------------------ | -------------------------------------- |
| **Target**               | Damn Vulnerable Web Application (DVWA) |
| **Environment**          | Isolated local laboratory              |
| **Operating System**     | Kali Linux                             |
| **Target URL**           | `http://localhost/DVWA/`               |
| **Testing approach**     | Grey-box                               |
| **Main security levels** | Low, Medium, High                      |
| **Reference level**      | Impossible                             |
| **Testing type**         | Web application penetration testing    |

### Out of scope

The following activities were excluded from the assessment:

* Denial of Service / Distributed Denial of Service
* Attacks against the underlying host operating system
* Attacks against Apache/MySQL infrastructure outside DVWA's application code
* Social engineering

---

## 🧭 Methodology

The assessment follows an approach inspired by **OWASP** and **PTES (Penetration Testing Execution Standard)**.

Each vulnerability was approached through several complementary phases:

### 1. 🔎 Dynamic Analysis

Understanding the application's behavior and identifying potentially interesting parameters, requests and attack surfaces.

### 2. 🕵️ HTTP Interception & Fuzzing

Using intercepted HTTP traffic to manipulate parameters, headers, cookies and requests.

### 3. 💥 Exploitation & Proof of Concept

Developing and executing payloads to demonstrate the impact of identified vulnerabilities.

### 4. 🔬 Static Analysis

Reviewing the PHP source code to understand the technical root cause of each vulnerability and identify implementation weaknesses.

### 5. 🛡️ Remediation

Analyzing the hardened implementation and identifying security mechanisms that can mitigate or prevent the vulnerability.

---

## 🛠️ Tools & Technologies

### Operating System

* **Kali Linux**

### Web Security Tools

* **Burp Suite**

  * Proxy
  * Repeater
  * Intruder
* **sqlmap**

### Technologies analyzed

* HTTP
* PHP
* SQL
* JavaScript
* Cookies & sessions
* HTTP headers
* Web authentication mechanisms

---

## 🧨 Vulnerabilities Tested

The project covers **17 DVWA modules**:

|  # | Module               | Category               |
| -: | -------------------- | ---------------------- |
| 01 | Brute Force          | Authentication         |
| 02 | Command Injection    | Injection              |
| 03 | CSRF                 | Request Forgery        |
| 04 | File Injection       | File Inclusion         |
| 05 | File Upload          | File Handling          |
| 06 | Insecure CAPTCHA     | Authentication         |
| 07 | SQL Injection        | Injection              |
| 08 | SQL Injection Blind  | Injection              |
| 09 | Weak Session         | Session Management     |
| 10 | DOM XSS              | Cross-Site Scripting   |
| 11 | Reflected XSS        | Cross-Site Scripting   |
| 12 | Stored XSS           | Cross-Site Scripting   |
| 13 | CSP Bypass           | Client-Side Security   |
| 14 | JavaScript Attacks   | Client-Side Security   |
| 15 | Authorisation Bypass | Access Control         |
| 16 | Open HTTP Redirect   | URL Redirection        |
| 17 | Cryptography         | Cryptographic Security |

---

## 🔥 Key Attack Areas

### 🔑 Authentication & Session Security

Testing included:

* Brute-force attacks
* Weak session identifiers
* CAPTCHA weaknesses
* Authentication controls
* Session manipulation

### 💉 Injection Attacks

The assessment covered:

* Command Injection
* SQL Injection
* Blind SQL Injection

The tests demonstrate how insufficient input validation and unsafe interaction with system commands or databases can lead to serious security consequences.

### 🌐 Cross-Site Scripting

Several XSS variants were investigated:

* DOM-based XSS
* Reflected XSS
* Stored XSS

The project also examines the relationship between client-side vulnerabilities and other attacks, including scenarios involving security-control bypasses.

### 📂 File-Based Attacks

The assessment includes:

* File Inclusion
* Local/Remote File Inclusion scenarios
* File Upload vulnerabilities
* Input validation bypasses

### 🔄 Request Forgery

CSRF testing demonstrates how an attacker can abuse authenticated user sessions when adequate anti-CSRF protections are not implemented.

### 🔐 Access Control & Application Logic

The assessment also examines:

* Authorization bypass
* Weak application logic
* Open HTTP redirects
* JavaScript-based security weaknesses

---

## 📊 Security-Level Analysis

One of the main objectives of the project was to observe how the application's security mechanisms evolve depending on the configured DVWA security level.

The tests therefore consider:

```text
Low
 ↓
Medium
 ↓
High
 ↓
Impossible
```

The **Impossible** level is used as a reference for analyzing hardened implementations and identifying appropriate defensive mechanisms.

This allows the project to go beyond simply exploiting vulnerabilities and understand **how they can be prevented**.

---

## 🔬 Static Code Review

An important part of this project is the analysis of the underlying PHP implementation.

For each vulnerability, the objective is to understand:

```text
User Input
    ↓
Application Processing
    ↓
Vulnerable Function / Logic
    ↓
Security Control
    ↓
Impact
```

The source-code review helps identify:

* Missing input validation
* Weak filtering mechanisms
* Unsafe function usage
* Missing authentication controls
* Insufficient output encoding
* Weak session management
* Inadequate authorization checks
* Incorrect security assumptions

---

## 🛡️ Remediation & Defense

The project does not stop at exploitation.

For each vulnerability, appropriate defensive mechanisms are examined, including:

* Strict input validation
* Allowlisting
* Output encoding
* Prepared SQL statements
* Secure session management
* CSRF tokens
* Strong authentication mechanisms
* Rate limiting
* Account lockout
* Secure file-upload validation
* Secure configuration
* Content Security Policy
* Secure HTTP headers
* Principle of least privilege
* Defense in depth

---

## 📁 Repository Structure

A recommended structure for the GitHub repository is:

```text
DVWA-Penetration-Testing/
│
├── RapportDVWA.pdf
│
└── README.md
```
---

## 📄 Full Report

The complete penetration testing report is available here:

**[📘 Rapport DVWA — PDF](./RapportDVWA.pdf)**

The report contains the detailed exploitation steps, Proofs of Concept, source-code analysis and remediation recommendations for the different modules.

---

## 🎓 Learning Outcomes

This project helped develop practical skills in:

* Web application penetration testing
* HTTP request analysis
* Burp Suite
* Web vulnerability identification
* Payload construction
* SQL Injection
* Command Injection
* Cross-Site Scripting
* CSRF
* File Inclusion
* File Upload vulnerabilities
* Session security
* Access control
* PHP source-code analysis
* Security remediation
* Defense in depth

---

## ⚠️ Legal & Ethical Disclaimer

DVWA is intentionally vulnerable and is designed for **educational and security-training purposes**.

The techniques demonstrated in this repository must only be used against:

* Systems you own
* Authorized penetration-testing environments
* Explicitly permitted targets
* Deliberately vulnerable laboratories such as DVWA

**Do not use these techniques against systems or applications without explicit authorization.**

---

## 👤 Author

### Oscar ALIDJINOU

🎓 Engineering Student — **IT Security & Digital Trust**
🏫 **ENSA Agadir — Morocco**

This project was created as part of my practical learning journey in **cybersecurity and web application security**.

---

## ⭐ Project Focus

> **Understand the vulnerability → Exploit it → Analyze the root cause → Understand the defense.**

The objective of this project is not only to demonstrate how vulnerabilities can be exploited, but also to understand **why they exist and how they can be properly mitigated**.

---

### 🔐 Cybersecurity | Web Pentesting | Ethical Hacking | Secure Development
