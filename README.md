# Cybersecurity Homelab in VMware

## Overview
This project showcases a fully virtualized cybersecurity homelab built using VMware Workstation. The lab is designed to simulate real-world attack and defense scenarios, combining vulnerable targets, attacker tools, firewall segmentation, and log analysis. It serves as a foundation for developing and documenting skills in penetration testing, intrusion detection, and threat analysis.

## Lab Components

| Machine              | Role                           | Tools / Purpose                                  |
|----------------------|--------------------------------|--------------------------------------------------|
| Kali Linux           | Attacker Box                   | Metasploit, Nmap, Burp Suite, Hydra              |
| Metasploitable 2     | Vulnerable Target (Linux)      | Legacy exploits, remote service vulnerabilities  |
| Windows 10 VM        | Vulnerable Target (Windows)    | Manual attack testing, simulated threats         |
| Security Onion       | IDS/Log Collector              | Suricata, Zeek, Wazuh, Kibana, Elasticsearch     |
| pfSense              | Virtual Firewall / Router      | Network segmentation, traffic filtering          |

## Project Goals

- Simulate attack scenarios and validate detection workflows.
- Experiment with intrusion detection tools like Zeek, Suricata, and Wazuh.
- Create dashboards and alerts for threat visibility in Kibana and Splunk.
- Showcase traffic segmentation and firewalling with pfSense.
- Document attack vectors, detection methods, and incident response steps.

## Setup Instructions

1. Install VMware Workstation.
2. Deploy each VM using appropriate ISO files or prebuilt images.
3. Configure VMware networking for:
   - Isolated networks (Host-only for attack/testing).
   - Shared segments for monitoring traffic.
4. Set up pfSense to manage traffic between segments.
5. Configure Security Onion with sniffing interfaces tied to traffic flows.
6. Launch attack simulations from Kali using tools like Metasploit and Nmap.
7. Monitor alerts and logs via Security Onion’s Kibana and Elasticsearch dashboards.

## Monitoring and Analysis

- **Security Onion**:
  - Suricata: Signature-based detection.
  - Zeek: Protocol-level logging and behavior analysis.
  - Wazuh: Host-based detection and compliance.

## Sample Attack Scenarios

- SSH brute-force on Metasploitable.
- SMB enumeration and exploitation on Windows VM.
- Reverse shell delivery and C2 traffic monitoring.
