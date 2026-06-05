# Account Lockout Resolution SOP

## Document Information

| Field | Value |
|---------|---------|
| SOP ID | SOP-004 |
| Title | Account Lockout Resolution Procedure |
| Department | Information Technology |
| Owner | IT Support Team |
| Version | 1.0 |
| Status | Active |
| Last Updated | June 2026 |

---

# Purpose

This Standard Operating Procedure (SOP) outlines the process for identifying, investigating, and resolving user account lockouts within the organization's authentication systems.

The objective is to restore user access while identifying the root cause of the lockout and preventing future occurrences.

---

# Scope

This procedure applies to:

- Active Directory User Accounts
- Microsoft 365 Accounts
- VPN Accounts
- Domain User Accounts

This procedure does not apply to:

- Service Accounts
- Domain Administrator Accounts
- Privileged Security Accounts

These require Systems Administrator involvement.

---

# Roles and Responsibilities

## End User

Responsible for:

- Reporting lockout issues
- Verifying identity
- Testing login access after resolution

---

## IT Support Technician

Responsible for:

- Verifying identity
- Unlocking accounts
- Investigating root cause
- Documenting actions taken

---

## Systems Administrator

Responsible for:

- Persistent lockout investigations
- Replication issues
- Authentication infrastructure problems

---

# Common Causes of Account Lockouts

## Incorrect Password Entry

Examples:

- User forgot password
- User entered incorrect password multiple times

---

## Cached Credentials

Examples:

- Outlook using old password
- Saved Windows credentials
- Mapped network drives

---

## Mobile Devices

Examples:

- Phone email application
- Microsoft Authenticator
- Company applications

---

## Service Dependencies

Examples:

- Scheduled Tasks
- Services using old credentials
- Scripts using outdated passwords

---

## Security Events

Examples:

- Brute force attempts
- Unauthorized login attempts
- Account compromise

---

# Identity Verification

Before unlocking an account, verify user identity.

Acceptable methods include:

### Method 1

Verify:

- Full Name
- Employee ID
- Department

---

### Method 2

Verify:

- Manager Name
- Office Location
- Company Email Address

---

### Method 3

Manager Confirmation

Manager approves unlock request.

---

# Procedure

## Step 1: Verify Request

Review support ticket.

Confirm:

- User identity
- Account ownership
- Lockout symptoms

---

## Step 2: Open Active Directory Users and Computers

Launch:

```text
Active Directory Users and Computers
```

Navigate to:

```text
corp.local
 └── Users
```

Locate user account.

---

## Step 3: Verify Lockout Status

Right-click account.

Select:

```text
Properties
```

Navigate to:

```text
Account Tab
```

Verify whether:

```text
Account is locked out
```

is enabled.

---

## Step 4: Unlock Account

Enable:

```text
Unlock Account
```

Click:

```text
Apply
```

Then:

```text
OK
```

---

## Step 5: Verify Account Status

Confirm:

```text
Account Enabled = Yes
```

Confirm:

```text
Account Locked = No
```

---

## Step 6: Investigate Root Cause

Determine why the lockout occurred.

Questions to ask:

- Did the user recently change passwords?
- Are multiple devices connected?
- Are old credentials stored?
- Are applications repeatedly attempting authentication?

---

## Step 7: Check Cached Credentials

Verify:

### Windows Credential Manager

Remove outdated credentials.

---

### Outlook

Verify current password.

---

### Mobile Devices

Verify:

- Email apps
- Teams
- OneDrive
- VPN clients

---

## Step 8: Review Event Logs

If lockouts continue:

Open:

```text
Event Viewer
```

Review:

```text
Security Logs
```

Look for:

```text
Event ID 4740
```

This event identifies the source of the lockout.

---

## Step 9: Verify Login

Ask user to:

1. Sign in
2. Access email
3. Access Microsoft 365
4. Access VPN if required

Confirm successful authentication.

---

# Troubleshooting Guide

## Repeated Lockouts

Possible Causes:

- Mobile device using old password
- Outlook profile issue
- Scheduled task
- VPN client

Recommended Actions:

- Update credentials
- Restart device
- Remove saved passwords

---

## User Can Log In But Lockout Returns

Possible Causes:

- Cached credentials
- Multiple connected devices
- Authentication loop

Recommended Actions:

- Review Event ID 4740
- Identify source device
- Remove outdated credentials

---

## Account Unlock Not Working

Possible Causes:

- Domain replication issue
- Group Policy issue
- Account disabled

Recommended Actions:

- Verify replication
- Verify account status
- Escalate to Systems Administrator

---

# Security Considerations

Always:

- Verify user identity
- Investigate repeated lockouts
- Review authentication logs
- Document actions taken

Never:

- Ignore repeated lockouts
- Unlock accounts without verification
- Disable security controls

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

---

### Root Cause

```text
Outlook using outdated credentials
```

---

### Actions Taken

```text
Account Unlocked

Credentials Updated

User Verified Access
```

---

### Resolution

```text
Issue Resolved

No Further Lockouts Observed
```

---

# Escalation Criteria

Escalate if:

- Lockouts continue after resolution
- Event logs indicate suspicious activity
- Replication issues exist
- Multiple users affected
- Security incident suspected

---

# Success Criteria

Procedure is complete when:

- User identity verified
- Account unlocked
- Root cause identified
- User successfully logged in
- Ticket updated and closed

---

# Skills Demonstrated

- Active Directory Administration
- Event Viewer Analysis
- Authentication Troubleshooting
- User Management
- Security Investigation
- IT Support Operations
- Root Cause Analysis
- Technical Documentation

---

# Related Procedures

- Password Reset SOP
- User Account Provisioning SOP
- VPN Configuration SOP
- Employee Offboarding Procedure

---

# Revision History

| Version | Date | Description |
|-----------|-----------|-----------|
| 1.0 | June 2026 | Initial Release |
