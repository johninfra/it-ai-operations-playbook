# Password Expiration Notification Automation

## Document Information

| Field | Value |
|---------|---------|
| Automation ID | AUTO-003 |
| Title | Password Expiration Notification Automation |
| Department | IT Operations |
| Owner | Systems Administration Team |
| Version | 1.0 |
| Status | Active |
| Last Updated | June 2026 |

---

# Purpose

This automation workflow identifies users with passwords approaching expiration and automatically sends notifications reminding them to change their password before expiration.

The objective is to reduce account lockouts, decrease Help Desk ticket volume, and improve user experience.

---

# Business Problem

Many password-related incidents occur because users are unaware their password is about to expire.

Common issues include:

- Account lockouts
- Password expiration
- Increased Help Desk tickets
- Lost productivity
- Authentication failures
- VPN access disruptions

Automation provides proactive notification before expiration occurs.

---

# Scope

This workflow applies to:

- Active Directory Users
- Hybrid Users
- Microsoft 365 Users
- VPN Users

This workflow excludes:

- Service Accounts
- Shared Accounts
- Disabled Accounts

---

# Workflow Overview

```text
Scheduled Task Runs
         │
         ▼
Query Active Directory
         │
         ▼
Identify Expiring Passwords
         │
         ▼
Generate User List
         │
         ▼
Send Notifications
         │
         ▼
Generate Report
         │
         ▼
Archive Results
```

---

# Automation Schedule

Frequency:

```text
Daily
```

Execution Time:

```text
7:00 AM
```

Notification Windows:

```text
14 Days Before Expiration

7 Days Before Expiration

3 Days Before Expiration

1 Day Before Expiration
```

---

# Data Sources

Automation retrieves information from:

- Active Directory
- Microsoft Entra ID
- Microsoft 365
- User Directory Services

---

# User Information Retrieved

| Field | Example |
|---------|---------|
| Username | jtyler |
| Display Name | John Tyler |
| Email Address | john.tyler@company.com |
| Password Expiration Date | 06/18/2026 |
| Days Remaining | 14 |

---

# Step 1: Query Active Directory

Automation searches Active Directory.

Example PowerShell:

```powershell
Get-ADUser -Filter *
```

Retrieve:

- Username
- Email Address
- Password Last Set
- Password Expiration Date

---

# Step 2: Calculate Remaining Days

Determine:

```text
Expiration Date - Current Date
```

Example:

```text
Expiration Date:
06/18/2026

Current Date:
06/04/2026

Days Remaining:
14
```

---

# Step 3: Filter Users

Identify users within notification thresholds.

Examples:

```text
14 Days Remaining

7 Days Remaining

3 Days Remaining

1 Day Remaining
```

---

# Step 4: Generate Notification List

Example Output:

```text
John Tyler
14 Days Remaining

Sarah Johnson
7 Days Remaining

Michael Davis
3 Days Remaining
```

---

# Step 5: Generate Notification Email

Example Email:

## Subject

```text
Password Expiration Notice
```

---

## Body

```text
Hello John Tyler,

Your company password will expire in 14 days.

Please update your password before expiration to avoid account access issues.

If you require assistance, contact the IT Help Desk.

Thank you,
IT Operations
```

---

# Step 6: Send Email

Notification sent using:

- Microsoft 365
- Exchange Online
- SMTP Service

Verify successful delivery.

---

# Step 7: Generate Daily Report

Example Report:

```text
Date:
06/04/2026

Users Notified:
42

14 Day Notices:
20

7 Day Notices:
12

3 Day Notices:
6

1 Day Notices:
4
```

---

# Step 8: Archive Results

Store:

- Notification Date
- User
- Delivery Status
- Expiration Date

For auditing and compliance purposes.

---

# Escalation Notifications

If password expires:

Automation may notify:

- User
- Manager
- IT Help Desk

Example:

```text
User Password Expired

Username:
jtyler

Expiration Date:
06/18/2026
```

---

# Example PowerShell Workflow

```powershell
Get-ADUser `
-Filter * `
-Properties PasswordLastSet
```

Calculate:

```powershell
PasswordExpirationDate
```

Send:

```powershell
Send-MailMessage
```

Generate:

```powershell
CSV Report
```

---

# Validation Procedures

Verify:

## Active Directory

```text
User Retrieved Successfully
```

---

## Email Delivery

```text
Email Sent Successfully
```

---

## Reporting

```text
Report Generated Successfully
```

---

## Logging

```text
Audit Log Created
```

---

# Error Handling

## User Has No Email Address

Action:

```text
Skip User

Log Exception
```

---

## Email Delivery Failure

Action:

```text
Retry Delivery

Generate Alert
```

---

## Active Directory Query Failure

Action:

```text
Generate Critical Alert

Escalate To Administrator
```

---

# Security Controls

Automation must:

- Use secure authentication
- Protect user information
- Log all activity
- Follow organizational email policies
- Restrict administrative access

---

# Benefits

## Reduced Help Desk Tickets

Users proactively update passwords.

---

## Improved User Experience

Reduces unexpected lockouts.

---

## Better Security

Encourages timely password changes.

---

## Increased Productivity

Users maintain uninterrupted access.

---

## Improved Compliance

Supports password management policies.

---

# Success Metrics

| Metric | Target |
|----------|----------|
| Notification Delivery Rate | 99%+ |
| Password Expiration Incidents | Reduced 50%+ |
| Password Related Tickets | Reduced 30%+ |
| Audit Log Completion | 100% |

---

# Technologies Involved

- Active Directory
- Windows Server
- PowerShell
- Microsoft 365
- Exchange Online
- Microsoft Entra ID
- SMTP Services

---

# Skills Demonstrated

- PowerShell Automation
- Active Directory Administration
- Identity Management
- Microsoft 365 Administration
- Email Automation
- Systems Administration
- IT Operations
- Process Automation
- Technical Documentation

---

# Related Documents

- Active Directory User Creation Automation
- Automated User Onboarding
- Password Reset SOP
- Account Lockout Resolution SOP

---

# Future Enhancements

Planned improvements:

- Microsoft Teams Notifications
- SMS Notifications
- Self Service Password Reset Integration
- Manager Escalation Workflow
- Password Health Dashboard

---

# Revision History

| Version | Date | Description |
|-----------|-----------|-----------|
| 1.0 | June 2026 | Initial Release |
