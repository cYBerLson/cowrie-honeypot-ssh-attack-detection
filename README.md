# Cowrie Honeypot SSH Attack Detection Lab

## Overview
This project demonstrates a controlled cybersecurity lab exercise focused on SSH attack detection and monitoring using the Cowrie Honeypot.

The lab simulates attacker activity from a Kali Linux machine against a Cowrie honeypot running on Ubuntu Server. Network reconnaissance, authentication attempts, and attacker interactions were captured and analyzed for defensive security and incident response learning purposes.

---

## Objectives
- Deploy and configure Cowrie Honeypot
- Simulate SSH attack activity
- Capture attacker behavior and login attempts
- Monitor live logs and session activity
- Analyze network traffic and forensic evidence
- Practice cybersecurity incident reporting

---

## Lab Environment

| Device | Role | IP Address |
|---|---|---|
| Kali Linux | Attacker Machine | 192.168.169.4 |
| Ubuntu Server + Cowrie | Honeypot Target | 192.168.169.3 |

Environment:
- VirtualBox Host-Only Network

---

## Tools Used
- Kali Linux
- Ubuntu Server
- Cowrie Honeypot
- Nmap
- Wireshark
- SSH Client
- VirtualBox

---

## Attack Simulation Process

### 1. Network Scanning
Nmap was used to identify exposed services on the target system.

```bash
nmap -sV 192.168.169.3
```

### 2. SSH Enumeration
An SSH service running on port 2222 was identified.

### 3. SSH Connection Attempt
Connection attempts were made from the attacker machine to the Cowrie honeypot.

```bash
ssh root@192.168.169.3 -p 2222
```

### 4. Session Monitoring
Cowrie captured:
- Source IP address
- Usernames
- Password attempts
- Session activity
- Connection termination events

---

## Key Findings
- SSH service detected on port 2222
- Login attempts successfully logged
- Attacker activity monitored in real time
- No actual system compromise occurred
- Honeypot effectively acted as a decoy environment

---

## Security Analysis
This exercise demonstrates how honeypots can be used to:
- Detect unauthorized access attempts
- Capture attacker behavior
- Improve threat intelligence
- Support forensic investigations
- Monitor suspicious activity safely

---

## Screenshots
Screenshots are available in the `/screenshots` folder:
- Nmap scan results
- Cowrie live logs
- SSH connection attempts
- Wireshark traffic capture

---

## Packet Capture
Network packet captures are available in the `/pcap` directory for further analysis.

---

## Skills Demonstrated
- Network Reconnaissance
- SSH Enumeration
- Honeypot Deployment
- Incident Reporting
- Packet Analysis
- Threat Monitoring
- Linux Administration
- Cybersecurity Lab Simulation

---

## Disclaimer
This project was conducted in a controlled and isolated lab environment strictly for educational and defensive cybersecurity purposes.
