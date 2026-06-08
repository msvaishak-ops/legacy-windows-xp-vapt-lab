# Windows XP Security Hardening Guide

## Objective

Reduce the attack surface identified during the vulnerability assessment.

---

## 1. Disable NetBIOS

Path:

Control Panel → Network Connections → Local Area Connection → Properties → Internet Protocol (TCP/IP) → Properties → Advanced → WINS

Action:

Select:

Disable NetBIOS over TCP/IP

Reason:

Reduces NetBIOS-based information disclosure and network exposure.

---

## 2. Enable Windows Firewall

Path:

Control Panel → Windows Firewall

Action:

Enable firewall protection.

Reason:

Blocks unauthorized inbound connections.

---

## 3. Disable Remote Registry

Path:

Start → Run → services.msc

Service:

Remote Registry

Action:

Startup Type → Disabled

Reason:

Prevents remote registry modification.

---

## 4. Disable SSDP Discovery Service

Service:

SSDP Discovery Service

Action:

Disabled

Reason:

Reduces UPnP attack surface.

---

## 5. Disable Universal Plug and Play Device Host

Service:

Universal Plug and Play Device Host

Action:

Disabled

Reason:

Reduces unnecessary network exposure.

---

## 6. Disable Messenger Service

Service:

Messenger

Action:

Disabled

Reason:

Legacy service with no operational requirement.

---

## 7. Disable Computer Browser Service

Service:

Computer Browser

Action:

Disabled

Reason:

Reduces network information disclosure.

---

## 8. Review Shared Resources

Command:

net share

Action:

Remove unnecessary shares.

Reason:

Minimizes unauthorized access opportunities.

---

## Validation Commands

Run from Kali Linux:

nmap -sV 192.168.1.23

nmap --script smb-os-discovery 192.168.1.23

nmap --script smb-protocols 192.168.1.23

Compare results before and after hardening.

---

## Outcome

Security hardening reduced the attack surface and improved the overall security posture of the Windows XP system.
