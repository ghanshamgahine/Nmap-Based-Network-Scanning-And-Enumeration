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

