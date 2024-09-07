# Configuration Guide

## 1. Configure Samba

1.1 Edit the Samba Configuration File
   
      sudo nano /etc/samba/smb.conf

1.2 Add a New Share
   At the end of the file, add:
   
      [shared]
      
      path = /media/mydrive
      
      browseable = yes
      
      writable = yes
      
      guest ok = yes
      
      create mask = 0777
      
      directory mask = 0777

   Save and exit (Ctrl+O, Enter, Ctrl+X).

1.3 Set Samba User Password

      sudo smbpasswd -a pi

Replace [ pi ] with your username.

Follow the prompts to enter and confirm the password.

1.4 Restart Samba Service

      sudo systemctl restart smbd

## 2. Access the Share

**Replace <raspberrypi-ip> with the IP address of your Raspberry Pi**

On **Windows**: Use \\<raspberrypi-ip>\shared in File Explorer.

On **Windows**: Open File Explorer and enter \\<raspberrypi-ip>\shared in the address bar.

On **macOS**: Use smb://<raspberrypi-ip>/shared in Finder.

On **macOS**: Open Finder, select Go > Connect to Server, and enter smb://<raspberrypi-ip>/shared.

**Replace <raspberrypi-ip> with the IP address of your Raspberry Pi**






