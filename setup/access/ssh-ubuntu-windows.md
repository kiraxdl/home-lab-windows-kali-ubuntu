# SSH Access: Ubuntu Server from Windows 

## Purpose
Enable SSH on an Ubuntu Server  and access it from a Windows 11 Pro .

## Ubuntu Server (SSH Server)
# Commands Used

systemctl status ssh
sudo systemctl enable ssh
sudo systemctl start ssh

## Windows 11 Pro (SSH Client)
# Commands Used

ssh kiraxd@192.168.64.5

## Result
- SSH enabled and running on Ubuntu Server
- Windows successfully connects via SSH

## Notes
- VMs must be on the same UTM network
- SSH uses port 22 by default
