# Email & Outlook Troubleshooting

Fix common Outlook and email problems.

---

## 🔥 Most Common Email Issues

| Issue | Frequency |
|-------|-----------|
| "Outlook keeps asking for password" | 🔥🔥🔥🔥🔥 |
| "Can't send/receive email" | 🔥🔥🔥🔥 |
| "Outlook won't open" | 🔥🔥🔥 |
| "Missing emails" | 🔥🔥🔥 |
| "Email stuck in Outbox" | 🔥🔥 |
| "Outlook is slow" | 🔥🔥 |
| "Calendar not syncing" | 🔥🔥 |

---

## 🔧 Outlook Keeps Asking for Password

### Cause
Usually means saved credentials are corrupted or expired.

### Fix 1: Clear Saved Credentials

```
1. Close Outlook completely
2. Open Control Panel
3. Search "Credential Manager"
4. Click "Windows Credentials"
5. Look for entries with "Outlook" or "Microsoft Office"
6. Remove them (click entry → Remove)
7. Reopen Outlook
8. Enter password when prompted
```

### Fix 2: Remove and Re-add Account

```
1. File → Account Settings → Account Settings
2. Select email account
3. Click Remove
4. Click New to add account again
5. Enter email and password
```

### Fix 3: Check Account in Azure/Entra

```
IT Admin check:
☐ Is account enabled?
☐ Is sign-in blocked?
☐ Is MFA working?
☐ Any Conditional Access blocking?
```

---

## 🔧 Can't Send or Receive Email

### Step 1: Check Internet Connection

```
Can you browse websites?
├── NO → Fix internet first
└── YES → Continue
```

### Step 2: Check Send/Receive Status

```
Look at bottom of Outlook window:
• "Connected to Microsoft Exchange" → Good
• "Disconnected" or "Trying to connect" → Problem
```

### Step 3: Try Manual Send/Receive

```
1. Press F9 (or Send/Receive → Send/Receive All)
2. Watch for error messages
3. Note exact error text
```

### Step 4: Check Outbox

```
If emails stuck in Outbox:
☐ Is attachment too large? (limit usually 25MB)
☐ Is recipient address valid?
☐ Try moving email to Drafts, then resend
```

### Step 5: Test Web Access

```
1. Go to https://outlook.office.com
2. Log in with work email
3. Try sending email from web

Works in web but not Outlook → Outlook problem
Doesn't work in web either → Account/server problem
```

---

## 🔧 Outlook Won't Open

### Fix 1: Start in Safe Mode

```
1. Press Windows + R
2. Type: outlook.exe /safe
3. Press Enter
4. If Outlook opens → Add-in problem
```

### Fix 2: Disable Add-ins

```
If Safe Mode works:
1. File → Options → Add-ins
2. Click "Go" next to COM Add-ins
3. Uncheck all add-ins
4. Click OK
5. Restart Outlook normally
6. Re-enable add-ins one by one to find problem
```

### Fix 3: Repair Office

```
1. Control Panel → Programs → Programs and Features
2. Find Microsoft Office
3. Click Change
4. Select "Quick Repair" → Repair
5. If that fails, try "Online Repair"
```

### Fix 4: Create New Outlook Profile

```
1. Close Outlook
2. Control Panel → Mail
3. Click "Show Profiles"
4. Click Add → Name new profile
5. Set up email in new profile
6. Set new profile as default
```

---

## 🔧 Missing Emails

### Check 1: Focused Inbox

```
Outlook splits inbox into "Focused" and "Other"

1. Click "Other" tab
2. Missing emails might be there
3. Right-click email → Move to Focused (to fix future emails)
```

### Check 2: Junk/Spam Folder

```
1. Check Junk Email folder
2. If email is there → Right-click → Not Junk
3. Add sender to Safe Senders list
```

### Check 3: Filters/Rules

```
1. File → Manage Rules & Alerts
2. Check for rules that move/delete emails
3. Disable suspicious rules
```

### Check 4: Search All Folders

```
1. Click in Search box
2. Change scope to "All Mailboxes"
3. Search for sender or subject
```

### Check 5: Deleted Items / Recoverable Items

```
1. Check Deleted Items folder
2. Right-click Deleted Items → "Recover deleted items"
3. Can recover recently deleted emails (up to 30 days)
```

---

## 🔧 Email Stuck in Outbox

### Quick Fix: Move and Resend

```
1. Go to Outbox
2. Open the stuck email
3. Click "Save" (don't send)
4. Move to Drafts folder
5. Open from Drafts and Send again
```

### Check: File Size

```
Attachments too large?
• Most limit: 25MB per email
• Reduce attachment size
• Use SharePoint/OneDrive link instead
```

### Check: Work Offline Mode

```
Look at status bar:
• "Working Offline" → Click "Work Offline" button to toggle off
```

---

## 🔧 Outlook is Slow

### Fix 1: Reduce Mailbox Size

```
1. File → Tools → Mailbox Cleanup
2. View Mailbox Size
3. Empty Deleted Items
4. Archive old emails
```

### Fix 2: Disable Unnecessary Add-ins

```
1. File → Options → Add-ins
2. Disable add-ins you don't use
```

### Fix 3: Compact Outlook Data File

```
1. File → Account Settings → Account Settings
2. Data Files tab
3. Select data file → Settings
4. Click "Compact Now"
```

### Fix 4: Check Hardware

```
Outlook stores data locally. If slow:
☐ SSD drive vs old hard drive?
☐ Enough free disk space (need 10%+ free)?
☐ Enough RAM?
```

---

## 🔧 Calendar Not Syncing

### Fix 1: Check Shared Calendar Permissions

```
If shared calendar not showing updates:
1. Right-click calendar
2. Properties → Permissions
3. Verify permission level
```

### Fix 2: Remove and Re-add Shared Calendar

```
1. Right-click shared calendar
2. Delete Calendar
3. Re-add via File → Open → Other User's Folder
```

### Fix 3: Check Mobile Sync

```
Calendar not syncing to phone:
1. Remove email account from phone
2. Re-add account
3. Ensure Calendar sync is enabled
```

---

## 📱 Mobile Email Issues

### iPhone

```
Can't add work email to iPhone:
1. Settings → Mail → Accounts → Add Account
2. Choose Microsoft 365 / Exchange
3. Enter work email
4. Approve MFA prompt
5. Select what to sync (Mail, Calendar, Contacts)
```

### Android

```
Can't add work email to Android:
1. Open Gmail or Outlook app
2. Add account → Office 365
3. Enter work email and password
4. Approve MFA
5. Allow permissions
```

### "Account Action Required"

```
This usually means:
• MFA needs re-approval
• Password changed
• Account policy update

Fix: Remove account and re-add
```

---

## 📋 Outlook Troubleshooting Checklist

```
OUTLOOK TROUBLESHOOTING

User: _______________________________
Issue: ______________________________

BASIC CHECKS
☐ Internet working?
☐ Web mail working? (outlook.office.com)
☐ Outlook showing "Connected"?

TRIED
☐ Press F9 to sync
☐ Restart Outlook
☐ Clear credentials
☐ Start in Safe Mode
☐ Repair Office
☐ Create new profile

RESULT
☐ Issue resolved
☐ Escalate to Tier 2

Notes: _______________________________
```

---

## 💡 User Tips to Share

1. **Check spam folder first** — Emails often land there
2. **Try web mail** — If Outlook doesn't work, try outlook.office.com
3. **Restart Outlook** — Fixes many sync issues
4. **Archive old mail** — Keeps Outlook fast
5. **Use OneDrive for large files** — Instead of large attachments

---

*Next: [How to Submit an IT Ticket](how-to-submit-ticket.md)*
