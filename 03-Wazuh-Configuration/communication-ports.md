# Wazuh Communication Ports

## Overview

This document records the network ports used by the Wazuh deployment and compares the documented Wazuh service purposes with the ports observed on the Ubuntu Wazuh VM.

The ports were verified using:

```bash
sudo ss -lntp
