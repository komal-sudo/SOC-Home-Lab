# Lab Inventory

## Systems

| System | Role | Platform | IP Address | Status |
|---|---|---|---|---|
| Windows Host | Monitored endpoint | Physical Windows | 192.168.0.100 | Active |
| Ubuntu Wazuh VM | SIEM platform | Ubuntu Server / VirtualBox | 192.168.0.105 | Active |
| Kali Linux VM | Attack simulation | Kali Linux / VirtualBox | TBD | Powered Off |

## Ubuntu Wazuh Services

The Ubuntu Wazuh VM hosts the following Wazuh components:

- Wazuh Manager
- Wazuh Indexer
- Wazuh Dashboard

All three services were verified as running.

## Notes

The Kali Linux IP address will be documented after the VM is powered on and its network configuration is verified.

The Windows Wazuh Agent and Sysmon will be documented in their respective project sections after deployment.
