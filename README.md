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
- WhatWeb — additional web technology reconnaissance

## Methodology
1. Scope and authorization
2. Reconnaissance and connectivity verification
3. Network scanning with Nmap
4. Web server assessment with Nikto
5. Web application assessment with Burp Suite
6. Traffic analysis with Wireshark
7. Additional reconnaissance with WhatWeb
8. Findings documentation
9. Risk summary and remediation recommendations

## Findings

| Finding | Severity |
|---|---|
| Missing Security Headers | Medium |
| Unencrypted HTTP Communication | Medium |
| Application Configuration Information Disclosure | Low |

## Additional Tool – WhatWeb

WhatWeb was used as an additional reconnaissance tool to identify technologies and HTTP headers used by the OWASP Juice Shop application.

### Command Used

```bash
whatweb http://127.0.0.1:3000
```

### Result
WhatWeb successfully identified the target as OWASP Juice Shop and detected information such as HTML5 and HTTP headers including `X-Frame-Options`.

### Why This Tool Was Selected
WhatWeb was selected because it is a simple and fast reconnaissance tool that helps identify web technologies and server information.

### Added Value
The tool provided additional information about the application and its HTTP headers, supporting the reconnaissance phase of the security assessment.

## Evidence
Evidence is organized by tool under the `evidence/` directory.

## Repository Structure

```text
ethical-hacking-assessment/
├── README.md
├── report/
│   ├── Security-Assessment-Report-Draft.md
│   └── Security-Assessment-Report.pdf
├── evidence/
│   ├── nmap/
│   ├── nikto/
│   ├── burpsuite/
│   ├── wireshark/
│   └── whatweb/
│       ├── whatweb-result.png
│       └── whatweb-results.txt
├── screenshots/
└── notes/
```

## Important Note
This work was completed in an authorized training environment. No systems outside the defined scope were tested.
