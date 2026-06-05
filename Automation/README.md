# Automation

## Overview

This folder contains enterprise IT automation workflows designed to reduce manual administrative effort, improve consistency, strengthen security, and streamline service desk operations.

These automations represent common tasks performed by IT Support, System Administration, Active Directory Administration, and Security Operations teams.

The objective is to automate repetitive workflows while maintaining operational accuracy, security, and documentation standards.

---

## Objectives

- Reduce repetitive administrative tasks
- Improve service desk efficiency
- Accelerate user provisioning
- Improve onboarding consistency
- Reduce password related support tickets
- Improve security response times
- Standardize ticket routing processes
- Enhance operational scalability
- Improve auditability and documentation

---

## Core Automation Principles

### Standardization

Automation ensures tasks are completed consistently every time.

Benefits include:

- Reduced human error
- Faster execution
- Improved compliance
- Better operational visibility

---

### Security First

Automation should follow enterprise security best practices.

Examples:

- Least privilege access
- Role based permissions
- Audit logging
- Approval workflows
- Credential protection

---

### Documentation Driven

Automation workflows should generate documentation whenever possible.

Examples:

- User creation logs
- Security alert reports
- Ticket updates
- Notification records
- Audit trails

---

### Human Oversight

Automation assists administrators and technicians.

Critical actions should still be reviewed when appropriate.

---

## Repository Structure

```text
Automation/
│
├── Active-Directory-User-Creation-Automation.md
├── Automated-User-Onboarding.md
├── Password-Expiration-Notification-Automation.md
├── Security-Alert-Automation.md
└── Ticket-Routing-Automation.md
```

---

# Automation Workflows

## 1. Active Directory User Creation Automation

### Purpose

Automate the creation of new Active Directory user accounts while ensuring consistency across naming conventions, organizational units, and security group assignments.

### Workflow

1. Receive new user information
2. Create Active Directory account
3. Configure user attributes
4. Place user in correct Organizational Unit
5. Assign security groups
6. Enable account
7. Log account creation

### Benefits

- Faster account provisioning
- Reduced administrative workload
- Consistent account creation
- Improved accuracy

---

## 2. Automated User Onboarding

### Purpose

Automate the onboarding process for newly hired employees.

### Workflow

1. HR submits onboarding request
2. Create user account
3. Assign department groups
4. Provision applications
5. Configure access permissions
6. Generate onboarding documentation
7. Notify management and IT teams

### Benefits

- Faster onboarding
- Improved user experience
- Consistent provisioning
- Reduced manual effort

---

## 3. Password Expiration Notification Automation

### Purpose

Automatically notify users before passwords expire to reduce account lockouts and help desk requests.

### Workflow

1. Query Active Directory
2. Identify users with upcoming password expirations
3. Generate notification messages
4. Send reminder emails
5. Log notification activity

### Notification Schedule

- 14 Days Before Expiration
- 7 Days Before Expiration
- 3 Days Before Expiration
- 1 Day Before Expiration

### Benefits

- Reduced lockouts
- Fewer password reset tickets
- Improved user awareness
- Better compliance

---

## 4. Security Alert Automation

### Purpose

Automate the processing and notification of security related events and alerts.

### Input Sources

- SIEM Platforms
- Endpoint Security Tools
- Firewall Logs
- Authentication Logs
- Event Viewer Logs

### Workflow

1. Receive security alert
2. Determine severity level
3. Generate summary
4. Notify administrators
5. Create investigation ticket
6. Log activity

### Benefits

- Faster incident response
- Improved visibility
- Reduced analyst workload
- Consistent alert handling

---

## 5. Ticket Routing Automation

### Purpose

Automatically categorize and route support tickets to the correct teams.

### Workflow

1. Analyze ticket description
2. Determine category
3. Determine priority
4. Identify support team
5. Route ticket
6. Log routing decision

### Example Categories

- Network Support
- Active Directory
- Microsoft 365
- Endpoint Support
- Security Operations
- Infrastructure

### Benefits

- Faster response times
- Improved routing accuracy
- Reduced service desk workload
- Improved SLA performance

---

# Technologies & Platforms

These automation workflows are based on concepts commonly used with:

- Active Directory
- Windows Server
- PowerShell
- Microsoft 365
- Azure / Entra ID
- ServiceNow
- Jira Service Management
- Microsoft Defender
- SIEM Platforms
- Enterprise Ticketing Systems

---

# Skills Demonstrated

- IT Automation
- Active Directory Administration
- Windows Server Administration
- User Lifecycle Management
- IT Service Management
- Incident Management
- Security Operations
- Process Automation
- Identity and Access Management
- Enterprise IT Operations
- Technical Documentation
- Workflow Design

---

# Real World Applications

These workflows are commonly used in:

- Corporate IT Departments
- Managed Service Providers (MSPs)
- Healthcare Organizations
- Financial Institutions
- Educational Institutions
- Government Agencies
- Security Operations Centers (SOCs)

---

# Future Enhancements

Planned additions:

- User Offboarding Automation
- Group Membership Automation
- Microsoft 365 License Assignment Automation
- Asset Management Automation
- Vulnerability Reporting Automation
- Compliance Reporting Automation
- AI Assisted IT Operations Automation

---

# Author

**John Tyler**

IT Support | System Administration | Cybersecurity | AI Operations

This repository demonstrates practical enterprise automation workflows used to streamline IT operations, improve security, reduce manual administrative effort, and support scalable enterprise environments.
