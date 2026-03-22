# Password Reset Procedure

Step-by-step guide for resetting user passwords.

---

## 📋 Overview

Password resets are the **#1 most common helpdesk ticket**. This guide covers both:
- Self-service (for users)
- IT-assisted reset (for helpdesk)

---

## 🔐 Option 1: Self-Service Password Reset (SSPR)

**Best option** — Users can reset their own password 24/7 without calling IT.

### For Users

1. Go to **https://passwordreset.microsoftonline.com**

2. Enter your work email address

3. Complete the CAPTCHA

4. Verify your identity:
   - Text/call to registered phone
   - Email to personal email
   - Answer security questions
   - Authenticator app

5. Create new password:
   - Minimum 12 characters
   - Mix of uppercase, lowercase, numbers, symbols
   - Cannot be a previous password

6. Click **Finish** — you're done!

### SSPR Not Working?

| Error | Meaning |
|-------|---------|
| "SSPR not enabled" | Contact IT — you're not set up for self-service |
| "Verification failed" | Contact IT — your recovery info may be outdated |
| "Account locked" | Wait 30 minutes or contact IT |

---

## 🎫 Option 2: IT-Assisted Reset

When user calls or submits ticket for password reset.

### Step 1: Verify User Identity ⚠️

**CRITICAL: Never reset a password without verification!**

Ask **two** of these questions:

| Verification Question | Why It Works |
|----------------------|--------------|
| Employee ID number | Only HR/user knows this |
| Manager's name | Confirms they know the org |
| Last 4 digits of phone on file | Matches HR records |
| Date of birth | HR record |
| Department and job title | Confirms legitimacy |

**Red Flags — Do NOT reset:**
- Caller can't verify identity
- Request from personal email
- Urgent pressure ("I need it NOW, no time for questions!")
- Third party calling "on behalf of" someone

If suspicious: "I'll need to call you back at your number on file."

---

### Step 2: Check Account Status

**In Microsoft Entra ID:**

1. Go to **entra.microsoft.com**
2. Navigate to **Users** → **All users**
3. Search for the user
4. Check:

| Check | What to Look For |
|-------|------------------|
| **Account enabled** | Should be "Yes" |
| **Sign-in blocked** | Should be "No" |
| **Password status** | Expired? |
| **Risk level** | Any flags? |

---

### Step 3: Reset the Password

**In Entra ID:**

1. Click on the user
2. Click **Reset password**
3. Options:
   - **Auto-generate** (recommended)
   - **Manual password** (if required)
4. ☑️ Check **"Require user to change password at next sign-in"**
5. Click **Reset**
6. Copy the temporary password

---

### Step 4: Communicate Securely

**DO:**
- ✅ Call user at their verified phone number
- ✅ Read password once, have them type it
- ✅ Confirm they logged in successfully

**DON'T:**
- ❌ Email the password
- ❌ Send via Teams/Slack
- ❌ Leave voicemail with password
- ❌ Text the password

**If user is in-person:**
- Write password on paper
- Watch them log in
- Shred the paper immediately

---

### Step 5: Document in Ticket

```
RESOLUTION:
- Verified user identity via employee ID and manager name
- Confirmed account active in Entra ID
- Reset password via Entra admin center
- Called user at verified phone number
- User confirmed successful login
- Instructed user to change password immediately
- Ticket resolved
```

---

## 🔒 Account Lockout

Different from password reset — account is temporarily locked due to too many failed attempts.

### Symptoms
- "Your account has been locked"
- "Too many failed attempts"

### Resolution

**Option A: Wait**
- Account auto-unlocks after 30 minutes (default)

**Option B: IT Unlock**
1. Entra ID → User → Authentication methods
2. Check if MFA device is the issue
3. Unlock if appropriate
4. Investigate why they were locked (potential security issue?)

---

## 📱 MFA Issues During Password Reset

### "I can't get the MFA code"

| Issue | Solution |
|-------|----------|
| Lost phone | Use backup method, or IT resets MFA |
| New phone | Need to re-register MFA |
| Authenticator not working | Remove and re-add account in app |
| Not receiving texts | Try voice call instead |

### To Reset MFA (IT Admin)

1. Entra ID → User
2. **Authentication methods**
3. **Require re-register MFA** or delete existing methods
4. User re-enrolls at next login

---

## 🚨 Escalation Triggers

Escalate to security/Tier 2 if:

| Situation | Action |
|-----------|--------|
| Multiple failed resets same day | Possible attack — escalate |
| User denies making request | Security incident — escalate |
| VIP/executive account | Follow VIP procedure |
| Suspicious caller behavior | Document and escalate |
| Account shows compromise indicators | Security incident — escalate |

---

## 📊 Password Policy (Typical)

| Setting | Requirement |
|---------|-------------|
| Minimum length | 12 characters |
| Complexity | Mix of upper/lower/number/symbol |
| History | Cannot reuse last 10 passwords |
| Expiration | 90 days (or no expiration with MFA) |
| Lockout threshold | 10 failed attempts |
| Lockout duration | 30 minutes |

---

## ✅ Password Reset Checklist

```
☐ Verify user identity (2 questions minimum)
☐ Check account status in Entra ID
☐ Reset password with "force change" enabled
☐ Communicate password via phone call
☐ Confirm user logged in successfully
☐ Document everything in ticket
☐ Close ticket
```

---

## 💡 Tips

1. **Encourage SSPR enrollment** — reduces ticket volume
2. **Never bypass verification** — even for people you "know"
3. **Document everything** — protects you and the company
4. **Watch for patterns** — multiple resets could indicate attack
5. **Be patient** — users are frustrated when locked out

---

*Next: [New Employee IT Setup](new-employee-setup.md)*
