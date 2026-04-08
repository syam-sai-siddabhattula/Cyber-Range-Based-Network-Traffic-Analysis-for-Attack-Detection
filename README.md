# Cyber Range-Based Network Traffic Analysis for Attack Detection

## Overview
This project demonstrates a cyber range environment designed to simulate real-world enterprise network conditions for analyzing external and internal cyber attacks. The objective is to study network traffic behavior and detect anomalies using behavior-based and threshold-driven techniques.

The environment enables controlled simulation of:
- External intrusion attempts
- Internal lateral movement
- Network traffic capture and analysis

---

## Architecture
The cyber range is built using a segmented network model consisting of:

- **WAN (External Network)**
- **DMZ (Public-facing services)**
- **OPS (Operations/Monitoring zone)**
- **USER/DATA Zone (Internal systems)**

All inter-zone traffic is routed through an **OPNsense firewall**, enabling:
- Traffic monitoring
- Packet capture
- Attack analysis

---

## Technologies Used
- **Proxmox VE** – Virtualization platform
- **OPNsense Firewall** – Network routing and security
- **Kali Linux** – Attack simulation (external & internal)
- **Ubuntu Servers** – Web server, monitoring, and services
- **Wireshark / PCAP Analysis** – Traffic analysis
- **Python (Scapy)** – Packet-level analysis

---

## Attack Scenarios

### External Attack
- Source: Kali Linux (WAN)
- Target: Web server (DMZ)
- Activities:
  - Port scanning
  - HTTP requests
  - Brute-force attempts
- Output: `external.pcap`

### Internal Attack
- Source: Compromised internal host
- Target: Internal systems
- Activities:
  - Lateral movement
  - SMB / RDP access attempts
- Output: `internal.pcap`

---

## Detection Approach
The system uses:
- **Behavior-based analysis**
- **Threshold-based anomaly detection**

Key observations:
- External attacks → High-intensity traffic spikes
- Internal attacks → Gradual and structured deviations

---

## Access the Cyber Range

🔗 **Proxmox Interface:**  
https://proxmox.ears-up-cybersec.com/

### Credentials (View Only)
