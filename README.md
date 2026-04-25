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
│   ├── ticket-01-user-has-no-internet-access.md
│   ├── ticket-02-dns-resolution-issue.md
│   ├── ticket-03-shared-folder-access-denied.md
│   ├── ticket-04-printer-not-working.md
│   └── ticket-05-slow-computer-performance.md
│
└── screenshots/
    ├── ticket-01-1-post-fix-connectivity-domain-verification.png
    ├── ticket-01-2-post-fix-connectivity-domain-verification.png
    ├── ticket-01-corrected-ipv4-dns-configuration.png
    ├── ticket-01-ipconfig-connectivity-failure.png
    ├── ticket-02-1-dns-resolution-success.png
    ├── ticket-02-2-dns-resolution-success.png
    ├── ticket-02-3-dns-resolution-success.png
    ├── ticket-02-corrected-dns-server.png
    ├── ticket-02-dns-resolution-failure.png
    ├── ticket-03-access-denied-finance-share.png
    ├── ticket-03-shared-folder-access-restored.png
    ├── ticket-03-user-added-to-IT-group.png
    ├── ticket-03-user-groups-before-fix.png
    ├── ticket-04-installed-printers.png
    ├── ticket-04-print-spooler-restarted.png
    ├── ticket-04-print-spooler-stopped.png
    ├── ticket-04-printing-failure-confirmed.png
    ├── ticket-04-sc-query-spooler-status.png
    ├── ticket-04-test-print-successful.png
    ├── ticket-05-01-task-manager-performance.png
    ├── ticket-05-02-task-manager-performance.png
    ├── ticket-05-03-startup-apps-before.png
    ├── ticket-05-04-disk-space-before.png
    ├── ticket-05-05-temp-files-before-cleanup.png
    ├── ticket-05-06-windows-update-status.png
    ├── ticket-05-07-01-event-viewer-system-log.png
    ├── ticket-05-07-02-event-viewer-system-log.png
    ├── ticket-05-07-03-event-viewer-system-log.png
    └── ticket-05-08-final-verification.png

```



## Completed Tickets

### 1. User Has No Internet Access / Network Connectivity Issue

Troubleshooting a Windows 11 client in a host-only Active Directory lab where an incorrect static IP configuration prevented communication with the Domain Controller and DNS services.

[View Ticket 01 Documentation](tickets/ticket-01-user-has-no-internet-access.md)

### 2. DNS Resolution Issue

Network connectivity is available, but domain names or server names do not resolve correctly. Troubleshooting includes `nslookup`, DNS server verification, DNS correction, and successful DNS resolution verification.

[View Ticket 02 Documentation](tickets/ticket-02-dns-resolution-issue.md)

### 3. Shared Folder Access Denied

A user cannot access a shared folder. Troubleshooting includes Share Permissions, NTFS Permissions, Active Directory group membership, and access restoration verification.

[View Ticket 03 Documentation](tickets/ticket-03-shared-folder-access-denied.md)

### 4. Printer Not Working

A user cannot print successfully. Troubleshooting includes installed printer review, print failure verification, Print Spooler service troubleshooting, service restart, and successful test print verification.

[View Ticket 04 Documentation](tickets/ticket-04-printer-not-working.md)

### 5. Slow Computer Performance

A Windows 11 workstation was reported as running slowly. Troubleshooting included Task Manager performance review, startup app review, disk space verification, temporary file cleanup, Windows Update status review, Event Viewer log review, and final performance verification.

[View Ticket 05 Documentation](tickets/ticket-05-slow-computer-performance.md)


## Planned Ticket Scenarios

The following scenarios are planned for future documentation in this lab:

### 6. Software Installation Issue

A user cannot install or run software. Troubleshooting will include admin permissions, UAC prompts, incomplete installation, and reinstall workflow.

### 7. Mapped Network Drive Not Connecting

A user cannot connect to a mapped network drive. Troubleshooting will include the `\\server\share` path, credentials, network access, and drive mapping.

### 8. Windows Update Problem

Windows updates fail or become stuck. Troubleshooting will include restart checks, Windows Update service status, disk space, and update retry steps.

### 9. User Profile Issue

A user profile does not load correctly, a temporary profile appears, or desktop/files are missing. Troubleshooting will include profile status, user folders, and Windows profile behavior.

## Tools and Commands Used

- Command Prompt
- PowerShell
- Network Adapter Settings
- Windows Settings
- Task Manager
- Event Viewer
- Group Policy Management
- Services Console
- Active Directory Users and Computers
- Printer Queue / Printer Settings

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
sc query spooler

```

