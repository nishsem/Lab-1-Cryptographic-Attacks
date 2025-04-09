📊 Network Protocol Vulnerability Lab

Overview

This project is a lab-based security assessment of common network protocols (FTP, TELNET, SSH, HTTP) focused on identifying vulnerabilities through brute force attacks and analyzing network traffic. The goal is to demonstrate protocol weaknesses and recommend secure alternatives.

💡 Objectives

Enumerate network services and discover usernames.

Perform brute force attacks using tools like Hydra and Burp Suite.

Sniff network traffic to detect plaintext vs. encrypted data.

Analyze weaknesses in each protocol.

Propose mitigation strategies and secure alternatives.

⚖️ Tools Used
### 🛰️ Nmap  
<img src="https://nmap.org/images/logo.png" width="150"/>

### 🐍 Hydra  
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/37/Hydra_logo.png/320px-Hydra_logo.png" width="150"/>

### 🧪 Burp Suite  
<img src="https://raw.githubusercontent.com/PortSwigger/portswigger-images/main/burp-logo-orange.png" width="150"/>

### 🧬 Wireshark  
<img src="https://upload.wikimedia.org/wikipedia/en/6/6e/Wireshark_icon.png" width="120"/>

💡 Lab Tasks Summary

1. Service Enumeration

Scanned target VM for open ports: FTP (21), SSH (22), TELNET (23), HTTP (80).

Discovered usernames via enum4linux and manual login attempts.

2. Brute Force Attacks

Used Hydra to brute force FTP, TELNET, and SSH.

Used Burp Suite Intruder to brute force an HTTP login form.

Identified weak credentials and gained access.

3. Packet Sniffing

Captured login sessions with Wireshark.

Verified that FTP, TELNET, and HTTP transmit data in plaintext.

Confirmed that SSH encrypts all data.

4. Issues and Resolutions

Rate limiting was encountered; resolved using delays.

Burp Community Edition has limitations; adapted strategy accordingly.

5. Mitigation Strategies

| Protocol | Vulnerability      | Secure Alternative      |
|----------|--------------------|--------------------------|
| FTP      | Plaintext login    | SFTP / FTPS              |
| TELNET   | No encryption      | SSH                      |
| HTTP     | Exposes credentials| HTTPS                    |
| SSH      | Brute force risk   | Fail2Ban, SSH keys       |

