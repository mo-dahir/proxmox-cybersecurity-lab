# Windows Server Deployment

## Purpose

This phase deployed Windows Server in Proxmox and prepared it to serve as the centralized server platform for the lab environment.

The Windows Server system was configured as the foundation for future Active Directory, DNS, domain management, and security monitoring activities.

## Scope

This documentation covers the initial Windows Server deployment process, including:

- Windows Server virtual machine creation
- Initial operating system installation
- Virtual hardware configuration
- Hostname and network configuration
- Server connectivity validation
- Preparation for Active Directory Domain Services
- Preparation for Sysmon, Wazuh, and Velociraptor integration

## Server Configuration and Role Preparation

After deploying Windows Server in Proxmox, the system was configured as the lab’s primary Windows server.

Initial configuration included:

- Verifying successful Windows Server installation
- Confirming hostname and logged-in user information
- Configuring network connectivity on the MCORP network
- Assigning the server a stable IP configuration
- Verifying communication with the lab network
- Preparing the system for Active Directory Domain Services and DNS
- Preparing the server for endpoint monitoring and security tooling

This configuration established the server foundation required for the later Active Directory, domain management, telemetry, and security monitoring phases of the lab.

## Windows Server Validation

The Windows Server deployment was validated after installation and initial configuration to confirm that the system was operating correctly within the lab environment.

Validation included:

- Confirming Windows Server successfully booted
- Verifying hostname and logged-in user information
- Confirming the expected IP configuration
- Verifying network connectivity on the MCORP network
- Confirming the server was ready for Active Directory Domain Services and DNS configuration
- Preparing the server for Sysmon, Wazuh, and Velociraptor integration

This validation confirmed that the Windows Server system was stable and ready to support the identity, monitoring, and security functions required by the broader lab.

## Skills Demonstrated

This phase demonstrates Windows Server deployment and infrastructure skills, including:

- Windows Server virtual machine deployment
- Virtual hardware configuration in Proxmox
- Windows Server installation and initial configuration
- Hostname and IP configuration validation
- Server network connectivity verification
- Preparation for Active Directory Domain Services and DNS
- Preparation for endpoint telemetry and security monitoring
- Integration of Windows Server into a segmented lab environment

These skills support the broader cybersecurity lab by establishing the server platform used for centralized identity, domain services, endpoint monitoring, and security operations.


---
