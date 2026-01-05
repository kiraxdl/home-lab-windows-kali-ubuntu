# Changing IP Address: Ubuntu Server 

## Purpose
To make the IP address of the Server static

## Ubuntu Server
# Commands Used

ls /etc/netplan/
# Result: 50-cloud-init.yaml
sudo nano /etc/netplan/50-cloud-init.yaml
# Edit the interface from

network:
  version: 2
  ethernets: 
    enp0s: 
      dhcp4: true

to 

network:
  version: 2
  ethernets: 
    enp0s: 
      addresses:
        - 192.168.64.67/24\
      gateway4: 192.168.64.1
      nameservers:
        addresses:
          - 8.8.8.8
          - 8.8.4.4

# Removed the dhcp4 because I already set the IP to static.
# Defines the DNS Server by adding 8.8.8.8 and 8.8.4.4

sudo netplan apply

# Result: ERROR: ifconfig doesn't show ipv4 and gateway
  pinging windows client: Network Unreachable
  pinging gateway: Network Unreachable
  pinging external DNS: Network Unreachable

## Fix
# Commands Used

sudo nano /etc/netplan/50-cloud-init.yaml

network:
  version: 2
  ethernets: 
    enp0s: 
      addresses:
        - 192.168.64.67/24\
      gateway4: 192.168.64.1
      nameservers:
        addresses:
          - 8.8.8.8
          - 8.8.4.4

# Error found in line 6. Removed the extra \ after /24

# Result: IP successfully changed to 192.168.64.67



















