# CyberSecurity-ZAP-Audit
# Week 1: Automated Vulnerability Testing & Audit Report

[cite_start]This repository contains the comprehensive security assessment report generated during Week 1 of the Cybersecurity Internship[cite: 1, 2]. [cite_start]The primary objective was to perform automated security scans on a local Node.js backend application to discover hidden vulnerabilities and missing layer-defenses[cite: 10].

## 🛠️ Audit Environment & Tools
* [cite_start]**Target Application:** Node.js Backend Server [cite: 10]
* [cite_start]**Testing Tool:** OWASP ZAP (Zed Attack Proxy) v2.17.0 [cite: 10]
* [cite_start]**Deployment Context:** Localhost:8080 [cite: 10, 13]
* [cite_start]**Scan Configuration:** Traditional & AJAX Spidering followed by an Active Scan phase[cite: 13].

## 🔍 Key Security Findings

[cite_start]The automated assessment successfully mapped the attack surface and flagged several vulnerabilities classified by risk levels[cite: 13, 14]:

1. [cite_start]**Content Security Policy (CSP) Failure (Medium Risk):** Missing strict fallback directives (like `default-src`), leaving the application exposed to Cross-Site Scripting (XSS) and arbitrary script injections[cite: 18, 23, 24].
2. [cite_start]**User Controllable HTML Element Attribute (Low Risk):** Potential XSS where user-controlled input parameters are reflected back into HTML attributes without proper contextual sanitization[cite: 26].
3. [cite_start]**Information Disclosure (Low Risk):** Sensitive transactional or contextual parameters passing directly through the URL string, risking exposure via server logs or browser history[cite: 28, 29].
4. [cite_start]**Authentication Endpoints Mapping (Informational):** Successfully identified active session creation routes (such as `/api/auth/signin`)[cite: 30].

## 📂 Repository Contents
* [cite_start]`intern task 1.docx`: The complete professional Word report detailing the executive summary, automated scanning phases, severity breakdowns, and mitigation advice[cite: 3, 10, 11, 16].
