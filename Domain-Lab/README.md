# Active Directory Home Lab

## Overview
This project documents the setup of a small enterprise-style Active Directory environment using Hyper-V. The lab consists of a Windows Server 2022 domain controller and a Windows client joined to the domain on an internal virtual network.

## Environment
- Host OS: Windows 11
- Hypervisor: Hyper-V
- Domain Controller: Windows Server 2022 (DC01)
- Client Machine: Windows 11 Enterprise (CLIENT01)
- Domain Name: corp.local
- Network Type: Hyper-V Internal Switch

## Configuration Performed
- Installed Windows Server 2022 and promoted it to a Domain Controller
- Installed and configured Active Directory Domain Services and DNS
- Assigned static IP addresses to the domain controller and client
- Joined the Windows client machine to the domain
- Verified authentication and network connectivity between systems

## Troubleshooting
- Resolved ICMP connectivity issues caused by Windows Firewall rules
- Diagnosed Hyper-V internal switch behavior after host network reset
- Verified DNS configuration for successful domain communication

## Skills Demonstrated
- Active Directory administration
- Windows Server configuration
- DNS and domain authentication
- Virtual networking with Hyper-V
- Network troubleshooting
