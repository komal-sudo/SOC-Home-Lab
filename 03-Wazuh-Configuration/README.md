# Wazuh Configuration

## Overview

This section documents the Wazuh SIEM deployment used in the SOC home lab.

The Wazuh environment is deployed as an **all-in-one installation** on an Ubuntu Server virtual machine. The deployment includes the Wazuh Manager, Wazuh Indexer, and Wazuh Dashboard.

The Windows host will later be integrated as a monitored endpoint using the Wazuh Agent.

## Wazuh Components

### Wazuh Manager

The Wazuh Manager is responsible for receiving security telemetry from Wazuh agents, decoding events, and applying detection rules.

In this lab, the Wazuh Manager runs on the Ubuntu Wazuh VM.

### Wazuh Indexer

The Wazuh Indexer stores and indexes security event data so that events can be searched and investigated efficiently.

The Indexer runs on the same Ubuntu VM as the Wazuh Manager in this lab.

### Wazuh Dashboard

The Wazuh Dashboard provides the web interface used by the SOC analyst to monitor alerts, search events, and investigate security activity.

The Dashboard also runs on the Ubuntu Wazuh VM.

### Wazuh Agent

The Wazuh Agent is installed on monitored endpoints and collects security telemetry before forwarding it to the Wazuh Manager.

The Windows host will be configured as a Wazuh Agent in the next stage of the project.

## Deployment Architecture

The current Wazuh deployment is:

```text
Ubuntu Wazuh VM
192.168.0.105
        |
        +-- Wazuh Manager
        |
        +-- Wazuh Indexer
        |
        +-- Wazuh Dashboard
