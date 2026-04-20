# Windows Endpoint Support & Troubleshooting Lab

This project documents common Windows endpoint support and help desk troubleshooting scenarios in a home lab environment. The goal is to demonstrate practical troubleshooting, root cause analysis, documentation, and verification skills for entry-level Help Desk, Desktop Support, and IT System Support roles.

## Lab Environment

- Windows Server Domain Controller
- Windows 11 domain-joined client
- Active Directory Domain Services
- DNS configured through the Domain Controller
- Host-only virtual network
- Static IPv4 configuration
- Shared folders and test user accounts

## Project Structure

Each troubleshooting scenario is documented as a separate ticket inside the `tickets` folder. Screenshots for each ticket are stored in the `screenshots` folder.

```text
windows-endpoint-support-troubleshooting-lab/
│
├── README.md
├── tickets/
│   └── ticket-01-user-has-no-internet-access.md
│
└── screenshots/
    └── ticket-01-...
```


## Completed Tickets

### 1. User Has No Internet Access / Network Connectivity Issue

Troubleshooting a Windows 11 client in a host-only Active Directory lab where an incorrect static IP configuration prevented communication with the Domain Controller and DNS services.

[View Ticket 01 Documentation](tickets/ticket-01-user-has-no-internet-access.md)


### 2. DNS Resolution Issue

Network connectivity is available, but domain names or server names do not resolve correctly. Troubleshooting includes `nslookup`, DNS server verification, and DNS cache flushing.

[View Ticket 02 Documentation](tickets/ticket-02-dns-resolution-issue.md)

## Planned Ticket Scenarios

The following scenarios are planned for this lab:

### 3. Shared Folder Access Denied

A user cannot access a shared folder. Troubleshooting includes Share Permissions, NTFS Permissions, and Active Directory group membership.

### 4. Printer Not Working

A user cannot print successfully. Troubleshooting includes default printer settings, offline printer status, stuck print queue, and restarting the Print Spooler service.

### 5. Slow Computer Performance

A workstation is running slowly. Troubleshooting includes Task Manager review, startup apps, disk space, temporary files, and Windows updates.

### 6. Software Installation Issue

A user cannot install or run software. Troubleshooting includes admin permissions, UAC prompts, incomplete installation, and reinstall workflow.

### 7. Mapped Network Drive Not Connecting

A user cannot connect to a mapped network drive. Troubleshooting includes the `\\server\share` path, credentials, network access, and drive mapping.

### 8. Windows Update Problem

Windows updates fail or become stuck. Troubleshooting includes restart checks, Windows Update service status, disk space, and update retry steps.

### 9. User Profile Issue

A user profile does not load correctly, a temporary profile appears, or desktop/files are missing. Troubleshooting includes profile status, user folders, and Windows profile behavior.

## Tools and Commands Used

- Command Prompt
- PowerShell
- Network Adapter Settings
- Event Viewer
- Group Policy Management
- Services Console
- Active Directory Users and Computers

Common commands used in this project include:

```cmd
ipconfig /all
ping
nslookup
ipconfig /flushdns
gpupdate /force
gpresult /r
whoami
net use
net stop spooler
net start spooler
```

## Note

The Active Directory login troubleshooting scenario was completed in a separate Active Directory home lab project. This repository focuses on Windows endpoint and help desk troubleshooting scenarios.
