# Laptop Deployment Procedure

## Document Information

| Field | Value |
|---------|---------|
| SOP ID | SOP-005 |
| Title | Laptop Deployment Procedure |
| Department | Information Technology |
| Owner | IT Support Team |
| Version | 1.0 |
| Status | Active |
| Last Updated | June 2026 |

---

# Purpose

This Standard Operating Procedure (SOP) outlines the process for preparing, configuring, deploying, and documenting laptops for employees.

The objective is to ensure devices are deployed consistently, securely, and fully operational prior to user assignment.

---

# Scope

This procedure applies to:

- New Employee Deployments
- Hardware Refreshes
- Replacement Devices
- Temporary Loaner Devices

Supported Operating Systems:

- Windows 10
- Windows 11
- macOS

---

# Roles and Responsibilities

## IT Support Technician

Responsible for:

- Device preparation
- Software installation
- User assignment
- Validation testing
- Documentation

---

## Systems Administrator

Responsible for:

- Device imaging standards
- Security policies
- Escalation support

---

## End User

Responsible for:

- Verifying device functionality
- Reporting issues
- Following company security policies

---

# Required Equipment

## Hardware

- Laptop
- Power Adapter
- Docking Station (if applicable)
- Monitor(s)
- Keyboard
- Mouse
- Headset

---

## Software

- Windows 11
- Microsoft 365
- Microsoft Teams
- Google Chrome
- Adobe Acrobat Reader
- Endpoint Protection Software
- VPN Client

---

# Pre-Deployment Checklist

Verify:

- Device powers on
- Device passes hardware inspection
- Charger included
- Asset tag assigned
- Serial number recorded
- No physical damage

---

# Asset Documentation

Record:

| Item | Example |
|---------|---------|
| Asset Tag | LT-1001 |
| Manufacturer | Dell |
| Model | Latitude 7440 |
| Serial Number | ABC123456 |
| Assigned User | John Tyler |
| Department | IT |
| Deployment Date | 06/04/2026 |

---

# Procedure

## Step 1: Hardware Inspection

Inspect laptop for:

- Physical damage
- Missing components
- Battery issues
- Screen damage
- Port damage

Document findings.

---

## Step 2: Install Operating System

Verify latest approved operating system is installed.

Example:

```text
Windows 11 Enterprise
```

Verify:

- Device activation
- Latest build version
- Company standards applied

---

## Step 3: Install Windows Updates

Navigate to:

```text
Settings > Windows Update
```

Install:

- Security Updates
- Feature Updates
- Driver Updates

Reboot if required.

---

## Step 4: Join Domain

Connect device to corporate network.

Join:

```text
corp.local
```

Verify:

- Domain Join Successful
- Computer Object Created
- Group Policies Applied

---

## Step 5: Configure User Account

Log in using assigned user account.

Verify:

- Active Directory Authentication
- User Profile Creation
- Home Directory Access

---

## Step 6: Install Standard Software

Install approved applications.

### Required Applications

```text
Microsoft 365
Microsoft Teams
Google Chrome
Adobe Acrobat Reader
VPN Client
```

Verify successful installation.

---

## Step 7: Configure Security Settings

Verify:

### Microsoft Defender

```text
Enabled
```

### Firewall

```text
Enabled
```

### BitLocker

```text
Enabled
```

### MFA

```text
Configured
```

### Endpoint Protection

```text
Installed and Active
```

---

# Security Validation

Verify:

- Antivirus Running
- Device Encryption Enabled
- Firewall Enabled
- Security Updates Current
- Screen Lock Policy Applied

---

# Step 8: Configure Email

Verify:

- Microsoft 365 Login
- Outlook Configuration
- Mailbox Synchronization

Send test email.

Confirm:

```text
Email Sending = Successful
Email Receiving = Successful
```

---

# Step 9: Configure VPN

Install VPN client.

Verify:

- Successful Authentication
- MFA Functionality
- Internal Resource Access

Test:

```text
VPN Connection
```

---

# Step 10: Configure Shared Resources

Verify access to:

- Shared Drives
- Department Folders
- Network Printers
- Business Applications

Examples:

```text
\\FILESERVER\Shared

\\FILESERVER\IT
```

---

# Step 11: Printer Configuration

Install required printers.

Verify:

- Printer Visible
- Test Page Prints Successfully

---

# Step 12: Validation Testing

Perform complete system validation.

Verify:

### Authentication

- User Login
- Domain Authentication

### Applications

- Microsoft Office
- Teams
- Chrome
- Adobe Reader

### Connectivity

- Internet Access
- VPN Access
- Shared Drive Access

### Hardware

- Keyboard
- Mouse
- Webcam
- Audio
- Microphone

---

# User Handoff Checklist

Review with employee:

- Login Process
- Password Policy
- MFA Enrollment
- VPN Usage
- Help Desk Contact Information

Provide:

- Laptop
- Charger
- Accessories

---

# Documentation Requirements

Update ticket with:

### Asset Information

```text
Asset Tag:
LT-1001

Serial Number:
ABC123456
```

### Assigned User

```text
John Tyler
```

### Applications Installed

```text
Microsoft 365
Teams
Chrome
Adobe Reader
VPN Client
```

### Deployment Status

```text
Completed
```

---

# Common Issues

## Domain Join Failure

Possible Causes:

- DNS Issues
- Network Connectivity
- Incorrect Credentials

Resolution:

- Verify DNS
- Verify Network Access
- Retry Join Process

---

## Software Installation Failure

Possible Causes:

- Corrupt Installer
- Insufficient Permissions
- Network Issues

Resolution:

- Re-download installer
- Run as Administrator
- Verify Connectivity

---

## VPN Connection Failure

Possible Causes:

- Incorrect Credentials
- MFA Failure
- VPN Server Issue

Resolution:

- Verify Credentials
- Verify MFA
- Contact Network Team

---

# Escalation Criteria

Escalate if:

- Domain Join Fails
- Security Software Fails
- Hardware Failure Detected
- Operating System Corruption Exists
- VPN Connectivity Cannot Be Established

---

# Success Criteria

Deployment is complete when:

- Device Fully Configured
- User Successfully Authenticated
- Software Installed
- Security Controls Enabled
- User Validated Functionality
- Documentation Complete

---

# Skills Demonstrated

- Windows Administration
- Active Directory
- Endpoint Management
- Device Deployment
- Microsoft 365 Administration
- VPN Configuration
- Asset Management
- Security Hardening
- Technical Documentation

---

# Related Procedures

- User Account Provisioning SOP
- New Employee Onboarding Playbook
- VPN Configuration SOP
- Asset Inventory Management SOP

---

# Revision History

| Version | Date | Description |
|-----------|-----------|-----------|
| 1.0 | June 2026 | Initial Release |
