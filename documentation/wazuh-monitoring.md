# Wazuh Monitoring and Agent Enrollment

## Purpose

This phase deployed Wazuh as the lab’s security monitoring platform and connected the Windows systems for centralized visibility.

Wazuh monitored endpoint activity, provided security telemetry, and prepared the environment for future alerting, detection engineering, and incident-response analysis.

## Scope

This documentation covers the initial Wazuh deployment and endpoint enrollment process, including:

- Wazuh deployment on Kali Purple
- Windows agent installation
- Agent enrollment and connectivity
- Monitoring of DC01, Win11-01, and Win11-02
- Validation of active agent status
- Preparation for future dashboards, alerts, and detection rules

  
## Wazuh Deployment and Architecture

Wazuh was deployed on the Kali Purple system within the ALLSAFE security network.

The Wazuh platform provides centralized visibility into activity from the Windows systems enrolled in the lab.

The monitored Windows systems include:

- DC01
- Win11-01
- Win11-02

The Wazuh server operates on the defensive security side of the lab and receives telemetry from the enrolled Windows agents for centralized monitoring and future detection development.

This architecture supports the lab’s security monitoring workflow by separating endpoint systems from the defensive tooling used to analyze their activity.

## Windows Agent Enrollment

Wazuh agents were installed on the lab's Windows systems and enrolled with the Wazuh server for centralized monitoring.

The enrolled systems include:

- DC01
- Win11-01
- Win11-02

Agent connectivity was verified from the Wazuh dashboard to confirm that each Windows system was actively communicating with the monitoring platform.

This enrollment provides centralized endpoint visibility and establishes the foundation for future alerting, detection rules, threat hunting, and incident-response analysis.

## Validation

The Wazuh deployment was validated by reviewing agent status from the Wazuh dashboard and confirming that all enrolled Windows systems were actively communicating with the platform.

Validation included:

- Confirming DC01 was enrolled and active
- Confirming Win11-01 was enrolled and active
- Confirming Win11-02 was enrolled and active
- Verifying agent connectivity from the Wazuh dashboard
- Confirming endpoint operating system information was visible
- Confirming the monitoring environment was ready for future alerting and detection work

This validation confirmed that Wazuh successfully received data from the Windows systems and provided centralized endpoint visibility across the lab.

## Skills Demonstrated

This phase demonstrates security monitoring and endpoint visibility skills, including:

- Wazuh deployment and configuration
- Windows security agent installation
- Endpoint enrollment and connectivity validation
- Centralized monitoring of Windows systems
- Security telemetry collection
- SIEM/XDR platform familiarity
- Preparation for alerting and detection engineering
- Foundational SOC monitoring and incident-response workflows

These skills support the broader cybersecurity lab by providing centralized visibility into endpoint activity and establishing the monitoring foundation needed for future detection, threat-hunting, and incident-response exercises.

---
