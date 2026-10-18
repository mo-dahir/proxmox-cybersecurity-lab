# Windows Domain Join and Endpoint Integration

## Purpose

This phase integrated the Windows 11 endpoints into the `MCorp.local` Active Directory domain.

Joining the endpoints to the domain allows centralized authentication, policy management, DNS integration, and security monitoring across the Windows environment.

## Scope

This documentation covers the domain join process for the Windows endpoints, including:

- Windows endpoint network configuration
- DNS configuration using DC01
- Joining Win11-01 and Win11-02 to the `MCorp.local` domain
- Domain user authentication
- Validation of domain membership
- Verification of computer objects in Active Directory

## Endpoint Network and DNS Configuration

Before joining the Windows endpoints to the domain, each system was configured to use the MCORP network and DC01 for DNS resolution.

| Endpoint | IP Address | Default Gateway | DNS Server |
|---|---|---|---|
| Win11-01 | 10.0.1.12 | 10.0.1.1 | 10.0.1.2 |
| Win11-02 | 10.0.1.13 | 10.0.1.1 | 10.0.1.2 |

DC01, located at `10.0.1.2`, provides DNS and Active Directory services for the `MCorp.local` domain.

Using the domain controller as the DNS server lets Windows endpoints locate Active Directory services and authenticate to the domain.

## Domain Join and Authentication

Both Windows 11 endpoints were joined to the `MCorp.local` Active Directory domain.

The domain join process included:

- Configuring each endpoint to use DC01 for DNS
- Joining Win11-01 and Win11-02 to the `MCorp.local` domain
- Restarting the endpoints after the domain join
- Signing in with domain user accounts
- Verifying domain membership from the Windows systems

Domain authentication was successfully validated using the following domain users:

- `MCORP\astark`
- `MCORP\jsnow`

This confirmed that the Windows endpoints were successfully integrated into the centralized Active Directory environment.

## Validation

The domain join configuration was validated from both the Windows endpoints and Active Directory.

Validation included:

- Confirming Win11-01 and Win11-02 were joined to the `MCorp.local` domain
- Verifying each endpoint received the expected MCORP network configuration
- Confirming DC01 was being used for DNS resolution
- Signing in with domain user accounts
- Verifying the `MCORP.LOCAL` domain was recognized by the endpoints
- Confirming both Windows systems appeared as computer objects in Active Directory

This validation confirmed that the Windows endpoints integrated successfully into the domain and were ready for centralized policy management, telemetry collection, and security monitoring.

## Skills Demonstrated

This phase demonstrates Windows endpoint and identity integration skills, including:

- Windows domain join configuration
- Active Directory endpoint integration
- DNS configuration for domain services
- Domain user authentication
- Windows network configuration
- Validation of domain membership
- Verification of computer objects in Active Directory
- Preparation of endpoints for centralized policy and security monitoring

These skills support the broader cybersecurity lab by integrating Windows endpoints into the domain environment used for telemetry collection, monitoring, and future detection and incident-response activities.

---
