# Setup Guide

## 1. Install Necessary Packages

    sudo apt update

    sudo apt install parted samba

**2. Partition the USB Drive**

2.1 Identify the USB Drive

      lsblk
  
2.2 Partition Using (parted)

       sudo parted /dev/sda
   
2.3 Create a new partition table:

(parted)     mklabel msdos

2.4 Create a new partition:

(parted)     mkpart primary ext4 0% 100%

2.5 Exit (parted):

    (parted)     quit

**3. Format the USB Drive**

    sudo mkfs.ext4 /dev/sda1

**4. Mount the USB Drive**

4.1 Create a Mount Point:

      sudo mkdir /media/mydrive

4.2 Mount the Drive :

      sudo mount /dev/sda1 /media/mydrive

4.3 Make the Mount Persistent:

      sudo nano /etc/fstab
  
  Add the following line:  
    
      /dev/sda1 /media/mydrive ext4 defaults 0 0
  
**Save and exit (Ctrl+O, Enter, Ctrl+X).**

