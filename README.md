# Week 1: Automated Vulnerability Testing & Audit Report

**Intern Name:** BUSHRA JABEEN  
**Intern ID:** DHC-587
**Environment:** Localhost:8080  
**Status:** Completed  

This repository contains the comprehensive security assessment report generated during Week 1 of the Cybersecurity Internship. The primary objective was to perform automated security scans on a local Node.js backend application to discover hidden vulnerabilities and missing layer-defenses.

## 🛠️ Audit Environment & Tools
* **Target Application:** Node.js Backend Server
* **Testing Tool:** OWASP ZAP (Zed Attack Proxy)
* **Deployment Context:** Localhost:8080
* **Scan Configuration:** Traditional & AJAX Spidering followed by an Active Scan phase.

## 🔍 Key Security Findings

The automated assessment successfully mapped the attack surface and flagged several vulnerabilities classified by risk levels:

1. **Content Security Policy (CSP) Failure (Medium Risk):** Missing strict fallback directives (like `default-src`), leaving the application exposed to Cross-Site Scripting (XSS) and arbitrary script injections.
2. **User Controllable HTML Element Attribute (Low Risk):** Potential XSS where user-controlled input parameters are reflected back into HTML attributes without proper contextual sanitization.
3. **Information Disclosure (Low Risk):** Sensitive parameters passing directly through the URL string, risking exposure via server logs or browser history.
4. **Authentication Endpoints Mapping (Informational):** Successfully identified active session creation routes (such as `/api/auth/signin`).

## 📂 Repository Contents
* `intern task 1.docx`: The complete professional Word report detailing the executive summary, automated scanning phases, severity breakdowns, and mitigation advice.
