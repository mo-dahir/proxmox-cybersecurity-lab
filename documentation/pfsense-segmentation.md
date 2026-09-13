# pfSense Firewall and Network Segmentation

## Purpose

This phase deployed pfSense as the firewall and routing layer for the cybersecurity lab.

pfSense segmented the lab into separate networks for enterprise systems, security tooling, and attack simulation. This design helps create a controlled environment for practicing defensive monitoring, detection engineering, threat hunting, and incident response.

## Scope

This documentation covers the pfSense deployment and network segmentation process, including:

- pfSense virtual machine deployment
- WAN, MCORP, ALLSAFE, and ATTACKLAN interface configuration
- Gateway and subnet assignments
- Firewall rule configuration
- Lab network segmentation
- Isolation of attack simulation activity from defensive and enterprise systems

## Network Zones and IP Layout

pfSense was configured with multiple interfaces to separate the lab into dedicated network zones.

| Interface / Zone | IP Address | Purpose |
|---|---|---|
| WAN | 192.168.1.25 | Upstream connection to the home network |
| MCORP | 10.0.1.1 | Enterprise network for domain services and Windows endpoints |
| ALLSAFE | 10.0.2.1 | Security network for monitoring and defensive tooling |
| ATTACKLAN | 10.0.3.1 | Isolated attack simulation network |

This segmentation separates enterprise systems, defensive security tooling, and attacker infrastructure into distinct networks. The design allows attack simulation and monitoring activity to occur in a controlled environment without mixing all systems into a single flat network.


## Firewall and Segmentation Goals

The firewall configuration supports controlled communication between lab networks while keeping attack simulation activity separate from enterprise and security systems.

The main segmentation goals were:

- Use pfSense as the central routing and firewall layer
- Separate enterprise systems from attack simulation systems
- Place defensive tooling on its own security network
- Control traffic between MCORP, ALLSAFE, and ATTACKLAN
- Support future detection engineering and incident-response scenarios
- Keep lab activity isolated from unnecessary exposure outside the environment

This design allows the lab to simulate enterprise-style network separation while still supporting monitoring, logging, and controlled security testing.

## Configured Lab Networks

The pfSense firewall was configured to support three main internal lab networks.

### MCORP

The MCORP network represents the enterprise environment. This network contains the Windows domain infrastructure and domain-joined endpoints.

Systems in this network include:

- DC01
- Win11-01
- Win11-02

### ALLSAFE

The ALLSAFE network represents the defensive security environment. This network contains monitoring, SIEM/XDR, and DFIR tooling used to observe and investigate activity across the lab.

Systems and tools in this network include:

- Kali Purple running Wazuh
- Ubuntu running Velociraptor

### ATTACKLAN

The ATTACKLAN network represents the isolated attack simulation environment. This network is used for controlled testing and future attack simulation activity.

Systems in this network include:

- Kali Linux

This network design separates enterprise assets, security tools, and attack infrastructure into distinct zones while still allowing controlled routing and monitoring through pfSense.


## Validation

The pfSense configuration was validated by confirming that the firewall interfaces, network zones, and rules were visible in the pfSense web interface.

Validation included:

- Confirming pfSense was accessible through the web interface
- Verifying WAN, MCORP, ALLSAFE, and ATTACKLAN interfaces were assigned
- Confirming each internal lab network had its own gateway IP address
- Reviewing firewall rules for the configured network zones
- Confirming pfSense was positioned as the central routing and segmentation layer for the lab

This validation confirmed that pfSense was ready to support controlled traffic flow between the lab networks and provide segmentation for future monitoring, attack simulation, and incident-response scenarios.


---
