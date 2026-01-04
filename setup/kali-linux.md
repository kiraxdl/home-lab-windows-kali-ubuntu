# Kali Linux (Attacker) Setup (Cybersecurity Home Lab)

## Overview
This document describes the setup of a **Kali Linux** virtual machine in **UTM** for a cybersecurity home lab.  
The system acts as the **attacker machine** used for scanning, enumeration, and exploitation against target systems.

- **Role:** Attacker
- **OS:** Kali Linux (Graphical)
- **Network:** Shared Network (NAT) — allows VM-to-VM communication and internet access

## Virtual Machine Specifications

| Component | Configuration |
|-----------|---------------|
| CPU       | 2 cores |
| RAM       | 4 GB |
| Storage   | 50 GB (virtual disk) |
| Network   | Shared Network (DHCP) |
| ISO       | Kali Linux Installer (Graphical) |

## Installation Steps

1. **Create VM in UTM**
   - CPU: 2 cores
   - RAM: 4 GB
   - Storage: 50 GB
   - Mount Kali Linux ISO

2. **Start VM and Install**
   - Select **Graphical Install**
   - Choose language, location, and keyboard

3. **Network Configuration**
   - Select interface (eth0)
   - Use **DHCP**
   - Set hostname (e.g., kali-attacker)

4. **User and Password Setup**
   - Create non-root user
   - Set user and root passwords

5. **Storage Configuration**
   - Guided storage → Use entire disk
   - All files in one partition
   - Confirm disk changes

6. **Software Selection**
   - Select **Kali Desktop**
   - Choose **XFCE** desktop environment
   - Install default Kali tools

7. **Complete Installation**
   - Install GRUB bootloader
   - Remove ISO from CD/DVD in UTM
   - Reboot VM

## Post-Installation Setup

1. **Login**
login: kali
password: password

2. **Verify Network Connectivity**
ip a

# Ping Ubuntu Server
ping 192.168.64.5

# Ping Windows 11 Client
ping 192.168.64.6

# Attacker IP: 192.168.64.x
# Target IPs reachable
