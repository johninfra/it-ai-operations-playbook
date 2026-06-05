# VPN Configuration SOP

## Document Information

| Field | Value |
|---------|---------|
| SOP ID | SOP-006 |
| Title | VPN Configuration SOP |
| Department | Information Technology |
| Owner | IT Support Team |
| Version | 1.0 |
| Status | Active |
| Last Updated | June 2026 |

---

# Purpose

This Standard Operating Procedure (SOP) outlines the process for configuring, testing, and supporting Virtual Private Network (VPN) access for employees requiring secure remote connectivity.

The objective is to provide secure access to company resources while maintaining compliance with organizational security standards.

---

# Scope

This procedure applies to:

- Full Time Employees
- Remote Workers
- Contractors
- Hybrid Employees
- Authorized Third Party Users

Supported Platforms:

- Windows 10
- Windows 11
- macOS

---

# Roles and Responsibilities

## IT Support Technician

Responsible for:

- VPN account provisioning
- VPN client installation
- User support
- Connectivity testing
- Documentation

---

## Network Administrator

Responsible for:

- VPN infrastructure
- VPN gateways
- Security policies
- Escalation support

---

## End User

Responsible for:

- Maintaining credentials
- Protecting MFA devices
- Reporting connectivity issues

---

# Prerequisites

Before configuring VPN access, verify:

- User account exists
- User identity verified
- Manager approval received
- VPN access authorized
- MFA enrollment completed

---

# Required Information

| Item | Required |
|----------|----------|
| Username | Yes |
| Department | Yes |
| Manager Approval | Yes |
| VPN Access Group | Yes |
| MFA Enrollment | Yes |

---

# VPN Access Workflow

```text
VPN Access Request
        │
        ▼
Manager Approval
        │
        ▼
VPN Account Provisioning
        │
        ▼
MFA Verification
        │
        ▼
VPN Client Installation
        │
        ▼
Connectivity Testing
        │
        ▼
User Validation
```

---

# Procedure

## Step 1: Verify Request

Review ticket and verify:

- User identity
- Business justification
- Manager approval
- Department authorization

---

## Step 2: Verify Active Directory Account

Open:

```text
Active Directory Users and Computers
```

Locate user account.

Verify:

```text
Account Enabled = Yes
```

Confirm account is active.

---

## Step 3: Assign VPN Access Group

Navigate to:

```text
Member Of
```

Add user to VPN security group.

Example:

```text
VPN_Users
```

Verify membership has been applied.

---

## Step 4: Verify MFA Enrollment

Confirm user is enrolled in Multi Factor Authentication.

Examples:

```text
Microsoft Authenticator
```

```text
Duo Security
```

```text
Okta Verify
```

Verify successful enrollment.

---

## Step 5: Install VPN Client

Install approved VPN software.

Examples:

```text
Cisco AnyConnect
```

```text
GlobalProtect
```

```text
FortiClient
```

```text
OpenVPN
```

Verify installation completes successfully.

---

## Step 6: Configure VPN Profile

Enter required information.

Example:

```text
VPN Server:
vpn.company.com
```

Authentication Method:

```text
Username and Password
```

Additional Security:

```text
MFA Required
```

Save configuration.

---

## Step 7: Test Authentication

Attempt login using:

```text
Domain Username
```

Example:

```text
jtyler
```

Verify:

- Credentials accepted
- MFA challenge received
- Authentication successful

---

## Step 8: Verify VPN Connection

Connect to VPN.

Confirm:

```text
Status: Connected
```

Verify assigned VPN IP address.

Example:

```text
10.10.50.25
```

---

## Step 9: Verify Internal Resource Access

Test connectivity to internal systems.

### File Server

```text
\\FILESERVER\Shared
```

### Domain Controller

```text
ping dc1.corp.local
```

### Internal Website

```text
https://intranet.company.local
```

Verify successful access.

---

## Step 10: Validate Business Applications

Confirm access to:

- Microsoft 365
- Shared Drives
- Internal Applications
- Remote Desktop Resources
- Ticketing Systems

Document results.

---

# Validation Checklist

Verify:

- VPN Client Installed
- User Authenticated
- MFA Working
- Internal Resources Accessible
- Business Applications Functional
- Ticket Updated

---

# Connectivity Testing

## Internet Connectivity

Run:

```text
ping 8.8.8.8
```

Expected Result:

```text
Successful Reply
```

---

## DNS Resolution

Run:

```text
nslookup company.com
```

Expected Result:

```text
Successful DNS Resolution
```

---

## Internal Resource Test

Run:

```text
ping dc1.corp.local
```

Expected Result:

```text
Successful Reply
```

---

# Common Issues

## Authentication Failure

Possible Causes:

- Incorrect password
- Account locked
- MFA failure

Resolution:

- Verify credentials
- Verify account status
- Verify MFA enrollment

---

## Unable to Reach VPN Server

Possible Causes:

- Internet outage
- Firewall restriction
- VPN gateway outage

Resolution:

- Verify internet access
- Test alternate network
- Escalate to Network Team

---

## Connected but No Internal Access

Possible Causes:

- DNS issues
- Routing issues
- Group membership issue

Resolution:

- Verify DNS
- Verify VPN permissions
- Verify routing configuration

---

## MFA Not Working

Possible Causes:

- Authenticator not enrolled
- Mobile device issue
- Expired enrollment

Resolution:

- Re-enroll MFA
- Verify device registration
- Reset MFA configuration

---

# Security Requirements

Always:

- Require MFA
- Use approved VPN clients
- Verify user identity
- Follow least privilege principles
- Document all access requests

Never:

- Share credentials
- Disable MFA
- Grant unauthorized VPN access
- Use unapproved VPN software

---

# Ticket Documentation

Record:

### User Information

```text
Username:
jtyler

Department:
IT
```

### VPN Configuration

```text
VPN Client:
Cisco AnyConnect

VPN Group:
VPN_Users
```

### Validation Results

```text
Authentication Successful

MFA Successful

Internal Resources Accessible
```

### Status

```text
Completed
```

---

# Escalation Criteria

Escalate if:

- VPN server unavailable
- Multiple users affected
- MFA system failure
- Routing issues identified
- Security incident suspected

---

# Success Criteria

VPN setup is complete when:

- User authenticated successfully
- MFA functioning properly
- VPN connection established
- Internal resources accessible
- Documentation completed

---

# Skills Demonstrated

- VPN Administration
- Network Troubleshooting
- Active Directory
- Multi Factor Authentication
- Remote Access Support
- Identity Management
- IT Support Operations
- Technical Documentation

---

# Related Procedures

- User Account Provisioning SOP
- Password Reset SOP
- Account Lockout Resolution SOP
- Laptop Deployment Procedure

---

# Revision History

| Version | Date | Description |
|-----------|-----------|-----------|
| 1.0 | June 2026 | Initial Release |
