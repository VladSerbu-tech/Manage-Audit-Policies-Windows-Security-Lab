# Manage Audit Policies Lab

## Lab Overview

Audit policies in Windows allow administrators to **track and record security-related events** occurring on a system. These records are essential for **security monitoring, troubleshooting, compliance, and incident investigations**.

In this lab, I explored how to view existing audit policies and apply policy updates using command-line tools.

---

# Lab Objectives

After completing this lab, I was able to:

- View default audit policies configured on a Windows system
- Understand different audit categories and what they monitor
- Apply Group Policy updates to enforce policy changes
- Identify where audit logs are stored
- Understand how to protect and manage audit logs

---

# Lab Environment

| Component | Description |
|---|---|
| Operating System | Windows Server / Windows Client |
| Interface | Command Prompt |
| Tools Used | auditpol, gpupdate, Event Viewer |

---

# Background Information

Windows uses **Audit Policies** to log activities related to system security. These logs help administrators answer questions such as:

- Who logged into the system?
- When was a policy changed?
- Which files were accessed?
- Were there any failed login attempts?

Audit policies are grouped into categories including:

- Account Logon
- Account Management
- Detailed Tracking
- Logon/Logoff
- Object Access
- Policy Change
- Privilege Use
- System

Each category can be configured to audit:

- **Success events**
- **Failure events**
- **Both**
- **None**

---

# Lab Tasks

## Task 1 – View Default Audit Policies

To view the current audit policy configuration, I used the following command:

```bash
auditpol /get /category:*
