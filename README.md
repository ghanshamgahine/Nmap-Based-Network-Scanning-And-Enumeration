# Nmap-Based Network Scanning And Enumeration

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

# 8. Operating System Detection

Command:

`nmap -O 192.168.157.129`

Purpose: To estimate the target operating system.
<img width="802" height="682" alt="nmap -o detection" src="https://github.com/user-attachments/assets/7dffcca7-2c12-4163-ad34-55fa3567110f" />
<img width="691" height="163" alt="-o detection" src="https://github.com/user-attachments/assets/456c10c9-6345-4254-ae98-486215a27415" />

# 9. Vulnerability Scanning Using NSE

Command:

`nmap --script vuln 192.168.157.129 -T4`

Purpose: To check for potential security vulnerabilities.
<img width="1085" height="737" alt="nmap vuln 1" src="https://github.com/user-attachments/assets/a47e531f-7a1c-46dc-be30-84ddd602406f" />
<img width="985" height="898" alt="vuln 2" src="https://github.com/user-attachments/assets/21ca2105-091e-47d4-af44-7a6cf944f419" />
<img width="957" height="903" alt="vuln 3" src="https://github.com/user-attachments/assets/45c7d8db-bbfa-4c1f-9d05-501ea66443ee" />
<img width="1191" height="902" alt="vuln 4" src="https://github.com/user-attachments/assets/4be1fa04-afc9-4035-9605-cd8599432ff6" />
<img width="1113" height="887" alt="vuln 5" src="https://github.com/user-attachments/assets/8e7258aa-4ae4-4379-bdcc-859ced67ddfc" />
<img width="1208" height="902" alt="vuln 6" src="https://github.com/user-attachments/assets/ec30e46c-e6ee-412f-8667-4cdbf356d6fb" />
<img width="675" height="895" alt="vuln 7" src="https://github.com/user-attachments/assets/095f0f9d-c725-483e-a86a-05b476c6d0e4" />
<img width="892" height="780" alt="vuln 8" src="https://github.com/user-attachments/assets/8dafb19d-d332-4664-8ce1-2b4dce2cb79a" />
<img width="1062" height="903" alt="vuln 9" src="https://github.com/user-attachments/assets/04caaffe-130b-41cf-ad12-b60d85c3bbab" />
<img width="1091" height="357" alt="vuln 10" src="https://github.com/user-attachments/assets/837ca831-f4f9-4b7f-b519-8c41036fdfc1" />
<img width="667" height="157" alt="vuln scan" src="https://github.com/user-attachments/assets/869497e3-98e3-48bb-8917-2794f948246a" />

# 10. Aggressive Scanning

Command:

`nmap -A 192.168.157.129 -T4`

Purpose: To collect detailed information about ports, services, versions, and the operating system.
<img width="1313" height="750" alt="nmap aggressive scan" src="https://github.com/user-attachments/assets/d8bf40d2-3198-491b-964a-db9f5498871b" />
<img width="1353" height="905" alt="-aG scan 2" src="https://github.com/user-attachments/assets/02af0f70-06db-4351-b53c-3199f88cd720" />
<img width="1310" height="885" alt="-aG scan 3" src="https://github.com/user-attachments/assets/11606dfa-1e09-40ec-a6dc-d62824b7ddc8" />
<img width="1171" height="653" alt="-aG scan 4" src="https://github.com/user-attachments/assets/22c601a0-a5d0-486e-8974-3c1fb35b4a0e" />
<img width="705" height="152" alt="nmap agresivescan txt" src="https://github.com/user-attachments/assets/985530b6-85fe-4219-bbc5-488554b198f9" />

# 11. Scan Summary and Analysis

| Scan Type | Command | Purpose |
|---|---|---|
| Host Discovery | `nmap -sn 192.168.157.129` | Check host availability |
| Port Scanning | `nmap -p- 192.168.157.129` | Find open TCP ports |
| Service Detection | `nmap -sV 192.168.157.129` | Detect services and versions |
| OS Detection | `nmap -O 192.168.157.129` | Estimate operating system |
| Vulnerability Scan | `nmap --script vuln 192.168.157.129 -T4` | Check potential vulnerabilities |
| Aggressive Scan | `nmap -A 192.168.157.129 -T4` | Gather detailed information |

# 12. Results and Findings

- Host discovery checks whether the target is reachable.
- Port scanning identifies accessible ports.
- Service detection attempts to identify running software.
- OS detection estimates the target operating system.
- NSE scripts check for potential vulnerabilities.
- Aggressive scanning gathers additional target information.

Actual findings should be based on the terminal outputs.

# 13. Conclusion

This project provided practical experience with Nmap network scanning and enumeration using Kali Linux and Metasploitable 2 in an authorized lab environment.

# 14. Disclaimer

This project is for educational purposes only. Scanning should be performed only on systems owned by the user or with explicit authorization.# Nmap 
















