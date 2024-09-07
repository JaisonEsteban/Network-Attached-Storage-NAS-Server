# Network-Attached-Storage-NAS-Server

# Raspberry Pi NAS Setup

This guide will help you set up a Network Attached Storage (NAS) on your Raspberry Pi. 
For detailed steps on partitioning, formatting, and configuring Samba, refer to the [Setup Guide](docs/setup.md) and other related documents.

## Prerequisites
Raspberry Pi with Raspberry Pi OS installed
USB drive connected to the Raspberry Pi
Basic familiarity with terminal commands

## Overview

The Raspberry Pi NAS project involves:
- Preparing your hardware
- Installing and configuring necessary software
- Setting up file sharing with Samba

## Quick Links

- [Setup Guide](docs/setup.md)
- [Configuration Guide](docs/configuration.md)
- [Troubleshooting](docs/troubleshooting.md)

## Getting Started

1. **Prepare Your Hardware**
   - Ensure your Raspberry Pi is set up and connected to the network.
   - Attach the USB drive to the Raspberry Pi.

2. **Installation**
   - Follow the instructions in the [Setup Guide](docs/setup.md) for partitioning and formatting your USB drive.

3. **Configuration**
   - Configure Samba by following the steps in the [Configuration Guide](docs/configuration.md).

4. **Accessing Your NAS**
   - Access your NAS from other devices on your network as described in the [Configuration Guide](docs/configuration.md).

## Troubleshooting

**Drive Not Mounted:** Ensure the USB drive is properly formatted and check /etc/fstab for correct entries.

**Access Issues:** Verify Samba configuration and ensure permissions are correctly set on the shared directory.
