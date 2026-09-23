# Lab Setup

## Overview

This section documents the physical and virtual infrastructure used to build the SOC home lab.

The lab uses VirtualBox for virtualization and a bridged network configuration so the Ubuntu Wazuh VM can communicate with the physical Windows host on the home LAN.

## Lab Components

| System | Role | Platform | Network Address | Status |
|---|---|---|---|---|
| Windows Host | Monitored endpoint | Physical Windows system | 192.168.0.100 | Active |
| Ubuntu Wazuh VM | SIEM platform | VirtualBox VM | 192.168.0.105 | Active |
| Kali Linux VM | Attack simulation | VirtualBox VM | TBD | Not currently running |

## Virtualization

VirtualBox is used to host the Ubuntu Wazuh VM and Kali Linux attack simulation VM.

The Ubuntu Wazuh VM uses a **Bridged Adapter**, allowing it to communicate directly with systems on the home LAN.

## Network

The lab currently operates on:

- Network: `192.168.0.0/24`
- Default Gateway: `192.168.0.1`
- Windows Host: `192.168.0.100`
- Ubuntu Wazuh VM: `192.168.0.105`

## Connectivity Verification

Connectivity between the Windows host and Ubuntu Wazuh VM was verified.

| Test | Result |
|---|---|
| Windows → Ubuntu ICMP | Successful |
| Windows → Ubuntu TCP/1514 | Successful |
| Windows → Ubuntu TCP/1515 | Successful |

TCP port 1514 is used for Wazuh agent communication, while TCP port 1515 is used for agent enrollment.

## Lab Status

The base infrastructure is operational.

The next stage is Wazuh configuration and Windows endpoint integration.
