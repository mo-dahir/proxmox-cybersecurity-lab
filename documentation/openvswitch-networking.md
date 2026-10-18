# Open vSwitch Network Configuration

## Purpose

This phase configured Open vSwitch in Proxmox to support the lab’s segmented virtual networking design.

Open vSwitch provides the virtual switching layer that organizes and separates traffic between the enterprise, defensive security, and attack simulation networks.

## Scope

This documentation covers the Open vSwitch configuration process, including:

- Open vSwitch installation and configuration
- Proxmox OVS bridge setup
- Internal network interface configuration
- VLAN-style network segmentation
- Validation of bridge and port assignments

## Open vSwitch Network Layout

Open vSwitch was configured in Proxmox using an OVS bridge and internal ports to support the segmented lab networks.

The configuration includes:

| Component | Configuration | Purpose |
|---|---|---|
| OVS Bridge | vmbr1 | Virtual switching layer for internal lab traffic |
| Internal Port | vlan10 | Supports the MCORP network |
| Internal Port | vlan20 | Supports the ALLSAFE network |
| Internal Port | vlan30 | Supports the ATTACKLAN network |

The internal ports were assigned VLAN tags to separate traffic between the enterprise, defensive security, and attack simulation networks while allowing Proxmox to host the virtualized environment on a shared switching layer.

---
