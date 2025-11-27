🛡️ Network Penetration Testing Project
Using Metasploitable 2 as Target Machine

📌 Overview

This project is a full Network Penetration Test performed on a vulnerable virtual machine (Metasploitable 2) inside an isolated lab environment.
The goal is to simulate real-world offensive security techniques including:

Network Scanning

Service Enumeration

Vulnerability Identification

Exploitation

Post‑Exploitation

Evidence Documentation

Reporting

The project follows industry-standard methodologies such as PTES and OWASP Testing Guide.

📂 Project Structure
-Evidence/
-Project-Planning/
-Feedback-&-Evaluation/
-User-Stories-&-Use-Cases/
-System-Analysis-&-Design/
-Nessus Results/
-Report/
-README/

🎯 Objectives

Identify exposed services on Metasploitable2.

Enumerate each service for potential vulnerabilities.

Exploit real vulnerabilities using Metasploit and manual techniques.

Capture proof-of-compromise screenshots.

Document all findings with severity, impact, and mitigation.

🚀Key Vulnerabilities Exploited 

UnrealIRCD Remote Command Execution (Port 6667)

Ingreslock Backdoor Shell (Port 1524)

FTP Anonymous Login (Port 21)

SMB Null Sessions (Ports 139/445)

VNC Weak Authentication (Port 5900)

📊 Results

Multiple vulnerabilities identified

Successful exploitation on several services

Full system compromise using backdoor services

Evidence collected for each stage

Final report delivered with mitigation recommendations

🛠️ Tools Used

Kali Linux

Nmap (port scanning & service detection)

Nessus ( Vulnerability scanning & assessment)

Enum4linux (SMB enumeration)

Metasploit Framework (automated exploitation)

Linux Utilities (post-exploitation)


🔍 Testing Methodology

1️⃣ Scanning

Performed a full TCP port scan using Nmap:

nmap -sV -sC -p- <192.168.6.136>

2️⃣ Enumeration

Identified and analyzed these services:

Port	Service	Finding
21	FTP	Anonymous Login Enabled
139/445	SMB	Open Shares / Weak Config
1524	ingreslock	Known Backdoor Shell
5900	VNC	Weak / No Authentication
6667	IRC	UnrealIRCd Backdoor
1099	Java RMI	Remote Deserialization Exploit

💥 Exploits Performed

✔ Port 21 – FTP Anonymous Access

Anonymous login successful

Directory listing allowed

Sensitive files accessible

✔ Ports 139/445 – SMB Share Exposure

Enumerated shares using smbclient

Retrieved open share contents

Information disclosure vulnerability

✔ Port 1524 – Ingreslock Backdoor

Direct shell access obtained

Backdoor intentionally placed in Metasploitable2

✔ Port 5900 – VNC Weak Authentication

Weak/no-password protection

Gained full remote desktop access

✔ Port 6667 – UnrealIRCd Backdoor

Remote command execution exploit

Spawned shell using Metasploit module

✔ Port 1099 – Java RMI Deserialization

Vulnerable to RMI deserialization remote code execution

Used Metasploit module to get a shell


🔧 Post‑Exploitation

Performed system‑level enumeration after gaining shell access:

Checked OS information

Enumerated users and groups

Searched for passwords and sensitive files

Tested privilege escalation vectors

Verified network interfaces and routes

Collected evidence (screenshots + outputs)

📸 Evidence

All screenshots are included in:

/Screenshots/
    ├── FTP/
    ├── SMB/
    ├── Backdoor-1524/
    ├── VNC/
    ├── IRC/
    └── RMI-1099/



📑 Final Report

A full penetration testing report including:

Executive Summary

Methodology

Detailed Findings

Screenshots

Exploit Steps

CVSS Scores

Mitigation Recommendations

Report is available inside /Reports/.

👨‍💻 Author

This project was completed by a penetration testing team, where each member contributed to scanning, enumeration, exploitation, documentation, and reporting.