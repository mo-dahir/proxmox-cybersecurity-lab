# Proxmox Enterprise Cybersecurity Lab

## Project Overview

This project documents the design and deployment of an enterprise-style cybersecurity home lab built on a dedicated Proxmox server.

The environment will be used to develop hands-on experience in virtualization, network segmentation, Active Directory, security monitoring, detection engineering, threat hunting, digital forensics, and incident response.

> **Current Status:** Planning and infrastructure setup in progress.

---

## Project Objectives

* Deploy and manage a Type-1 hypervisor using Proxmox VE
* Build segmented enterprise and attack networks
* Configure pfSense firewall rules and network routing
* Deploy Windows Server and Active Directory
* Join Windows endpoints to the domain
* Collect endpoint telemetry with Sysmon
* Ingest and analyze security events using SIEM platforms
* Simulate attacker activity from Kali Linux
* Develop and test security detections
* Perform digital forensic and incident response investigations
* Document troubleshooting, findings, and lessons learned

---

## Hardware

| Component   | Specification         |
| ----------- | --------------------- |
| Workstation | Dell Precision T5810  |
| Processor   | Intel Xeon E5-2680 v4 |
| Memory      | 64 GB DDR4 ECC RAM    |
| Storage     | 960 GB SSD            |
| Hypervisor  | Proxmox VE            |

---

## Planned Technology Stack

### Virtualization and Networking

* Proxmox VE
* Open vSwitch
* pfSense
* Virtual LAN and network segmentation

### Operating Systems

* Windows Server
* Windows 11
* Ubuntu Linux
* Kali Linux
* Kali Purple

### Identity and Endpoint Security

* Active Directory Domain Services
* Group Policy
* Sysmon
* Microsoft Defender

### Security Monitoring and Incident Response

* Elastic Security
* Wazuh
* Splunk
* Velociraptor
* VirusTotal

### Security Testing and Analysis

* Atomic Red Team
* Wireshark
* Nmap
* PowerShell
* Digital forensic tools

---

## Planned Lab Architecture

The environment will include separate virtual networks for enterprise systems, security tools, and attack simulation.

```text
Internet
   |
Home Router
   |
Proxmox Server
   |
pfSense Firewall
   |
   |-- Enterprise Network
   |     |-- Windows Server / Domain Controller
   |     |-- Windows 11 Endpoints
   |
   |-- Security Network
   |     |-- Elastic Security
   |     |-- Wazuh
   |     |-- Velociraptor
   |
   |-- Attack Network
         |-- Kali Linux
         |-- Kali Purple
```

A complete network diagram will be added after the environment is configured.

---

## Project Roadmap

* [ ] Install and configure Proxmox VE
* [ ] Create and configure virtual networks
* [ ] Deploy pfSense
* [ ] Configure firewall rules and segmentation
* [ ] Deploy Windows Server
* [ ] Configure Active Directory
* [ ] Create users, groups, and organizational units
* [ ] Join Windows endpoints to the domain
* [ ] Install and configure Sysmon
* [ ] Deploy Elastic Security
* [ ] Deploy Wazuh
* [ ] Deploy Velociraptor
* [ ] Configure endpoint agents and log ingestion
* [ ] Simulate attack activity
* [ ] Build detection rules and threat-hunting queries
* [ ] Conduct incident-response investigations
* [ ] Publish final architecture and lessons learned

---

## Documentation Plan

This repository will include:

* Architecture diagrams
* Deployment documentation
* Configuration notes
* Screenshots
* Commands and queries
* Detection rules
* Investigation reports
* Troubleshooting records
* Lessons learned
* Security recommendations

---

## Repository Structure

```text
proxmox-cybersecurity-lab/
├── README.md
├── architecture/
├── deployment/
├── networking/
├── active-directory/
├── siem/
├── detections/
├── investigations/
├── screenshots/
├── troubleshooting/
└── lessons-learned/
```

These folders will be added as the project develops.

---

## Safety and Privacy

All testing will be conducted in an isolated lab environment using systems and accounts created specifically for educational purposes.

Public documentation will not include passwords, private IP information that creates unnecessary exposure, API keys, tokens, personal data, or other sensitive information.

---
