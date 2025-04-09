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
![nmap](https://nmap.org/images/logo.png)  
- Network scanning

### 🐍 Hydra  
![Hydra](https://upload.wikimedia.org/wikipedia/commons/3/37/Hydra_logo.png)  
- Brute force tool

### 🐙 Medusa  
![Medusa](https://raw.githubusercontent.com/jmk-foofus/medusa/master/doc/medusa-logo.png)  
- Brute force alternative

### 🧪 Burp Suite  
![Burp Suite](https://portswigger.net/cms/images/03/60/3035-featured-370x201.png)  
- HTTP login brute forcing

### 🧬 Wireshark  
![Wireshark](https://upload.wikimedia.org/wikipedia/en/6/6e/Wireshark_icon.png)  
- Network packet analysis

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

