# IoT Device Penetration Testing
### Penetration Testing Module — CA Project | May 2026

## Overview
This project involved performing a security assessment on 
a simulated organisational IoT environment using OWASP 
IoTGoat v1.0. The goal was to assess device security, 
identify weak configurations, and evaluate exposure risks.

---

## Environment
| Item | Details |
|------|---------|
| Target Device | OWASP IoTGoat v1.0 |
| Target IP | 192.168.57.128 |
| Attacker OS | Kali Linux 2026 |
| Network | VMware Host-Only (isolated) |

---

## Tools Used
| Tool | Purpose |
|------|---------|
| Nmap | Network scanning and port discovery |
| Nikto | Web vulnerability scanning |
| Netcat | Backdoor connection testing |
| John the Ripper | Password hash analysis |
| Wireshark | Network traffic analysis |

---

## Findings Summary
| ID | Finding | Severity |
|----|---------|----------|
| F-001 | Unauthenticated backdoor on port 5515 | 🔴 Critical |
| F-002 | Telnet service running unencrypted | 🔴 Critical |
| F-003 | Weak MD5 password hashes exposed | 🔴 Critical |
| F-004 | WiFi access point with no encryption | 🔴 Critical |
| F-005 | Linux kernel from 2019 (outdated) | 🟠 High |
| F-006 | dnsmasq 2.73 with known CVEs | 🟠 High |
| F-007 | Backup config files exposed | 🟠 High |
| F-008 | Missing X-Frame-Options header | 🟠 High |
| F-009 | Missing HSTS header | 🟠 High |
| F-010 | Self-signed SSL certificate | 🟡 Medium |
| F-011 | Certificate hostname mismatch | 🟡 Medium |
| F-012 | Missing X-Content-Type-Options | 🟡 Medium |
| F-013 | ETag inode leakage CVE-2003-1418 | 🟡 Medium |
| F-014 | Duplicate /etc/shadow entry | 🟢 Low |

---

## Screenshots
### Backdoor Shell Access (F-001)
![Backdoor]("E:\IoT-Penetration-Testing\screenshots\02_backdoor_shell.png")

### Nmap Scan Results
![Nmap]("E:\IoT-Penetration-Testing\screenshots\01_nmap_results.png")

---

## Report
Full penetration testing report available in the 
/report folder.

---

## Disclaimer
All testing was conducted on OWASP IoTGoat v1.0, a 
deliberately vulnerable device built for educational 
purposes. Testing was done in an isolated VMware 
environment with no connection to any real systems.
This project is for academic use only.