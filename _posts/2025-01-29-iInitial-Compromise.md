---
title: "Useful Red Teaming Tools"
date: 2025-01-29 00:00:01 -0700
categories: [Red Teaming, Cybersecurity]
tags: [red teaming, tools, hacking, penetration testing]
---

# Useful Red Teaming Tools

## 1. Cobalt Strike
**What It Does:**  
A command-and-control (C2) framework used for red team operations and adversary simulation. It enables payload generation, beacon deployment, lateral movement, and post-exploitation tasks.

**How to Check If It's Running:**
```bash
ps aux | grep teamserver
sudo systemctl status teamserver
```

## 2. dnscan
**What It Does:**  
A tool used for brute-force subdomain enumeration by querying DNS records.

**How to Use:**  
```bash
python3 dnscan.py -d target-domain.com -w subdomains.txt -o results.txt
```

## 3. Spoofy
**What It Does:**  
A tool for assessing domain spoofability based on SPF and DMARC records.

**How to Use:**  
```bash
python3 spoofy.py -d target-domain.com -o stdout
```

## 4. Amass
**What It Does:**  
A reconnaissance tool for mapping a domain's attack surface using DNS enumeration.

**How to Use:**  
```bash
amass enum -d target-domain.com
```

## 5. Sublist3r
**What It Does:**  
A Python-based tool for discovering subdomains using search engines and brute force.

**How to Use:**  
```bash
python3 sublist3r.py -d target-domain.com
```

## 6. MailSniper
**What It Does:**  
A tool for testing password spraying attacks against Office 365 and Exchange services, allowing attackers to check for valid credentials.

**How to Use:**  
```powershell
Import-Module .\MailSniper.ps1
Invoke-SprayOWA -UserList users.txt -Password Password123 -Domain mail.target.com
```

## 7. SprayingToolkit
**What It Does:**  
A tool designed for performing password spraying attacks on various services, including Office 365.

**How to Use:**  
```powershell
Invoke-PasswordSprayO365 -Users users.txt -Password Password123!
```

## 8. Hunter.io
**What It Does:**  
An online service that gathers email addresses associated with a given domain for reconnaissance and social engineering.

**How to Use:**  
Visit [Hunter.io](https://hunter.io) and input a domain to retrieve email addresses and associated details.

## 9. Dig (Linux DNS Tool)
**What It Does:**  
A built-in Linux tool for querying DNS records, including MX, A, and TXT records.

**How to Use:**  
```bash
dig ANY target-domain.com
dig TXT target-domain.com
```

## 10. WhatWeb
**What It Does:**  
A reconnaissance tool that fingerprints web technologies, detecting CMS platforms, web servers, and security mechanisms.

**How to Use:**  
```bash
whatweb https://target-domain.com
```

## 11. o365enum
**What It Does:**  
A tool used for enumerating valid Office 365 email addresses by analyzing responses from login pages.

**How to Use:**  
```bash
python3 o365enum.py -d target-domain.com -u userlist.txt
```

## 12. Wireshark
**What It Does:**  
A network packet analyzer used to capture and inspect traffic for reconnaissance and troubleshooting.

**How to Use:**  
```bash
wireshark -k -i eth0
```

## 13. ProxyLogon & ProxyShell Exploit Tools
**What They Do:**  
Exploit known vulnerabilities in Microsoft Exchange to gain remote access.

**How to Check if a Target is Vulnerable:**  
```bash
nmap -p 443 --script http-vuln-cve2021-26855 target-ip
```

## 14. Nmap
**What It Does:**  
A network scanning tool used to identify open ports, running services, and potential vulnerabilities.

**How to Use:**  
```bash
nmap -A -T4 target-ip
```

## 15. SecurityTrails
**What It Does:**  
An online service for querying domain intelligence, subdomains, historical DNS records, and leaked credentials.

**How to Use:**  
Visit [SecurityTrails](https://securitytrails.com) and search for a domain to analyze its data footprint.
```