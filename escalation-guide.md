# Escalation Guide

When and how to escalate issues to Tier 2/3 support.

---

## 📋 What is Escalation?

**Escalation** = Passing a ticket to someone with more expertise or access.

Not every issue can be solved at Tier 1. Knowing when to escalate is a **key helpdesk skill**.

---

## 🏢 Support Tiers Explained

| Tier | Who | What They Handle |
|------|-----|------------------|
| **Tier 1** | Helpdesk / IT Support | Password resets, basic troubleshooting, common issues |
| **Tier 2** | System Administrators | Server issues, complex problems, elevated access |
| **Tier 3** | Engineers / Specialists | Network, security, infrastructure, development |
| **External** | Vendors | Microsoft, hardware manufacturers, software vendors |

---

## ⏰ When to Escalate

### Escalate Immediately

| Situation | Escalate To |
|-----------|-------------|
| Security incident (breach, phishing, malware) | Security Team |
| Server/service down affecting multiple users | Tier 2 / Sysadmin |
| Data loss or corruption | Tier 2 / Backup Team |
| Executive/VIP issue you can't solve in 15 min | Tier 2 |
| Network outage | Network Team |

### Escalate After Troubleshooting

| Situation | Escalate To |
|-----------|-------------|
| Tried all Tier 1 steps, still not resolved | Tier 2 |
| Need admin access you don't have | Tier 2 |
| Hardware failure confirmed | Hardware Team |
| Software bug (not user error) | Application Team |
| Vendor issue (Microsoft, etc.) | Vendor Support |

---

## 🚫 When NOT to Escalate

| Situation | What to Do Instead |
|-----------|---------------------|
| Haven't tried basic troubleshooting | Try restart, check KB articles first |
| User just frustrated (issue is simple) | Stay calm, solve it |
| Don't know the answer yet | Research first, ask colleague |
| Want to pass off difficult user | Handle it professionally |

**Golden Rule:** Exhaust your options before escalating.

---

## 📝 How to Escalate Properly

### Step 1: Document Everything First

Before escalating, your ticket should include:

```
☐ Clear problem description
☐ User's contact info
☐ Device/system affected
☐ Error messages (exact text or screenshot)
☐ Steps already taken
☐ Results of each step
☐ Why you're escalating
```

### Step 2: Update Ticket Status

```
Change status to: "Escalated" or "Pending Tier 2"
Assign to: Appropriate team/person
```

### Step 3: Write Escalation Notes

**Good Escalation Note:**

```
ESCALATION TO: Tier 2 - Systems Team

ISSUE SUMMARY:
User cannot access SharePoint site. Getting "Access Denied" error.

TROUBLESHOOTING COMPLETED:
1. Verified user account is active ✓
2. Checked user is in correct security group ✓
3. Cleared browser cache ✓
4. Tested in different browser ✓
5. Tested with my admin account - I can access the site
6. Checked SharePoint admin - user appears to have permissions

REASON FOR ESCALATION:
Permissions appear correct but user still denied. 
May need SharePoint admin to check site-level permissions 
or audit logs.

USER CONTACT:
Jane Smith | jane.smith@company.com | x5678
Available: 9 AM - 5 PM
```

**Bad Escalation Note:**

```
User can't access SharePoint. Please fix.
```

---

## 📞 Escalation Contacts

| Team | Contact | Use For |
|------|---------|---------|
| **Tier 2 - Systems** | sysadmin@company.com | Server, AD, complex issues |
| **Network Team** | network@company.com | Connectivity, VPN infrastructure |
| **Security Team** | security@company.com | Incidents, suspicious activity |
| **Application Team** | apps@company.com | Software bugs, integrations |
| **Hardware Team** | hardware@company.com | Physical equipment failures |

*Update these with your actual team contacts*

---

## 🎯 Escalation by Issue Type

### Account/Access Issues

| Issue | First Try | Escalate To |
|-------|-----------|-------------|
| Password reset | Self-service or Tier 1 reset | Security (if suspicious) |
| Account locked | Wait or Tier 1 unlock | Security (if repeated) |
| Permission denied | Check group membership | Tier 2 / App owner |
| MFA issues | Re-register MFA | Security Team |

### Hardware Issues

| Issue | First Try | Escalate To |
|-------|-----------|-------------|
| Laptop won't boot | Basic troubleshooting | Hardware Team |
| Blue screen | Check event logs | Tier 2 |
| Slow performance | Task Manager, cleanup | Tier 2 (if persistent) |
| Physical damage | Document, collect | Hardware Team |

### Software Issues

| Issue | First Try | Escalate To |
|-------|-----------|-------------|
| App crashes | Restart, repair, reinstall | Application Team |
| Software bug | Verify it's a bug | Application Team / Vendor |
| License issue | Check license pool | Tier 2 / Licensing |
| Installation failed | Clear temp, retry | Tier 2 |

### Network Issues

| Issue | First Try | Escalate To |
|-------|-----------|-------------|
| Can't connect to Wi-Fi | Forget/reconnect, restart | Network Team |
| VPN not working | Basic VPN troubleshooting | Network Team |
| Slow network | Test speed, check local | Network Team (if widespread) |
| Internet outage | Verify scope (one user vs many) | Network Team |

### Email Issues

| Issue | First Try | Escalate To |
|-------|-----------|-------------|
| Can't send/receive | Outlook troubleshooting | Tier 2 / Exchange Admin |
| Mailbox full | Archive, cleanup | User (educate) |
| Missing emails | Check filters, junk | Tier 2 (if not found) |
| Email delivery issues | Check recipient, size | Exchange Admin |

---

## 🔴 Security Escalations

**Always escalate immediately:**

| Incident | Action |
|----------|--------|
| User clicked phishing link | Escalate to Security NOW |
| Ransomware/malware detected | Escalate + Isolate device |
| Suspicious login attempts | Escalate to Security |
| Data breach suspected | Escalate to Security + Management |
| Lost/stolen device | Escalate to Security for remote wipe |

**Security Escalation Template:**

```
🚨 SECURITY INCIDENT 🚨

TYPE: [Phishing / Malware / Unauthorized Access / Data Breach / Other]

REPORTED BY: [User name and contact]
TIME DISCOVERED: [Date and time]
AFFECTED SYSTEMS: [Devices, accounts, data]

INITIAL DETAILS:
[What happened, what was clicked/downloaded, etc.]

IMMEDIATE ACTIONS TAKEN:
☐ Device isolated from network
☐ User password reset
☐ Account disabled (if appropriate)

ESCALATED TO: Security Team
TIME: [Now]
```

---

## ✅ Escalation Checklist

```
BEFORE ESCALATING

☐ Tried all Tier 1 troubleshooting steps
☐ Documented everything in ticket
☐ Captured error messages/screenshots
☐ Identified correct team to escalate to
☐ Wrote clear escalation notes
☐ Included user contact information
☐ Set appropriate priority level

AFTER ESCALATING

☐ Informed user ticket has been escalated
☐ Provided expected response time
☐ Ticket status updated
☐ Assigned to correct team/person
```

---

## 💡 Tips for Good Escalations

1. **Don't apologize for escalating** — It's part of the process
2. **Be thorough** — Missing info = ticket bounced back to you
3. **Stay involved** — Monitor escalated tickets for updates
4. **Learn from escalations** — Ask Tier 2 what the fix was
5. **Build relationships** — Know your Tier 2 team members
6. **Follow up** — Ensure user is updated on progress

---

## 📈 Tracking Your Escalations

Good metrics to watch:

| Metric | Target |
|--------|--------|
| First-call resolution rate | 70-80% |
| Escalation rate | 20-30% |
| Escalations bounced back | < 5% |
| Avg time before escalating | Varies by issue |

If you're escalating > 50% of tickets, you may need more training.
If < 10%, you might be spending too long on complex issues.

---

*Next: [IT Terminology Glossary](it-glossary.md)*
