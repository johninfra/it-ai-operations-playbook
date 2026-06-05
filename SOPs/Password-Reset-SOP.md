# Password Reset SOP

## Document Information

| Field | Value |
|---------|---------|
| SOP ID | SOP-003 |
| Title | Password Reset Procedure |
| Department | Information Technology |
| Owner | IT Support Team |
| Version | 1.0 |
| Status | Active |
| Last Updated | June 2026 |

---

# Purpose

This Standard Operating Procedure (SOP) outlines the process for securely resetting user passwords within the organization's identity management systems.

The objective is to restore user access while maintaining security, compliance, and proper documentation.

---

# Scope

This procedure applies to:

- Active Directory User Accounts
- Microsoft 365 Accounts
- VPN Accounts
- Internal Business Applications
- Domain User Accounts

This SOP does not apply to:

- Administrative Service Accounts
- Domain Administrator Accounts
- Privileged Security Accounts

These accounts require Systems Administrator approval.

---

# Roles and Responsibilities

## End User

Responsible for:

- Requesting password reset assistance
- Verifying identity
- Creating a new secure password

---

## IT Support Technician

Responsible for:

- Verifying user identity
- Resetting passwords
- Documenting actions taken
- Confirming successful login

---

## Systems Administrator

Responsible for:

- Escalated password issues
- Account synchronization problems
- Administrative account resets

---

# Password Reset Requirements

Passwords must comply with organizational standards.

Minimum requirements:

- Minimum 12 characters
- Uppercase letter
- Lowercase letter
- Number
- Special character

Example:

```text
MySecurePassword2026!
```

Users should avoid:

- Names
- Birthdays
- Company names
- Common dictionary words

---

# Identity Verification

Before performing a password reset, verify the user's identity.

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

Manager Approval

Manager confirms password reset request.

---

# Procedure

## Step 1: Verify Request

Review support ticket.

Confirm:

- User identity
- Account ownership
- Password reset requirement

If identity cannot be verified, escalate to management.

---

## Step 2: Open Active Directory Users and Computers

Launch:

```text
Active Directory Users and Computers
```

Navigate to the user account.

Example:

```text
corp.local
 └── Users
      └── John Tyler
```

---

## Step 3: Locate User Account

Search for the account.

Verify:

- Username
- Full Name
- Department

Ensure correct account selection.

---

## Step 4: Reset Password

Right-click user account.

Select:

```text
Reset Password
```

Enter temporary password.

Example:

```text
TempPassword2026!
```

Enable:

```text
User must change password at next logon
```

Click:

```text
OK
```

---

## Step 5: Unlock Account (If Necessary)

If account is locked:

Right-click account.

Select:

```text
Properties
```

Navigate to:

```text
Account Tab
```

Enable:

```text
Unlock Account
```

Apply changes.

---

## Step 6: Verify Account Status

Confirm:

```text
Account Enabled = Yes
```

Verify:

```text
Account Locked = No
```

---

## Step 7: Communicate Temporary Password

Provide temporary password through approved communication channels.

Approved methods:

- Company phone call
- Secure messaging platform
- Verified email procedure

Never send passwords through unsecured channels.

---

## Step 8: User Login Verification

Ask user to:

1. Log in using temporary password.
2. Create a new password.
3. Confirm successful login.

Verify:

- Windows Login
- Microsoft 365 Access
- Email Access
- VPN Access

---

# Validation Checklist

Verify:

- Password successfully reset
- User can authenticate
- Account unlocked
- Applications accessible
- Ticket updated

---

# Common Issues

## User Cannot Change Password

Possible Causes:

- Password complexity requirements not met
- Replication delay
- Group Policy issue

Resolution:

- Verify password policy
- Wait for replication
- Escalate if necessary

---

## Password Reset Not Working

Possible Causes:

- Wrong account selected
- Replication issue
- Azure AD synchronization issue

Resolution:

- Verify account
- Check replication
- Escalate to Systems Administrator

---

## Account Remains Locked

Possible Causes:

- Multiple devices using old password
- Mobile device authentication attempts
- Cached credentials

Resolution:

- Update saved credentials
- Remove old passwords
- Restart affected devices

---

# Security Considerations

Always:

- Verify user identity
- Follow password policies
- Document all password resets
- Require password changes at next login

Never:

- Share passwords publicly
- Reuse passwords
- Bypass identity verification
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

### Actions Taken

```text
Password Reset Completed

Temporary Password Assigned

Account Unlocked
```

---

### Validation

```text
User Successfully Logged In

Password Changed

Ticket Resolved
```

---

# Escalation Criteria

Escalate if:

- Password reset fails
- Account synchronization issues occur
- Azure AD issues exist
- Multiple account lockouts occur
- Administrative accounts require reset

---

# Success Criteria

Password reset is complete when:

- User identity verified
- Password reset successfully
- User can log in
- Account unlocked
- Ticket updated and closed

---

# Related Procedures

- User Account Provisioning SOP
- Account Lockout Resolution SOP
- VPN Configuration SOP
- Employee Offboarding Procedure

---

# Skills Demonstrated

- Active Directory
- Microsoft 365 Administration
- User Management
- Identity Verification
- Access Management
- IT Support Operations
- Security Best Practices
- Documentation

---

# Revision History

| Version | Date | Description |
|-----------|-----------|-----------|
| 1.0 | June 2026 | Initial Release |
