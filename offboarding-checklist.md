# Employee Offboarding Checklist

Secure procedure for removing employee access when they leave the company.

---

## 📋 Overview

When an employee leaves (resignation, termination, or retirement), IT must **remove all access quickly and securely**. This prevents:
- Unauthorized access to company data
- Security breaches
- License waste
- Compliance violations

---

## ⚠️ Timing Matters

| Departure Type | When to Disable Access |
|----------------|----------------------|
| **Voluntary resignation** | Last day of work, end of business |
| **Involuntary termination** | Immediately (coordinate with HR) |
| **Retirement** | Last day of work |
| **Contractor end** | Contract end date |

**For terminations:** HR will typically call IT before/during the termination meeting. Be ready to disable instantly.

---

## ✅ Offboarding Checklist

### 1. Account Access (Do Immediately)

```
☐ Disable user account in Entra ID / Active Directory
   - Do NOT delete yet (may need for audit/legal)
   - Set "Block sign-in" = Yes

☐ Reset password (prevents last-minute access)

☐ Revoke all active sessions
   - Entra ID → User → Revoke sessions

☐ Disable MFA devices
   - Remove registered phones/authenticators

☐ Remove from all security groups
   - Department groups
   - Access groups
   - Distribution lists

☐ Revoke VPN access
   - Disable in VPN management system

☐ Disable remote access
   - Remove from any remote access tools
```

### 2. Email & Communication

```
☐ Set Out of Office message (if appropriate)
   Example: "I am no longer with [Company]. Please contact 
   [alternate contact] at [email] for assistance."

☐ Email forwarding (if approved by manager)
   - Forward to manager or designated person
   - Set expiration date (typically 30-90 days)

☐ Convert mailbox to shared mailbox (optional)
   - Allows manager to access without license

☐ Remove from Teams/Slack
   - Remove from channels and teams

☐ Revoke calendar sharing
   - Remove delegates
```

### 3. Applications & Services

```
☐ Revoke access to business applications
   - Salesforce
   - Workday
   - Jira
   - Any department-specific apps

☐ Remove from cloud services
   - AWS accounts
   - Azure subscriptions
   - Google Cloud

☐ Disable single sign-on (SSO) access
   - All SSO-connected apps revoked automatically
   
☐ Revoke API keys and tokens
   - Check with development team if applicable
```

### 4. Data & Files

```
☐ Back up user's data (if required)
   - OneDrive files
   - Local documents
   - Email archive

☐ Transfer file ownership
   - OneDrive files to manager
   - SharePoint permissions

☐ Check for shared files
   - Ensure nothing breaks when access removed

☐ Preserve data for legal hold (if required)
   - HR/Legal will advise if needed
```

### 5. Equipment Recovery

```
☐ Laptop returned
   - Asset tag: _______________
   - Condition noted

☐ Mobile devices returned (company-owned)
   - Phone
   - Tablet

☐ Peripherals returned
   - Monitor(s)
   - Keyboard/mouse
   - Headset
   - Docking station

☐ Access cards / badges returned

☐ Keys returned (if any)

☐ Wipe devices
   - Factory reset phones
   - Reimage laptop for next user
```

### 6. Licenses

```
☐ Remove Microsoft 365 license
   - Save ~$20/month per user

☐ Remove other software licenses
   - Adobe Creative Cloud
   - Zoom
   - Any paid subscriptions

☐ Update license inventory
```

### 7. Documentation

```
☐ Update asset inventory
   - Mark equipment as returned

☐ Update user directory
   - Remove from internal directory/phone list

☐ Document actions taken
   - Record all steps in ticket
   - Note any issues or exceptions

☐ Close offboarding ticket
```

---

## 📝 Quick Reference Checklist (Printable)

```
EMPLOYEE OFFBOARDING CHECKLIST

Employee: _____________________________
Last Day: _____________________________
Department: ___________________________
Manager: _____________________________
Reason: ☐ Resignation  ☐ Termination  ☐ Retirement

═══════════════════════════════════════
IMMEDIATE ACTIONS (Day of Departure)
═══════════════════════════════════════
☐ Account disabled in Entra ID
☐ Password reset
☐ Sessions revoked
☐ VPN access disabled
☐ Building access card deactivated

═══════════════════════════════════════
WITHIN 24 HOURS
═══════════════════════════════════════
☐ Removed from all groups
☐ Email forwarding configured (if approved)
☐ Out of Office set
☐ Application access revoked
☐ License removed

═══════════════════════════════════════
EQUIPMENT RETURNED
═══════════════════════════════════════
☐ Laptop (Asset: ____________)
☐ Monitor (Asset: ____________)
☐ Phone (Asset: ____________)
☐ Badge/access card
☐ Other: ___________________

═══════════════════════════════════════
DATA HANDLING
═══════════════════════════════════════
☐ Data backed up (if required)
☐ Files transferred to manager
☐ Legal hold applied (if required)

═══════════════════════════════════════
COMPLETION
═══════════════════════════════════════
☐ All actions documented in ticket
☐ Manager notified of completion
☐ Ticket closed

Completed by: _____________ Date: ______
```

---

## 🚨 Special Scenarios

### Involuntary Termination

```
⚠️ HIGH PRIORITY — Act immediately

1. HR calls IT before termination meeting
2. IT disables account DURING the meeting
3. Sessions revoked immediately
4. VPN/remote access killed
5. Building access deactivated
6. Manager collects equipment in meeting

DO NOT tell the employee or anyone else about the termination.
Coordinate only with HR and management.
```

### Employee Keeps Company Phone

```
If employee is allowed to keep company phone:
☐ Remove MDM (Mobile Device Management)
☐ Remove company apps remotely
☐ Remove from company inventory
☐ Document manager's approval
```

### Legal Hold

```
If HR/Legal requests data preservation:
☐ DO NOT delete email or files
☐ Enable litigation hold on mailbox
☐ Preserve OneDrive in place
☐ Document hold request
☐ Check with Legal before any deletion
```

---

## 📊 Offboarding Ticket Template

```
TICKET TYPE: Employee Offboarding

Employee: Sarah Johnson
Email: sarah.johnson@company.com
Department: Sales
Manager: Mike Wilson
Last Day: March 22, 2026
Type: Resignation

ACTIONS COMPLETED:
[x] Account disabled in Entra ID
[x] Password reset
[x] Sessions revoked
[x] Removed from all groups (Sales, All-Staff)
[x] VPN access disabled
[x] Out of Office message set
[x] Email forwarding to manager (30 days)
[x] M365 E3 license removed
[x] Salesforce access revoked

EQUIPMENT RETURNED:
[x] Laptop Dell Latitude (Asset: LAP-2024-0221)
[x] iPhone 14 (Asset: PHN-2024-0098)
[x] Building badge collected by HR

DATA:
[x] OneDrive ownership transferred to Mike Wilson
[x] No legal hold required per HR

NOTES:
Smooth offboarding. No issues.
Completed: 2026-03-22 5:30 PM
```

---

## 🔐 Security Reminders

1. **Speed matters** — Disable access quickly, especially for terminations
2. **Don't announce** — Keep terminations confidential
3. **Verify with HR** — Always confirm offboarding request is legitimate
4. **Document everything** — Audit trail is critical
5. **Check back** — Verify account stays disabled

---

## 📅 Account Retention

| After Departure | What Happens |
|-----------------|--------------|
| Immediately | Account disabled, access blocked |
| 30 days | Email forwarding expires (typical) |
| 30-90 days | Account may be deleted (varies by policy) |
| Per Legal | Account retained if legal hold |

**Check your company policy** for specific retention requirements.

---

*Next: [VPN Troubleshooting](vpn-troubleshooting.md)*
