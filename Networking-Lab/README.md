# Networking Lab: DNS, DHCP, and Connectivity Troubleshooting

## Overview
This lab demonstrates foundational enterprise networking concepts using a Windows Server Domain Controller and a Windows client. The focus is on IP addressing, DNS name resolution, DHCP functionality, and troubleshooting common network failures.

The lab was completed in a virtualized environment to simulate a small corporate network.

## Lab Environment

**Domain Controller (DC)**
- OS: Windows Server
- Roles:
  - Active Directory Domain Services (AD DS)
  - DNS Server
  - DHCP Server
- IP Address: `192.168.10.10` (Static)

**Client Machine**
- OS: Windows
- Joined the domain
- IP Address: DHCP-assigned (or static for testing)
- DNS Server: Domain Controller

## Objectives
- Assign and verify IP configuration
- Validate DNS name resolution
- Configure and test DHCP
- Simulate a DNS failure scenario
- Troubleshoot and restore connectivity
- Document real-world networking behavior

## IP Configuration Verification

The client machine was verified to have correct network settings, including:
- Valid IPv4 address
- Correct subnet mask
- DNS server pointing to the Domain Controller

