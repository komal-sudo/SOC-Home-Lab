# Sysmon

## Overview

This section documents the installation and configuration of Microsoft Sysmon on the Windows 11 endpoint and its integration with the Wazuh SIEM manager.

Sysmon provides detailed Windows telemetry that supports endpoint monitoring and security investigations.

## Components

- **Sysmon:** Generates detailed Windows system activity events.
- **Wazuh Agent:** Collects configured Windows event channels and forwards events to the manager.
- **Wazuh Manager:** Processes incoming events and evaluates configured detection rules.
- **Sysmon configuration:** SwiftOnSecurity Sysmon configuration.

## Implementation

1. Downloaded Sysmon from the official Microsoft Sysinternals website.
2. Extracted the Sysmon utilities on the Windows endpoint.
3. Installed Sysmon using the SwiftOnSecurity configuration file.
4. Verified that the Sysmon service was running.
5. Verified local events in the `Microsoft-Windows-Sysmon/Operational` channel.
6. Configured the Wazuh agent to monitor the Sysmon Operational event channel.
7. Restarted the Wazuh agent and verified that Sysmon events appeared in Wazuh alert logs.

## Validation Evidence

- Sysmon Operational events were observed locally on Windows.
- Wazuh agent `001` (`Windows-Endpoint`) was confirmed Active.
- A Sysmon Process Create event (Event ID 1) associated with `net1.exe` and the `net user` command appeared in Wazuh alerts.
- Wazuh rule `92031`, **Discovery activity executed**, matched the observed event.
- The alert included MITRE ATT&CK mapping `T1087` — Account Discovery.

## Analyst Notes

The `net user` command can be used for legitimate administration or account discovery. A detection-rule match does not independently establish malicious activity. Further investigation would be required to determine whether the behavior was authorized.

## Status

**Completed — basic Sysmon installation, Wazuh event-channel configuration, and alert-ingestion validation.**

## Evidence

Screenshots documenting installation, local event verification, Wazuh agent status, and alert ingestion are maintained in `08-Screenshots`.
