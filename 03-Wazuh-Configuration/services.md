# Wazuh Services

## Overview

The SOC home lab uses an all-in-one Wazuh deployment on the Ubuntu Wazuh VM.

The following Wazuh components are currently running on the server:

- Wazuh Manager
- Wazuh Indexer
- Wazuh Dashboard

## Service Status

Service status was verified using:

```bash
sudo systemctl is-active wazuh-manager wazuh-indexer wazuh-dashboard
