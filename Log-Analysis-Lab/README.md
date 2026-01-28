# Active Directory Audit Policy Lab

## Overview
This lab demonstrates configuring Advanced Audit Policies in an Active Directory environment to monitor authentication activity. The focus is on capturing and analyzing successful logons, failed logons, and explicit credential usage using Windows Event Viewer.

## Lab Environment
- Hyper-V
- Windows Server (Domain Controller with AD DS and DNS)
- Windows 10/11 Client (Domain-Joined)
- Domain Admin and Domain User accounts

## Objectives
- Configure Advanced Audit Policies using Group Policy
- Apply audit policies to a specific Organizational Unit (OU)
- Generate authentication events
- Analyze security logs
- Understand where authentication events are logged in a domain environment

## Configuration

### Organizational Unit
- Created a dedicated OU for auditing
- Moved the client computer object into the OU

### Group Policy
- Created and linked a GPO to the auditing OU
- Configured Advanced Audit Policies:

Computer Configuration  
Policies  
Windows Settings  
Security Settings  
Advanced Audit Policy Configuration  
Audit Policies  
Logon/Logoff  

- Audit Logon: Success, Failure  
- Audit Account Logon: Success, Failure  

### Policy Application
- Forced Group Policy update on the client:
gpupdate /force

- Verified audit policy status using:
auditpol /get /category:Logon/Logoff

## Testing

### Failed Logon
- Attempted to log in to the client using an incorrect password
- Confirmed Event ID 4625 in Event Viewer

### Successful Logon
- Logged in with valid credentials
- Confirmed Event ID 4624


## Event IDs

4624 – Successful logon  
4625 – Failed logon  

## Key Takeaways
- Authentication events are logged on the system where the logon attempt occurs
- Audit policies must be applied at the computer level
- Failed authentication attempts generate security events without account lockout
- Windows Security logs are essential for monitoring and investigation


