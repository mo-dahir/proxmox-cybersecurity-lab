# Active Directory Domain Services

## Purpose

This phase built a centralized Windows identity environment for the cybersecurity lab using Active Directory Domain Services.

DC01 was configured as the domain controller for the `MCorp.local` domain, providing centralized authentication, DNS, user and computer management, and Group Policy capabilities for the Windows environment.

## Scope

This documentation covers the Active Directory configuration process, including:

- Windows Server domain controller configuration
- Active Directory Domain Services deployment
- DNS configuration
- `MCorp.local` domain creation
- Active Directory user and group creation
- Group Policy configuration
- Validation of the domain environment

## Domain Services Configuration

Windows Server was configured as the domain controller for the lab environment.

The server was configured with the following core services:

- Active Directory Domain Services
- DNS
- Active Directory Certificate Services
- File and Storage Services

The domain was created as `MCorp.local`.

DC01 was assigned the IP address `10.0.1.2` and provides domain and DNS services for the Windows systems on the MCORP network.

This configuration established the centralized identity and authentication foundation required for domain-joined endpoints, Group Policy, and future security monitoring activities.

---

---
