# Windows 11 Pro Setup (Cybersecurity Home Lab)

## Overview
This document describes the setup of a **Windows 11 Pro** virtual machine in **UTM** for a cybersecurity home lab.  
The system acts as a **client machine** used to access services hosted on the Ubuntu Server and to observe normal user-side behavior during security testing.

- **Role:** Client
- **OS:** Windows 11 Pro (Trial)
- **Network:** Shared Network (NAT) — allows VM-to-VM communication and internet access

## Virtual Machine Specifications

| Component | Configuration |
|-----------|---------------|
| CPU       | 2 cores |
| RAM       | 4–6 GB |
| Storage  | 50 GB (virtual disk) |
| Network  | Shared Network (DHCP) |
| ISO      | Windows 11 Multi-Edition (Pro) |

## Installation Steps

1. **Create VM in UTM**
   - CPU: 2 cores  
   - RAM: 4–6 GB  
   - Storage: 50 GB  
   - Mount Windows 11 ISO  

2. **Start VM and Install**
   - Select language, time, and keyboard layout
   - Click **Install Now**

3. **Windows Edition Selection**
   - Choose **Windows 11 Pro**
   - Accept license terms

4. **Installation Type**
   - Select **Custom: Install Windows only**
   - Choose the unallocated virtual disk
   - Proceed with installation

5. **Initial Setup**
   - Skip Microsoft account (offline account)
   - Create local user account
   - Disable unnecessary privacy options

6. **Complete Installation**
   - Windows will reboot automatically
   - VM boots into Windows desktop

## Post-Installation Setup

1. **Verify Network Connectivity**
```powershell
ipconfig

# Ping Ubuntu Server VM
ping 192.168.64.5

# Confirm Windows VM IP
# Windows 11 Client IP: 192.168.64.6
