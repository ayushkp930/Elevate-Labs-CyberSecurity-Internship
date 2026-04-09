# Task 01: Scan Local Network For Open Ports

📌 Executive Summary
As part of the Elevate Labs Cyber Security Residency, this project focuses on the first phase of the Cyber Attack Lifecycle: Reconnaissance. The objective was to perform a network scan on a local subnet to identify active hosts and open services using Nmap and Wireshark.

🛠️ Technical Specifications
Operating System: Kali Linux (GNOME Desktop Environment)

Primary Tool: Nmap 7.98

Packet Analyzer: Wireshark

Target Subnet: 10.202.66.0/24

Scan Methodology: TCP SYN (Stealth) Scan

🚀 Methodology & Execution
The scan was executed using a "Half-Open" stealth technique to minimize detection while ensuring high accuracy.

Command Used:

Bash
sudo nmap -sS -v -T4 10.202.66.0/24 -oN task1_report.txt
Nmap Flags Breakdown:
-sS: TCP SYN Stealth scan to identify open ports without completing the 3-way handshake.

-v: Enabled verbose mode for real-time visual feedback.

-T4: Set timing to 'Aggressive' for faster execution on a reliable network.

-oN: Logged output to a structured text file for documentation.

🔍 Key Findings
The scan successfully identified 3 active hosts on the network:

Host 10.202.66.212

Status: Up

Open Port: 53/tcp (Service: Domain/DNS)

Note: Active DNS resolution service detected.

Host 10.202.66.233 (Oppo Mobile Device)

Status: Up

Filtered Port: 5060/tcp (Service: SIP)

Note: Security filtering detected on VoIP-related services.

Local Host 10.202.66.18 (Scanning Machine)

Status: Up

Note: All 1000 ports appeared filtered/ignored due to local firewall settings.

📸 Visual Evidence (Proof of Work)
1. Nmap Command Execution
Initial deployment of the stealth scan on the subnet.

2. Scan Results Summary
Discovery of active hosts and identified open/filtered ports.

3. Wireshark Packet Analysis
Confirmation of the SYN ➔ SYN/ACK ➔ RST flow, validating the stealth scan.

🧠 Security Analysis & Interview Questions
1. What is an "Open Port"?
An open port is a communication channel actively accepting incoming traffic. Port 53 was found open on .212, indicating an active service ready for connection.

2. How does a TCP SYN Scan work?
It is a "Half-Open" scan. Nmap sends a SYN packet; if a SYN/ACK is received, the port is open. Nmap then sends a RST packet instead of an ACK, closing the connection before it's fully established to remain stealthy.

3. Risks of Open Port 53 (DNS)?
Open DNS ports can be exploited for DNS Cache Poisoning, DNS Amplification DDoS attacks, or Zone Transfers to map internal networks.

4. What does "Filtered" mean for Port 5060?
It means a firewall or packet filter is preventing Nmap from determining if the port is open or closed by dropping the probes.

5. Why are ports on the local host (10.202.66.18) filtered?
This is due to the local OS firewall protecting the machine from unauthorized external probes.

6. General risks of unnecessary open ports?
They increase the "Attack Surface," allowing hackers to find entry points for exploitation, unauthorized access, or malware injection.

7. How to secure these ports?
Implement strict firewall rules, disable unused services, and ensure all active services are regularly patched and hardened.

8. Importance of Network Reconnaissance?
Reconnaissance is the first step of the Cyber Kill Chain. Identifying exposed services allows security professionals to proactively fix vulnerabilities before an attacker can exploit them.

Internship: Elevate Labs
Intern: Ayush Kumar Patel
