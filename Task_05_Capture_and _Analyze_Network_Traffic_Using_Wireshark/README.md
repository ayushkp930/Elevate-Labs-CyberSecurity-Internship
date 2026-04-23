# Elevate Labs Cyber Security Internship - Task 5
## Capture and Analyze Network Traffic Using Wireshark

### 📌 Objective
To capture live network traffic, analyze different protocols, and understand the flow of data packets using Wireshark on Kali Linux.

---

### 🛠️ Environment Details
- **OS:** Kali Linux (6.19.11-amd64)
- **Processor:** 12th Gen Intel(R) Core(TM) i3-1215U
- **Tool:** Wireshark 4.6.4

---

### 📊 Protocols Identified
During the session, I identified and analyzed the following protocols:
1. **TCP (Transmission Control Protocol):** Connection-oriented traffic for reliable data transfer.
2. **DNS (Domain Name System):** Resolving domain names to IP addresses.
3. **TLS/HTTP:** Encrypted and plain web traffic.

---

### 📸 Task Screenshots

#### 1. Main Traffic Capture
![Main Capture](screenshots/01_capture_main.png)
*Description: Capturing live traffic on the wlan0 interface.*

#### 2. Protocol Filtering (DNS/TCP)
![DNS Filter](screenshots/02_dns_filter.jpg)
*Description: Applying filters to isolate specific protocol packets.*

#### 3. Detailed Packet Analysis
![Analysis](screenshots/03_tcp_filter.jpg)
*Description: Inspecting the 3-way handshake and packet headers.*

---

### ❓ Interview Questions & Answers

**1. What is Wireshark used for?**
It is a network protocol analyzer used to capture and interactively browse the traffic running on a computer network.

**2. What is a packet?**
A packet is a small segment of a larger message. Data sent over a network is broken into packets to be transmitted efficiently.

**3. How to filter packets in Wireshark?**
We use the 'Display Filter' bar. For example, typing `dns`, `tcp`, or `ip.addr == 192.168.1.1` isolates specific traffic.

**4. What is the difference between TCP and UDP?**
TCP is connection-oriented and reliable (3-way handshake), while UDP is connectionless and faster but doesn't guarantee delivery.

**5. What is a DNS query packet?**
It's a request sent by a client to a DNS server to resolve a hostname (like google.com) into an IP address.

**6. How can packet capture help in troubleshooting?**
It allows us to see exactly what is happening on the wire, helping identify latency, dropped packets, or unauthorized access.

**7. What is a protocol?**
A set of rules that governs how data is exchanged between devices on a network.

**8. Can Wireshark decrypt encrypted traffic?**
Yes, but only if you have the session keys or the private keys of the server (e.g., SSL/TLS decryption).

---

### 📂 Files Included
- **Capture File:** [network_traffic.pcapng](capture/network_traffic.pcapng)
- **Report:** This README serves as the summary report.

**Submitted by:** Ayush Kumar Patel
