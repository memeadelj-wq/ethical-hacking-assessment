# Ethical Hacking Security Assessment

## Project Overview
This repository documents an authorized security assessment performed against OWASP Juice Shop in a local training lab.

## Scope
- Target: OWASP Juice Shop
- Target IP: `192.168.56.101`
- Application Port: `3000`
- Environment: Authorized local lab only
- Attacker machine: Kali Linux

## Tools Used
- Nmap — network/service discovery
- Nikto — web server security assessment
- Burp Suite — HTTP request/response inspection
- Wireshark — network traffic analysis

## Methodology
1. Scope and authorization
2. Reconnaissance and connectivity verification
3. Network scanning with Nmap
4. Web server assessment with Nikto
5. Web application assessment with Burp Suite
6. Traffic analysis with Wireshark
7. Findings documentation
8. Risk summary and remediation recommendations

## Findings
| Finding | Severity |
|---|---|
| Missing Security Headers | Medium |
| Unencrypted HTTP Communication | Medium |
| Application Configuration Information Disclosure | Low |

## Evidence
Evidence is organized by tool under the `evidence/` directory.

## Repository Structure
```text
ethical-hacking-assessment/
├── README.md
├── report/
│   └── Security-Assessment-Report-Draft.md
├── evidence/
│   ├── nmap/
│   ├── nikto/
│   ├── burpsuite/
│   └── wireshark/
├── screenshots/
└── notes/
```

## Important Note
This work was completed in an authorized training environment. No systems outside the defined scope were tested.
