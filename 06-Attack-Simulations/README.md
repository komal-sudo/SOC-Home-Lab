# Attack Simulations

## Overview

This module demonstrates controlled attack simulations and security monitoring in my SOC Home Lab.

The objective is to understand how common attack behaviors appear in endpoint telemetry, how SIEM solutions collect and analyze security events, and how a SOC analyst investigates suspicious activity.

## Lab Environment

| Component | Technology |
|---|---|
| SIEM | Wazuh |
| SIEM Manager | Ubuntu 24.04 LTS |
| Endpoint | Windows 11 |
| Endpoint Monitoring | Sysmon |
| Agent | Wazuh Agent |
| Network Testing | Nmap |
| PowerShell Monitoring | Windows PowerShell |
| File Integrity Monitoring | Wazuh FIM |
| Malware Test | EICAR test file |

## Attack Simulation List

| ID | Simulation | Tool / Technique | Status |
|---|---|---|---|
| AS-01 | Account Discovery | Windows CMD / PowerShell | In progress |
| AS-02 | Network Scanning | Nmap | Planned |
| AS-03 | Brute-Force Simulation | Windows Security Logs | Planned |
| AS-04 | PowerShell Activity | PowerShell / Sysmon | Planned |
| AS-05 | File Integrity Tests | Wazuh FIM | Planned |
| AS-06 | Malware Simulation | EICAR / Windows Defender | Planned |

## Simulation Methodology

Each simulation follows these stages:

1. Define the objective and authorized lab scope.
2. Prepare the test environment.
3. Execute the controlled activity.
4. Collect endpoint and security telemetry.
5. Verify event ingestion in Wazuh.
6. Check whether a detection rule generated an alert.
7. Investigate the event and assess its context.
8. Record findings, limitations, and conclusions.
9. Capture screenshots and document the evidence.

## Evidence

Screenshots and supporting evidence are maintained in the repository's `08-Screenshots` directory.

## Safety and Scope

All exercises are performed within an authorized, controlled home lab.

No real malware, unauthorized targets, or production systems are used. The EICAR test file is used for harmless antivirus validation.

## Learning Outcomes

- Network reconnaissance monitoring
- Windows authentication-event analysis
- PowerShell activity monitoring
- Sysmon event investigation
- File integrity monitoring
- Antivirus and security-event analysis
- Wazuh alert validation
- MITRE ATT&CK mapping
- SOC investigation and documentation

## Important Observation

A command execution or security event does not automatically indicate malicious activity. Each finding is assessed using available evidence, context, and correlation with related events.
