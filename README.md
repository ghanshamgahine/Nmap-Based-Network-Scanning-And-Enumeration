# Nmap Network Scanning and Enumeration Lab

# 1. Introduction

Nmap (Network Mapper) is an open-source tool used for network discovery and security auditing. It helps identify active hosts, open ports, running services, service versions, and operating systems.

This project demonstrates different Nmap scanning techniques using Kali Linux and Metasploitable 2 in a virtual lab environment. It includes Host Discovery, Port Scanning, Service and Version Detection, OS Detection, Vulnerability Scanning, and Aggressive Scanning.

The main purpose of this project is to gain practical knowledge of network scanning, understand exposed services, and learn basic security assessment techniques in an authorized environment.

# 2. Objectives

- To understand Nmap scanning techniques.
- To discover active hosts.
- To identify open ports.
- To detect services and versions.
- To identify the operating system.
- To perform vulnerability scanning.
- To analyze scan results.

# 3. Tools and Technologies Used

| Tool | Purpose |
|---|---|
| Kali Linux | Scanning machine |
| Nmap | Network scanning |
| Metasploitable 2 | Lab target |
| VMware | Virtual machine environment |
| Terminal | Execute commands |

# 4. Lab Setup and Target Identification

Target IP Address: `192.168.157.129

Command:
ifconfig
<img width="1713" height="816" alt="metasploitable ifconfig" src="https://github.com/user-attachments/assets/4cef6911-a45d-483a-920f-19b5a248d635" />


# 5. Host Discovery Scan

Command:

`nmap -sn 192.168.157.129`

Purpose: To check whether the target host is active.
<img width="1057" height="537" alt="nmap hostdiscovery" src="https://github.com/user-attachments/assets/fb610865-18c0-49d2-9375-60d50a6f8dd3" />

# 6. Port Scanning

Command:

`nmap -p- 192.168.157.129`

Purpose: To scan all TCP ports and identify open ports.

| Port | Common Service |
|---|---|
| 21 | FTP |
| 22 | SSH |
| 23 | Telnet |
| 25 | SMTP |
| 80 | HTTP |
| 445 | SMB |
| 3306 | MySQL |

These are common examples; actual results may differ.
<img width="912" height="813" alt="port scan" src="https://github.com/user-attachments/assets/db15ecf0-35a9-4505-a8ab-e3c271909ddd" />

# 7. Service and Version Detection

Command:

`nmap -sV 192.168.157.129`

Purpose: To identify running services and their versions.

| Option | Meaning |
|---|---|
| `-sV` | Service and version detection |
<img width="1277" height="805" alt="nmap -sv version" src="https://github.com/user-attachments/assets/7b3d11c8-47a1-45af-889c-0588cbc6b878" />
<img width="827" height="182" alt="-sv version" src="https://github.com/user-attachments/assets/66c2d16b-ea1d-458a-a944-9b82abad19e7" />

