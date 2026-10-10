## Agent Verification and Event Ingestion

### Environment
- Endpoint: Windows 11
- SIEM: Wazuh 4.14.7
- Agent name: `Windows-Endpoint`
- Wazuh Manager: Ubuntu VM
- Agent communication: TCP/1514

### Verification Results

| Check | Result |
|---|---|
| Windows Wazuh service | Running |
| Manager connectivity | Successful |
| Manager-side agent status | Active |
| Windows Security event collection | Confirmed |
| Wazuh alert ingestion | Confirmed |

### Troubleshooting: Manager IP Change

After restarting the lab, the Ubuntu VM's DHCP-assigned IP address changed. The Windows agent continued attempting to connect to the previous address.

**Resolution:** Verified the manager's current IP, confirmed TCP/1514 connectivity, updated the Windows agent's manager address, and restarted the agent service. The agent subsequently connected and appeared as Active on the manager.

### Syscollector Diagnostic Note

The agent previously terminated with an access violation reported in `sysinfo.dll`. Syscollector was temporarily disabled during troubleshooting. Although the agent subsequently became operational, the underlying cause of the original crash has not been conclusively established.

### Evidence

- `../08-Screenshots/windows-agent-active.png`
- `../08-Screenshots/windows-event-ingestion.png`
