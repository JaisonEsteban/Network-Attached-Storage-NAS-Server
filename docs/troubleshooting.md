# Troubleshooting Guide

## Common Issues

### 1. Unable to Access the Share

 **Check Samba Status**

    sudo systemctl status smbd

**Verify Network Connection:** Ensure your Raspberry Pi and client device are on the same network.

### 2. Permissions Issues

Check Directory Permissions 

    ls -l /media/mydrive

Adjust Permissions

      sudo chown -R pi:pi /media/mydrive

### 3. Drive Not Mounting

**Verify** /etc/fstab **Entry**
Ensure that the entry is correctly formatted and matches your drive and mount point.

**Manually Mount**
          sudo mount -a


Feel free to adjust the content based on your specific setup and preferences!

