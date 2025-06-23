# Elevate_Labs_Cybersecurity_Task_01
# CYBER SECURITY INTERNSHIP - TASK 1  
**Network Port Scanning with Nmap**  

## What I Did  
1. I scanned my local network (`192.168.x.0/24`) using Nmap's TCP SYN scan (`-sS`) to find open ports.  
2. I analyzed the results to identify devices like the router, laptops, and IoT devices along with their exposed services.  
3. I researched common vulnerabilities linked to open ports, such as SSH brute-forcing and HTTP data leaks.  
4. (Optional) I captured network traffic during the scan with Wireshark to see how Nmap interacts with target ports.  

## Tools Used  
- **Nmap**: For port scanning (`nmap -sS [IP]`).  
- **Wireshark**: To check scan traffic (optional).  
- **Command Line**: To find my local IP range (`ipconfig`/`ifconfig`).  

## What I Learned  
- **Open Ports**: They serve as gateways for communication, and if misconfigured, they can expose devices to attacks, such as port 22 for SSH.  
- **TCP SYN Scan**: This is a stealthy scan that avoids establishing full TCP connections and is useful for evading basic detection.  
- **Network Security**: Services like HTTP (port 80) send data in plaintext, while HTTPS (port 443) offers more safety.  
- **Firewalls**: They can block unnecessary ports to lower the attack surface, such as closing port 23 for Telnet if it's not in use.  

## Interesting Findings  
- **Router Exposure**: My router (`192.168.1.1`) had port 80 (HTTP) open, exposing the admin panel to the local network.  
- **Unexpected Device**: I discovered a smart TV (`192.168.1.105`) with port 8008 open for the Google Cast service.  
- **Security Risk**: A laptop had port 445 (SMB) open, which could be used for ransomware attacks.  

## Interview Questions (Brief Answers)  
1. **Open Port**: This is a listening service on a device, such as port 80 for web servers.  
2. **TCP SYN Scan**: It sends SYN packets and analyzes responses to map open ports without completing connections.  
3. **Risks**: They include unauthorized access, data leaks, and malware infections, such as EternalBlue via SMB.  
4. **TCP vs UDP**: TCP scans, like SYN scans, are reliable, while UDP scans (`-sU`) are slower but essential for services like DNS and DHCP.  

---

**Repo Contents**:  
- `scan_results.txt`: Nmap output.  
- `screenshots/`: Wireshark/Nmap visuals (if taken).  
