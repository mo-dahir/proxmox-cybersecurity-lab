# Proxmox Host Setup and VM Deployment

## Purpose

This phase built the virtualization foundation for the cybersecurity lab using Proxmox VE on a dedicated physical server.

Proxmox provides the hypervisor layer that hosts the lab’s Windows, Linux, firewall, security monitoring, and attack simulation systems.

## Scope

This documentation covers the initial Proxmox setup and virtual machine deployment process, including:

- Proxmox VE host configuration
- ISO image uploads
- Windows endpoint VM deployment
- Windows Server VM deployment
- Kali Linux and Kali Purple VM deployment
- Ubuntu Server VM deployment
- Initial lab inventory validation


## Lab Host Details

| Component | Configuration |
|---|---|
| Hostname | pve01 |
| Hypervisor | Proxmox VE |
| Management IP | 192.168.1.240 |
| Physical System | PowerSpec B947 |
| CPU | AMD Ryzen 7 9800X3D |
| Memory | 64 GB DDR5 |
| Storage | 2 TB NVMe SSD |
| Network Adapter | Realtek PCIe 2.5GbE Ethernet |

This host provides the compute, memory, storage, and networking resources required to run the lab’s virtualized infrastructure.


## ISO Image Uploads

Required installation ISO files were uploaded to the Proxmox storage before VM deployment.

The uploaded ISO images supported deployment of:

- Windows 11 endpoints
- Windows Server
- pfSense firewall
- Kali Linux
- Kali Purple
- Ubuntu Server
- VirtIO drivers for Windows virtual machines

This step ensured that all required operating systems and drivers were available directly from Proxmox during VM creation and installation.


## Virtual Machine Deployment

Multiple virtual machines were created in Proxmox to support the lab environment.

The initial VM deployment included:

| Virtual Machine | Purpose |
|---|---|
| pfSense | Firewall, routing, and network segmentation |
| DC01 | Windows Server domain controller and DNS server |
| Win11-01 | Domain-joined Windows endpoint |
| Win11-02 | Domain-joined Windows endpoint |
| Kali Linux | Attack simulation and security testing workstation |
| Kali Purple | Defensive security workstation running Wazuh |
| Ubuntu | Server platform running Velociraptor |

Each VM was deployed with resources appropriate for its role in the lab. Windows systems were configured with VirtIO drivers where needed to support virtualized storage and networking.


## Validation

The Proxmox environment was validated by confirming that the host was accessible through the web interface and that the deployed virtual machines were visible in the Proxmox inventory.

Validation included:

- Confirming Proxmox web management access
- Verifying uploaded ISO images were available in storage
- Confirming core virtual machines were created
- Confirming Windows and Linux systems successfully booted
- Confirming virtual networking was available for lab systems
- Confirming the environment was ready for firewall, domain, endpoint, and security tooling configuration

This validation confirmed that the core virtualization layer was ready to support the rest of the cybersecurity lab.


---
