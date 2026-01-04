# **Ubuntu Server (minimized)** Setup (Cybersecurity Home Lab)

## Overview
This document describes the setup of an **Ubuntu Server (minimized)** VM in **UTM** for a cybersecurity home lab.  
The server acts as a target for testing and networking practice.

- **Role:** Server
- **OS:** Ubuntu Server LTS (Minimized)
- **Network:** Shared Network (NAT) — allows VM-to-VM communication and internet access

## Virtual Machine Specifications

| Component | Configuration |
|-----------|---------------|
| CPU       | 2 cores |
| RAM       | 2 GB |
| Storage   | 50 GB (virtual disk) |
| Network   | Shared Network (DHCP) |
| ISO       | Ubuntu Server LTS (Minimized) |

## Installation Steps

1. **Create VM in UTM**
   - CPU: 2 cores, RAM: 2 GB, Storage: 50 GB
   - Mount Ubuntu Server ISO

2. **Start VM and Install**
   - Select language and keyboard
   - Choose **Install Ubuntu Server**

3. **Network Configuration**
   - Select interface (ens3)
   - Use **DHCP**
   - Skip proxy configuration

4. **Storage Configuration**
   - Guided storage → Use entire disk
   - Enable **LVM**
   - No disk encryption

5. **OpenSSH Server**
   - Install **OpenSSH server**
   - Skip importing SSH keys
   - Skip Featured Server Snaps

6. **Complete Installation**
   - Remove ISO from CD/DVD in UTM
   - Reboot VM

## Post-Installation Setup

1. **Login**
```bash
login: username
password: password
