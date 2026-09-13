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


---
