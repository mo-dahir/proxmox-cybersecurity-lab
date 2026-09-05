
<img width="2056" height="765" alt="architecture:lab-banner" src="https://github.com/user-attachments/assets/36aa73ce-ee53-410d-929e-8f1609f9361a" />

# Proxmox Enterprise Cybersecurity Lab

## Project Overview

This project documents the design and deployment of an enterprise-style cybersecurity home lab built on a dedicated Proxmox server.

The environment is designed to develop hands-on experience in virtualization, network segmentation, Active Directory, endpoint telemetry, SIEM/XDR monitoring, detection engineering, threat hunting, digital forensics, and incident response.

> **Current Status:** In progress — core infrastructure is deployed, with detection engineering, attack simulation, and incident-response documentation still underway.

---

## Hardware

| Component | Specification |
|---|---|
| System | PowerSpec B947 |
| CPU | AMD Ryzen 7 9800X3D |
| Cores / Threads | 8 cores / 16 logical processors |
| Memory | 64 GB DDR5 |
| Storage | WD Blue SN5100 2TB NVMe SSD |
| Network | Realtek PCIe 2.5GbE Ethernet |
| Hypervisor | Proxmox VE |

## Technology Stack

<details>
<summary><strong>Virtualization and Networking</strong></summary>

<br>

- Proxmox VE
- Open vSwitch
- pfSense
- VLAN-style network segmentation
- Virtual bridges and internal lab networks

</details>

<details>
<summary><strong>Operating Systems</strong></summary>

<br>

- Windows Server 2025
- Windows 11 Enterprise
- Ubuntu Linux
- Kali Linux
- Kali Purple

</details>

<details>
<summary><strong>Identity and Endpoint Security</strong></summary>

<br>

- Active Directory Domain Services
- DNS
- Group Policy
- Sysmon
- Microsoft Defender

</details>

<details>
<summary><strong>Security Monitoring and Incident Response</strong></summary>

<br>

- Wazuh
- Velociraptor
- Elastic Security
- Splunk
- VirusTotal

</details>

<details>
<summary><strong>Security Testing and Analysis</strong></summary>

<br>

- Kali Linux
- Atomic Red Team
- Wireshark
- Nmap
- PowerShell
- Digital forensic tools

</details>

---

## Network Diagram

The diagram below shows the current lab network design, including the Proxmox host, pfSense firewall, segmented lab networks, domain infrastructure, security tooling, and attack simulation network.

<img width="1448" height="1086" alt="CyberLab Network Diagram" src="https://github.com/user-attachments/assets/0fca246d-e6be-4907-b5c0-5dac78838217" />


---
## Current Lab Systems

| System | Network | IP Address | Role |
|---|---|---|---|
| Proxmox Host | Management | 192.168.1.240 | Hypervisor hosting the lab environment |
| pfSense | WAN / MCORP / ALLSAFE / ATTACKLAN | 192.168.1.25 / 10.0.1.1 / 10.0.2.1 / 10.0.3.1 | Firewall, routing, and segmentation |
| DC01 | MCORP | 10.0.1.2 | Domain controller, Active Directory, and DNS |
| Win11-01 | MCORP | 10.0.1.12 | Domain-joined Windows endpoint |
| Win11-02 | MCORP | 10.0.1.13 | Domain-joined Windows endpoint |
| Kali Linux | ATTACKLAN | 10.0.3.2 | Attack simulation workstation |
| Kali Purple | ALLSAFE | 10.0.2.2 | Defensive security workstation running Wazuh |
| Ubuntu | ALLSAFE | 10.0.2.3 | Server running Velociraptor |

---

## Project Roadmap

<details>
<summary><strong>Completed</strong></summary>

<br>

- [x] Install and configure Proxmox VE
- [x] Upload required ISO files
- [x] Deploy Windows 11 endpoint VMs
- [x] Deploy Windows Server
- [x] Deploy Kali Linux
- [x] Deploy Kali Purple
- [x] Deploy Ubuntu server
- [x] Deploy pfSense firewall
- [x] Configure pfSense interfaces
- [x] Configure pfSense firewall rules and segmentation
- [x] Install and configure Open vSwitch
- [x] Configure Active Directory Domain Services
- [x] Create Active Directory users, groups, and Group Policy
- [x] Join Windows endpoints to the domain
- [x] Install Sysmon on Windows systems
- [x] Deploy Wazuh and enroll Windows agents
- [x] Deploy Velociraptor and enroll Windows clients

</details>

### In Progress / Next Steps

- [ ] Configure additional endpoint logging
- [ ] Configure Wazuh dashboards, alerts, and detection rules
- [ ] Configure Velociraptor hunts and artifact collection
- [ ] Simulate attack activity using Kali Linux and Atomic Red Team
- [ ] Build detection rules and threat-hunting queries
- [ ] Conduct incident-response investigations
- [ ] Document findings, screenshots, troubleshooting, and lessons learned
- [ ] Publish final architecture and project summary

---

## Documentation Plan

This repository will document the lab build and security workflow through focused technical notes, screenshots, and investigation writeups.

### Planned Documentation Areas

- Proxmox host setup and VM deployment
- pfSense interface configuration and firewall segmentation
- Open vSwitch network configuration
- Active Directory domain setup and endpoint joins
- Sysmon deployment and Windows telemetry validation
- Wazuh agent enrollment, dashboards, alerts, and detections
- Velociraptor client enrollment, hunts, and artifact collection
- Attack simulation and detection engineering
- Incident-response investigations and lessons learned

---

## Portfolio Evidence

This project will be supported by screenshots, configuration notes, detection logic, investigation writeups, and lessons learned that demonstrate the lab build and security workflow.

Evidence will focus on:

- Proxmox virtualization and VM deployment
- pfSense firewall routing and segmentation
- Open vSwitch network configuration
- Active Directory domain services
- Windows endpoint telemetry with Sysmon
- Wazuh monitoring and alerting
- Velociraptor endpoint DFIR and threat hunting
- Attack simulation, detection engineering, and incident response

---

## Safety and Privacy

All testing will be conducted in an isolated lab environment using systems and accounts created specifically for educational purposes.

Public documentation will not include passwords, private IP information that creates unnecessary exposure, API keys, tokens, personal data, or other sensitive information.

---
