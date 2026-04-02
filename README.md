# vulnapp-passive-reconnaissance

# Passive Reconnaissance of VulnApp Solutions Inc.

![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Scope](https://img.shields.io/badge/Scope-Passive%20Only-blue)
![Target](https://img.shields.io/badge/Target-VulnApp%20Solutions%20Inc.-orange)
![OWASP](https://img.shields.io/badge/Framework-OWASP%20Top%2010%202021-red)
![License](https://img.shields.io/badge/Purpose-Educational-lightgrey)

## Overview

This repository contains a passive reconnaissance and vulnerability assessment planning project conducted against **VulnApp Solutions Inc.**

The work was performed strictly within **passive scope**, focusing on publicly accessible pages, HTML source inspection, HTTP response analysis, and external passive intelligence sources. No active exploitation, brute forcing, payload injection, or authentication bypass was performed.

## Target

- **Application:** VulnApp Solutions Inc.
- **URL:** `http://143.198.205.185/`

## Project Objective

The objective of this project was to gather maximum intelligence about the application's exposed structure, sensitive endpoints, weak security controls, and likely attack surfaces using only passive reconnaissance techniques.

## Scope

### Included
- Publicly accessible endpoints
- Navigation analysis
- HTML source inspection
- HTTP header observation
- Hidden endpoint discovery through low-footprint inference
- External passive intelligence gathering
- Risk classification and OWASP mapping

### Excluded
- SQL injection testing
- XSS payload execution
- Authentication bypass
- Command injection
- File upload exploitation
- Brute-force or active scanning
- Any intrusive or destructive action

## Key Findings

- Public exposure of sensitive endpoints
- Unauthenticated administrative access
- IDOR exposure through predictable profile identifiers
- Reflected XSS evidence in search functionality
- Missing CSRF protection on the login form
- Internal product and developer comment leakage
- Lack of HTTPS / weak transport security
- Hidden endpoints revealing dynamic file-loading behavior
- Public PHP configuration exposure through `info.php`
- External infrastructure disclosure through passive OSINT

## Hidden Endpoints Identified

- `/page.php`
- `/page.php?file=welcome.html`
- `/info.php`

## Tools Used

- **Google Chrome Developer Tools**
- **Burp Suite Community Edition** (passive mode only)
- **Mozilla Firefox**
- **Wappalyzer**
- **Shodan**
- **Wayback Machine**

## Methodology Summary

1. Initial scoping of the target application
2. Enumeration of visible endpoints from public navigation
3. Discovery of hidden endpoints through passive inference
4. HTML source inspection for comments, parameters, and forms
5. HTTP response header review
6. Information disclosure analysis
7. URL pattern and IDOR analysis
8. OWASP Top 10:2021 mapping
9. Severity classification and risk assessment
10. Recommendations and active testing scope definition

## Repository Contents

- `report/` - Final report file

## OWASP Top 10 Mapping

This project references the following OWASP Top 10:2021 categories:

- **A01** Broken Access Control
- **A02** Cryptographic Failures
- **A03** Injection
- **A04** Insecure Design
- **A05** Security Misconfiguration
- **A07** Identification and Authentication Failures

## Learning Outcomes

This project strengthened practical skills in:

- Passive web reconnaissance
- Endpoint mapping
- HTML source analysis
- Information disclosure identification
- Infrastructure intelligence gathering
- Evidence-based risk assessment
- Security reporting aligned with professional standards

## References

- [OWASP Top 10:2021](https://owasp.org/Top10/2021/)
- [OWASP Web Security Testing Guide v4.2](https://owasp.org/www-project-web-security-testing-guide/v42/)

## Disclaimer

This project was conducted strictly for **educational purposes** within an authorized training environment. All findings were obtained through **passive observation only**, and no active exploitation was performed.
