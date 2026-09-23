# Network Configuration

## Network Topology

The SOC home lab currently operates on the `192.168.0.0/24` network.

| Device | Address |
|---|---|
| Home Router / Gateway | 192.168.0.1 |
| Windows Host | 192.168.0.100 |
| Ubuntu Wazuh VM | 192.168.0.105 |

## Ubuntu Wazuh VM

The Ubuntu Wazuh VM uses a VirtualBox **Bridged Adapter**.

Network interface:

```text
enp0s3
