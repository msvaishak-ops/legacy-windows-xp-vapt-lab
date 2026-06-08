# legacy-windows-xp-vapt-lab
Vulnerability Assessment and Security Hardening of a Windows XP Virtual Machine using Kali Linux, Nmap and Nessus.
# Windows XP Vulnerability Assessment and Security Hardening

## Project Overview

This project demonstrates a complete Vulnerability Assessment and Security Hardening lifecycle performed on a Windows XP virtual machine using Kali Linux.

## Objectives

- Host Discovery
- Port Scanning
- Service Enumeration
- SMB Enumeration
- Vulnerability Assessment
- Security Hardening
- Remediation Validation

## Tools Used

- Kali Linux
- Nmap
- Nessus Essentials
- VirtualBox

## Target

| Asset | Operating System |
|---------|---------|
| Windows XP VM | Windows XP SP3 |

## Assessment Methodology

### 1. Host Discovery

```bash
nmap -sn 192.168.1.0/24
```

### 2. Port Scanning

```bash
nmap -sS -Pn 192.168.1.23
```

### 3. Service Enumeration

```bash
nmap -sV -O 192.168.1.23
```

### 4. SMB Enumeration

```bash
nmap --script smb-os-discovery 192.168.1.23
```

### 5. SMB Protocol Analysis

```bash
nmap --script smb-protocols 192.168.1.23
```

### 6. Vulnerability Scanning

Performed using Nessus Essentials.

## Findings

| Vulnerability | Severity |
|--------------|-----------|
| Windows XP End of Life | Critical |
| SMBv1 Enabled | High |
| SMB Exposure | High |
| NetBIOS Exposure | Medium |
| SMB Information Disclosure | Medium |

## Security Hardening

- Disabled NetBIOS
- Enabled Windows Firewall
- Disabled unnecessary services
- Reduced exposed attack surface

## Validation

Post-remediation scans were performed to validate security improvements.

## Skills Demonstrated

- Vulnerability Assessment
- Network Enumeration
- SMB Security Testing
- Nessus Scanning
- Security Hardening
- Risk Assessment
- Technical Documentation
