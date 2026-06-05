# Active Directory User Creation Automation

## Document Information

| Field | Value |
|---------|---------|
| Automation ID | AUTO-002 |
| Title | Active Directory User Creation Automation |
| Department | IT Operations |
| Owner | Systems Administration Team |
| Version | 1.0 |
| Status | Active |
| Last Updated | June 2026 |

---

# Purpose

This automation workflow provisions new Active Directory user accounts automatically based on approved onboarding requests.

The objective is to reduce manual account creation tasks, improve consistency, minimize provisioning errors, and accelerate employee onboarding.

---

# Business Problem

Manual user creation introduces several challenges:

- Inconsistent account naming
- Incorrect group assignments
- Missing user attributes
- Delayed onboarding
- Administrative overhead

Automation ensures that all users are provisioned according to organizational standards.

---

# Scope

This workflow applies to:

- New Employees
- Contractors
- Temporary Employees
- Interns

The workflow provisions:

- Active Directory Accounts
- Organizational Unit Placement
- Group Memberships
- Password Configuration
- User Attributes

---

# Workflow Overview

```text
Approved Request Received
            │
            ▼
Automation Triggered
            │
            ▼
Validate User Data
            │
            ▼
Generate Username
            │
            ▼
Create AD Account
            │
            ▼
Assign Groups
            │
            ▼
Apply User Attributes
            │
            ▼
Enable Account
            │
            ▼
Generate Report
```

---

# Required Input Data

| Field | Required |
|---------|---------|
| First Name | Yes |
| Last Name | Yes |
| Department | Yes |
| Job Title | Yes |
| Manager | Yes |
| Office Location | Yes |
| Employee Type | Yes |

---

# Example Input

```text
First Name: John

Last Name: Tyler

Department: IT

Job Title: IT Support Technician

Manager: Jane Smith

Location: San Francisco

Employee Type: Full Time
```

---

# Step 1: Validate Request

Automation verifies:

- Request approved
- Required fields completed
- Manager assigned
- Department assigned

If validation fails:

```text
Request Rejected
```

Generate exception report.

---

# Step 2: Generate Username

Naming standard:

```text
firstname.lastname
```

Example:

```text
john.tyler
```

Alternative format:

```text
jtyler
```

Automation verifies username uniqueness.

---

# Username Conflict Handling

If username already exists:

```text
john.tyler1

john.tyler2
```

Generate next available username automatically.

---

# Step 3: Generate Temporary Password

Automation creates:

```text
Complex Temporary Password
```

Example:

```text
TempP@ss2026!
```

Requirements:

- Uppercase
- Lowercase
- Number
- Special Character
- Minimum 12 Characters

---

# Step 4: Create Active Directory User

Automation creates:

```text
User Object
```

Example PowerShell:

```powershell
New-ADUser `
-Name "John Tyler" `
-GivenName "John" `
-Surname "Tyler" `
-SamAccountName "jtyler"
```

---

# Step 5: Configure User Attributes

Populate:

```text
Display Name

Department

Title

Manager

Office

Email Address
```

---

# Example Attributes

```text
Display Name:
John Tyler

Department:
IT

Title:
IT Support Technician

Manager:
Jane Smith

Location:
San Francisco
```

---

# Step 6: Assign Organizational Unit

Examples:

```text
corp.local
│
├── Users
├── IT
├── HR
├── Finance
└── Contractors
```

Automation places user in correct OU.

---

# Step 7: Assign Security Groups

Department determines memberships.

---

## IT Department

```text
Domain Users

IT_Users

VPN_Users

SharedFolderUsers
```

---

## HR Department

```text
Domain Users

HR_Users

SharedFolderUsers
```

---

## Finance Department

```text
Domain Users

Finance_Users

SharedFolderUsers
```

---

# Step 8: Enable Account

Automation enables:

```text
User Account
```

Configuration:

```text
Enabled = Yes

Password Change Required = Yes
```

---

# Step 9: Create Home Directory

Example:

```text
\\FILESERVER\Users\jtyler
```

Permissions:

```text
Owner: User

Full Control: User

Administrators: Full Control
```

---

# Step 10: Generate Audit Log

Record:

```text
User Created

Date

Technician

Automation ID

Groups Assigned
```

Example:

```text
User:
jtyler

Created:
06/04/2026

Groups:
IT_Users
VPN_Users
Domain Users
```

---

# Validation Procedures

Verify:

## Active Directory

```text
Account Exists

Account Enabled

Attributes Correct
```

---

## Group Memberships

```text
Required Groups Assigned
```

---

## Organizational Unit

```text
Correct OU Placement
```

---

## Password Configuration

```text
Password Change Required
```

---

# Error Handling

## Duplicate User

Issue:

```text
Username Already Exists
```

Resolution:

```text
Generate Alternate Username
```

---

## Group Assignment Failure

Issue:

```text
Security Group Not Found
```

Resolution:

```text
Generate Alert

Escalate To Administrator
```

---

## OU Placement Failure

Issue:

```text
Organizational Unit Missing
```

Resolution:

```text
Create Exception Ticket
```

---

# Security Controls

Automation must:

- Require approved requests
- Enforce password standards
- Apply least privilege access
- Maintain audit logs
- Validate group assignments

---

# Benefits

## Faster Provisioning

Reduces account creation time.

---

## Improved Consistency

Standardizes user creation.

---

## Reduced Errors

Eliminates manual configuration mistakes.

---

## Better Compliance

Creates complete audit trail.

---

## Improved Security

Ensures correct permissions and password policies.

---

# Success Metrics

| Metric | Target |
|----------|----------|
| Account Creation Time | < 2 Minutes |
| Provisioning Accuracy | 99%+ |
| Failed Provisioning Rate | < 1% |
| Audit Log Completion | 100% |

---

# Technologies Involved

- Active Directory
- PowerShell
- Windows Server
- Group Policy
- Microsoft Entra ID
- Microsoft 365
- ServiceNow

---

# Skills Demonstrated

- Active Directory Administration
- PowerShell Automation
- Identity Management
- User Provisioning
- Process Automation
- Systems Administration
- IT Operations
- Security Administration
- Technical Documentation

---

# Related Documents

- User Account Provisioning SOP
- Automated User Onboarding
- VPN Configuration SOP
- New Employee Onboarding Playbook

---

# Future Enhancements

Planned improvements:

- Microsoft Graph API Integration
- ServiceNow Integration
- Automatic License Assignment
- Automated Welcome Email Generation
- Automated MFA Enrollment

---

# Revision History

| Version | Date | Description |
|-----------|-----------|-----------|
| 1.0 | June 2026 | Initial Release |
