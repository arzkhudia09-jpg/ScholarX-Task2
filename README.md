# Web Application Vulnerability Assessment

## Project Overview

This project demonstrates a web application vulnerability assessment performed on a self-owned Flask-based task tracker application hosted on Render infrastructure.

The assessment was conducted using industry-standard cybersecurity tools and manual testing techniques to identify common web application security weaknesses, analyze HTTP traffic, and evaluate input validation behavior.

---

# Objective

The objective of this assessment was to:

- Perform reconnaissance and enumeration
- Identify exposed services and technologies
- Conduct automated vulnerability scanning
- Perform manual testing using Burp Suite
- Evaluate application input handling behavior
- Document findings professionally

---

# Scope

Testing was conducted only on a self-owned and authorized web application for educational and internship purposes.

Target Application:
- Flask Task Tracker Application

Hosting Environment:
- Render
- Cloudflare Reverse Proxy

---

# Tools Used

| Tool | Purpose |
|---|---|
| Nmap | Port scanning and service detection |
| WhatWeb | Technology fingerprinting |
| Nikto | Web vulnerability scanning |
| Gobuster | Directory enumeration |
| Burp Suite Community Edition | Manual web application testing |
| Firefox | Browser-based testing |

---

# Assessment Methodology

```text
Reconnaissance
      ↓
Enumeration
      ↓
Vulnerability Scanning
      ↓
Manual Testing
      ↓
Analysis & Reporting
```

---

# Assessment Activities

## Reconnaissance

- Port scanning using Nmap
- Service identification
- Infrastructure detection

## Enumeration

- Technology fingerprinting
- Directory enumeration
- Header analysis

## Automated Vulnerability Scanning

- HTTP header inspection
- Infrastructure analysis
- Web server observations

## Manual Testing

- Burp Suite HTTP interception
- Input validation testing
- HTML Injection testing
- Cross-Site Scripting (XSS) payload testing
- Special character handling analysis

---

# Key Findings

| Severity | Finding | Status |
|---|---|---|
| Informational | Cloudflare reverse proxy detected | Identified |
| Informational | Gunicorn server header identified | Identified |
| Informational | HTTP/3 support detected | Identified |
| Low | Automated scan interruptions observed | Identified |
| Medium | XSS payload testing performed | No vulnerability identified |
| Informational | Input validation testing | Handled safely |

---

# Manual Testing Observations

Manual testing was performed using Burp Suite Repeater and browser-based interaction.

The following payload categories were tested:

- HTML Injection
- XSS Payloads
- Special Character Inputs

The application rendered payloads as plain text and no unsafe JavaScript execution or HTML rendering behavior was observed during testing.

---

# Project Structure

```text
web-app-vulnerability-assessment/
│
├── README.md
├── tools-used.md
│
├── report/
│   └── vulnerability_report.pdf
│
├── screenshots/
│   ├── nmap.png
│   ├── whatweb.png
│   ├── gobuster.png
│   ├── nikto.png
│   ├── burp-history.png
│   └── manual-testing.png
│
├── scan-results/
│   ├── nmap.txt
│   ├── nikto.txt
│   ├── gobuster.txt
│   └── whatweb.txt
```

---

# Recommendations

- Continue validating and sanitizing user input
- Implement stronger Content Security Policy (CSP) headers
- Regularly update Flask dependencies
- Perform periodic security assessments
- Continue monitoring application activity and logs

---

# Conclusion

The assessment successfully demonstrated reconnaissance, enumeration, vulnerability scanning, and manual testing techniques against a Flask-based web application.

No critical vulnerabilities were identified during testing. The application handled tested payloads safely and demonstrated stable behavior during manual assessment.

---

# Disclaimer

This assessment was conducted strictly for authorized educational and internship purposes on a self-owned application. No unauthorized systems were targeted during testing.
