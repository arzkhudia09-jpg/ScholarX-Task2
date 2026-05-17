# Tools Used During Vulnerability Assessment

This document describes the tools used during the web application vulnerability assessment project.

---

# 1. Nmap

## Purpose
Used for:
- Port scanning
- Service detection
- Infrastructure reconnaissance

## Command Used

```bash
nmap -sV flask-task-tracker-l9oj.onrender.com
```

## Key Outcome
- Identified exposed HTTP and HTTPS services
- Detected Cloudflare proxy infrastructure

---

# 2. WhatWeb

## Purpose
Used for:
- Web technology fingerprinting
- Infrastructure identification

## Command Used

```bash
whatweb https://flask-task-tracker-l9oj.onrender.com
```

## Key Outcome
- Identified hosting infrastructure
- Detected reverse proxy technologies

---

# 3. Gobuster

## Purpose
Used for:
- Directory enumeration
- Endpoint discovery

## Command Used

```bash
gobuster dir -u https://flask-task-tracker-l9oj.onrender.com -w /usr/share/wordlists/dirb/common.txt
```

## Key Outcome
- Enumerated accessible directories
- No sensitive endpoints identified

---

# 4. Nikto

## Purpose
Used for:
- Web vulnerability scanning
- HTTP header analysis
- Infrastructure observations

## Command Used

```bash
nikto -h https://flask-task-tracker-l9oj.onrender.com
```

## Key Outcome
- Detected Cloudflare protection
- Observed Gunicorn-related headers
- Identified automated scan interruptions

---

# 5. Burp Suite Community Edition

## Purpose
Used for:
- HTTP interception
- Request analysis
- Manual payload testing
- Repeater-based testing

## Activities Performed

- Intercepted HTTP requests
- Analyzed request/response behavior
- Tested HTML Injection payloads
- Tested XSS payloads
- Evaluated input validation behavior

## Key Outcome
- No reflected or stored XSS behavior observed
- Payloads rendered safely as plain text

---

# 6. Firefox Browser

## Purpose
Used for:
- Browser interaction
- Form testing
- Payload submission
- Proxy integration with Burp Suite

---

# Overall Learning Outcomes

This project provided practical exposure to:

- Web application reconnaissance
- Vulnerability assessment workflow
- HTTP traffic analysis
- Manual security testing
- Burp Suite usage
- Security reporting practices
- Secure input handling concepts
