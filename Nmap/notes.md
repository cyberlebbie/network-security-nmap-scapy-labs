# **Lab Activity Summary – Practical Network Scanning & Packet Analysis**

Over the past sessions, I completed a set of hands-on cybersecurity lab activities focused on **network discovery, service enumeration, and packet inspection** using **Nmap** and **Wireshark/Scapy**. These labs were designed to sharpen both technical analysis skills and real-world problem-solving techniques essential for modern cybersecurity roles.


## **What I Learned**

### **1. Network Discovery & Host Enumeration (Nmap)**

I practiced identifying active hosts within a network using:

* `nmap -sn 10.6.6.0/24`
  *A simple yet powerful way to map live devices and understand the network surface before deeper scans.*

### **2. Service and OS Detection**

* `nmap -A -p139,445 10.6.6.23`
  *Helped to enumerate SMB-related ports, reveal services, and estimate OS fingerprints.*

### **3. SMB Share Enumeration**

* `nmap --script smb-enum-shares.nse -p445 10.6.6.23`
  *Useful for uncovering open/shared resources and misconfigurations common in enterprise environments.*

### **4. Packet Capture & Traffic Analysis**

Using **Wireshark** and **Scapy**, I explored:

* How packets flow across the network
* Recognizing suspicious patterns
* Identifying new devices or anomalies
* The importance of correlating logs, traffic spikes, and device behavior

---

## ⚙️ **What Was Challenging**

* Interpreting **noisy or ambiguous packet data** in Wireshark
* Distinguishing normal SMB traffic from potentially risky behavior
* Ensuring I applied the right scan type without overwhelming the target network
* Understanding subtle differences in scan outputs depending on firewall rules or host configurations

These challenges improved my ability to think like an attacker and a defender—balancing curiosity with careful methodology.

---

## **Why These Tools Matter in Real Cybersecurity**

In real-world environments:

🔹 **Nmap** helps identify vulnerabilities before attackers find them.
🔹 **SMB enumeration** is critical for spotting overexposed network shares—an attacker’s favourite entry point.
🔹 **Traffic analysis** helps detect intrusions, malware C2 traffic, or data exfiltration attempts.
🔹 **Combining tools** builds a 360° picture of network health and risk exposure.

These labs reinforced that **practical skills** not just theory are what truly prepare cybersecurity practitioners to secure modern infrastructures.
