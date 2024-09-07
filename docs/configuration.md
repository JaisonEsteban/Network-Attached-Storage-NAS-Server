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

1.3 Set Samba User Password

      sudo smbpasswd -a pi

Replace [pi] with your username.

1.4 Restart Samba Service

      sudo systemctl restart smbd

## 2. Access the Share

On **Windows**: Use \\<raspberrypi-ip>\shared in File Explorer.
On **macOS**: Use smb://<raspberrypi-ip>/shared in Finder.


