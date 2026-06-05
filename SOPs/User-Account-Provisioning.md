# User Account Provisioning SOP

## Document Information

| Field | Value |
|---------|---------|
| SOP ID | SOP-001 |
| Title | User Account Provisioning |
| Department | Information Technology |
| Owner | IT Operations |
| Version | 1.0 |
| Status | Active |
| Last Updated | June 2026 |

---

# Purpose

This Standard Operating Procedure (SOP) outlines the process for creating, configuring, and validating user accounts within the organization's Active Directory environment.

The objective is to ensure users receive appropriate access while maintaining security, compliance, and operational consistency.

---

# Scope

This procedure applies to:

- Full-time employees
- Part-time employees
- Contractors
- Temporary staff
- Interns

This SOP covers:

- Active Directory account creation
- Group membership assignment
- Microsoft 365 provisioning
- Access validation
- Documentation requirements

---

# Roles and Responsibilities

## Hiring Manager

Responsible for:

- Submitting access requests
- Defining required permissions
- Approving resource access

## IT Support Technician

Responsible for:

- Creating user accounts
- Assigning permissions
- Verifying access
- Documenting completion

## Systems Administrator

Responsible for:

- Managing Active Directory infrastructure
- Resolving provisioning failures
- Escalation support

---

# Prerequisites

Before creating an account, verify:

- Approved onboarding request exists
- Employee start date is confirmed
- Department information is available
- Manager information is available
- Required access has been approved

---

# Required Information

The following information must be provided:

| Information | Required |
|------------|------------|
| First Name | Yes |
| Last Name | Yes |
| Department | Yes |
| Job Title | Yes |
| Manager | Yes |
| Start Date | Yes |
| Email Address | Yes |
| Office Location | Yes |

---

# Procedure

## Step 1: Verify Request

Review onboarding ticket and confirm:

- Employee details are accurate
- Manager approval exists
- Access requirements are documented

If information is incomplete, return the request to the hiring manager.

---

## Step 2: Open Active Directory Users and Computers

Launch:

```text
Active Directory Users and Computers (ADUC)
```

Navigate to the appropriate Organizational Unit (OU).

Example:

```text
corp.local
 └── Users
```

---

## Step 3: Create User Account

Right-click the appropriate OU.

Select:

```text
New → User
```

Enter:

- First Name
- Last Name
- Full Name
- Username

### Username Standard

Example naming convention:

```text
john.tyler
```

or

```text
jtyler
```

Follow company standards.

Click:

```text
Next
```

---

## Step 4: Configure Password

Assign a temporary password.

Example:

```text
TempPassword2026!
```

Enable:

```text
User must change password at next logon
```

Verify:

```text
Password never expires = Disabled
```

Click:

```text
Finish
```

---

## Step 5: Populate User Attributes

Open user properties.

Update:

### General Tab

- Office
- Phone Number
- Email Address

### Organization Tab

- Title
- Department
- Manager

### Address Tab

- Office Location

Save changes.

---

## Step 6: Assign Group Memberships

Navigate to:

```text
Member Of
```

Add required groups.

Examples:

### Standard Groups

```text
Domain Users
```

### Department Groups

```text
HR_Users
Finance_Users
IT_Users
```

### Application Groups

```text
VPN_Users
Microsoft365_Users
SharedFolderUsers
```

Verify memberships before proceeding.

---

## Step 7: Configure Email Access

Create Microsoft 365 account.

Verify:

- User mailbox exists
- License assigned
- Email address configured

Example:

```text
john.tyler@company.com
```

---

## Step 8: Configure VPN Access

If required:

Add user to:

```text
VPN_Users
```

Verify VPN permissions are assigned.

---

## Step 9: Configure Shared Resource Access

Grant access to:

- Shared drives
- Department folders
- Printers
- Internal applications

Examples:

```text
\\FILESERVER\HR

\\FILESERVER\Finance

\\FILESERVER\Shared
```

Follow least privilege principles.

---

## Step 10: Validation Testing

Verify:

### Active Directory

- User account exists
- Account is enabled
- Group memberships correct

### Email

- Mailbox created
- Email sending functional

### VPN

- Access assigned

### Shared Resources

- Folder permissions working

### Applications

- Required applications accessible

---

# Documentation Requirements

Update ticket with:

- Username
- Email Address
- Assigned Groups
- Date Completed
- Technician Name

Example:

```text
User Created: john.tyler

Email:
john.tyler@company.com

Groups:
Domain Users
VPN_Users
SharedFolderUsers

Completed By:
John Tyler

Date:
06/04/2026
```

---

# Escalation Criteria

Escalate to Systems Administrator if:

- Active Directory replication fails
- Account creation errors occur
- Group Policy issues occur
- Exchange provisioning fails
- Azure AD synchronization fails
- Licensing issues occur

---

# Security Requirements

Always:

- Follow least privilege principles
- Assign only approved access
- Require password changes at first login
- Verify manager approval before granting access
- Document all actions performed

Never:

- Share passwords through unsecured channels
- Grant unauthorized permissions
- Create accounts without approval

---

# Completion Checklist

## Account Creation

- [ ] User created
- [ ] Password configured
- [ ] User enabled

## Configuration

- [ ] Department assigned
- [ ] Manager assigned
- [ ] Email configured

## Access

- [ ] Groups assigned
- [ ] VPN assigned
- [ ] Shared folders assigned

## Validation

- [ ] Account verified
- [ ] Email verified
- [ ] Access verified

## Documentation

- [ ] Ticket updated
- [ ] Request completed

---

# Related Procedures

- New Employee Onboarding Playbook
- Password Reset SOP
- Account Lockout Resolution SOP
- Employee Offboarding Procedure
- VPN Configuration SOP

---

# Revision History

| Version | Date | Description |
|-----------|-----------|-----------|
| 1.0 | June 2026 | Initial Release |
