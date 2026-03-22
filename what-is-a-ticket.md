# What is a Helpdesk Ticket?

A guide for IT staff to understand how tickets work, priority levels, and SLAs.

---

## 📋 What is a Ticket?

A **ticket** is a record of a user's IT issue or request. It tracks:
- What the problem is
- Who reported it
- When it was reported
- Current status
- All actions taken
- Resolution details

**Think of it like a medical chart** — it follows the issue from start to finish.

---

## 🔄 Ticket Lifecycle

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│   USER                    HELPDESK                          │
│                                                             │
│   Reports Issue ──────►  Ticket Created                     │
│                              │                              │
│                              ▼                              │
│                         Ticket Assigned                     │
│                              │                              │
│                              ▼                              │
│                    ┌─────────────────┐                      │
│                    │  Can Fix?       │                      │
│                    └────────┬────────┘                      │
│                             │                               │
│              ┌──────────────┴──────────────┐                │
│              │                             │                │
│              ▼                             ▼                │
│         YES: Fix It               NO: Escalate              │
│              │                         to Tier 2            │
│              │                             │                │
│              ▼                             ▼                │
│         Document                    Tier 2 Fixes            │
│         Resolution                       │                  │
│              │                           │                  │
│              └───────────┬───────────────┘                  │
│                          ▼                                  │
│                    Close Ticket                             │
│                          │                                  │
│                          ▼                                  │
│   User Notified ◄────  RESOLVED                             │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 📝 Ticket Statuses

| Status | Meaning |
|--------|---------|
| **New** | Just submitted, not yet looked at |
| **Open / In Progress** | IT is actively working on it |
| **Pending** | Waiting for user response or parts |
| **On Hold** | Paused (waiting for vendor, approval, etc.) |
| **Escalated** | Sent to higher tier for expertise |
| **Resolved** | Fixed, waiting for user confirmation |
| **Closed** | Complete, no further action needed |

---

## 🚨 Priority Levels

| Priority | Response Time | Examples |
|----------|---------------|----------|
| **Critical (P1)** | 15-30 minutes | Server down, security breach, entire team can't work |
| **High (P2)** | 1-2 hours | Single user can't work, executive issue, data loss risk |
| **Medium (P3)** | 4-8 hours | Slow computer, software bug, non-urgent request |
| **Low (P4)** | 1-3 days | Questions, minor issues, "nice to have" requests |

### How to Determine Priority

Ask yourself:
1. **How many people are affected?** (1 user vs entire department)
2. **Can they still work?** (Complete block vs minor inconvenience)
3. **Is there a business deadline?** (Presentation in 1 hour vs general request)
4. **Is there a security risk?** (Data breach vs password reset)

---

## ⏱️ What is an SLA?

**SLA = Service Level Agreement**

It's a promise for how fast IT will:
- **Respond** (first reply to user)
- **Resolve** (fix the issue)

### Example SLA Table

| Priority | First Response | Resolution Target |
|----------|----------------|-------------------|
| Critical | 15 minutes | 2 hours |
| High | 1 hour | 4 hours |
| Medium | 4 hours | 24 hours |
| Low | 8 hours | 72 hours |

**Missing SLAs = unhappy users + unhappy managers.** Track your time!

---

## 🎫 Anatomy of a Good Ticket

### Example Ticket

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
TICKET #: INC0012345
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Submitted:    2026-03-22 10:30 AM
User:         John Smith
Department:   Human Resources
Email:        john.smith@company.com
Phone:        x5678

Priority:     Medium (P3)
Category:     Email / Outlook
Status:       Open

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SUBJECT: Outlook not syncing on mobile phone
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

USER DESCRIPTION:
"I got a new iPhone yesterday and set up my work email. 
It worked at first but now it says 'Cannot connect to server.' 
My laptop email works fine. I've tried restarting the phone."

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
WORK LOG:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[2026-03-22 10:45 AM] - Assigned to: Tech_Amogh
Verified user identity via employee ID.

[2026-03-22 10:50 AM] - Investigation
- Checked account in Entra ID: Active ✓
- Checked MFA status: Enabled ✓
- Checked recent sign-ins: No blocks ✓
- Issue identified: User needs to re-authenticate 
  with MFA on new device.

[2026-03-22 11:00 AM] - Resolution
- Called user at x5678
- Walked through removing and re-adding account
- Had user complete MFA prompt
- Email now syncing successfully
- User confirmed working

[2026-03-22 11:05 AM] - RESOLVED
Root cause: New device required MFA re-enrollment
Resolution: Guided user through mobile Outlook setup with MFA

Time spent: 35 minutes
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## ✅ Ticket Best Practices

### DO:

| Practice | Why |
|----------|-----|
| ✅ Document everything | Future reference, cover yourself |
| ✅ Update ticket in real-time | User can see progress |
| ✅ Set realistic expectations | "I'll update you by 3 PM" |
| ✅ Verify user identity | Security — especially for password resets |
| ✅ Confirm resolution with user | Make sure it's actually fixed |
| ✅ Categorize correctly | Helps with reporting |

### DON'T:

| Practice | Why Not |
|----------|---------|
| ❌ Close without confirming | Issue might not be fixed |
| ❌ Leave tickets "In Progress" forever | SLA violations |
| ❌ Copy/paste lazy notes | "Fixed it" tells nothing |
| ❌ Skip the root cause | Same issue will return |
| ❌ Be rude in notes | Users might see them |

---

## 📊 Ticket Categories

Common categories in most ticketing systems:

| Category | Examples |
|----------|----------|
| **Hardware** | Laptop broken, monitor, keyboard, mouse |
| **Software** | Install request, app not working, crashes |
| **Email** | Outlook, calendar, mobile email |
| **Account/Access** | Password reset, locked out, permissions |
| **Network** | VPN, Wi-Fi, internet, slow connection |
| **Printer** | Can't print, paper jam, setup |
| **Phone/Video** | Teams, Zoom, desk phone |
| **New Hire** | Onboarding setup |
| **Termination** | Offboarding, disable account |
| **Other** | Anything else |

---

## 🛠️ Common Ticketing Systems

| System | Used By |
|--------|---------|
| **ServiceNow** | Large enterprises |
| **Jira Service Management** | Tech companies |
| **Zendesk** | Many mid-size companies |
| **Freshservice** | Growing companies |
| **ConnectWise** | MSPs (Managed Service Providers) |
| **osTicket** | Small businesses (free) |

They all work similarly — learn one, you'll adapt to others quickly.

---

## 💡 Key Takeaways

1. **Every interaction = ticket** — Document everything
2. **Priority matters** — Critical issues first
3. **SLAs are promises** — Track your response times
4. **Good notes save time** — Future you will thank present you
5. **Confirm before closing** — Verify with the user

---

*Next: [Common Issues & Quick Fixes](common-issues-quick-fixes.md)*
