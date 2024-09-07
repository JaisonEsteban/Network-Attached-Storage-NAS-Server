# Setup Guide

## 1. Install Necessary Packages

    sudo apt update

    sudo apt install parted samba

**2. Partition the USB Drive**

2.1 Identify the USB Drive:

List all storage devices to identify your USB drive

      lsblk

Look for the device identifier, such as /dev/sda.
  
2.2 Partition Using (parted):

Start parted and select your USB drive (replace /dev/sda with your drive identifier)

       sudo parted /dev/sda
   
2.3 Create a new partition table:

    (parted) mklabel msdos

2.4 Create a new partition:

    (parted) mkpart primary ext4 0% 100%

2.5 Exit (parted):

    (parted)     quit

**3. Format the USB Drive**

3.1 Format the new partition:

    sudo mkfs.ext4 /dev/sda1

**4. Mount the USB Drive**

4.1 Create a Mount Point:

Create a directory where the USB drive will be mounted

      sudo mkdir /media/mydrive

4.2 Mount the Drive :

      sudo mount /dev/sda1 /media/mydrive

4.3 Make the Mount Persistent:

To make the mount persistent across reboots, edit /etc/fstab

      sudo nano /etc/fstab
  
  Add the following line:  
    
      /dev/sda1 /media/mydrive ext4 defaults 0 0
  
**Save and exit (Ctrl+O, Enter, Ctrl+X).**

