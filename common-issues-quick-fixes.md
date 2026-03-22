# Common Issues & Quick Fixes

The top 10 helpdesk problems and how to solve them fast.

---

## 🔥 The Reality

**80% of tickets are the same 10 problems.** Master these and you'll handle most of your queue.

---

## 1. Password Reset / Account Locked

**Frequency:** 🔥🔥🔥🔥🔥 (Most common)

### Symptoms
- "I forgot my password"
- "It says my account is locked"
- "Password expired"

### Quick Fix

**Step 1:** Verify user identity
- Ask: Employee ID, manager name, or last 4 of phone number
- NEVER reset without verification

**Step 2:** Check account status
```
Entra ID → Users → Search user → Check:
☐ Account enabled?
☐ Sign-in blocked?
☐ Password expired?
```

**Step 3:** Reset password
```
Entra ID → User → Reset Password
☑️ Check "Require password change"
```

**Step 4:** Communicate securely
- Call user with temp password
- NEVER email passwords

### Prevention Tip
Encourage users to set up **Self-Service Password Reset (SSPR)**.

---

## 2. Outlook Not Working

**Frequency:** 🔥🔥🔥🔥

### Symptoms
- "Outlook won't open"
- "Email stuck in Outbox"
- "Can't see new emails"
- "Outlook keeps asking for password"

### Quick Fixes by Symptom

| Symptom | Try This |
|---------|----------|
| Won't open | Start Outlook in Safe Mode: `outlook.exe /safe` |
| Keeps crashing | Repair Office: Control Panel → Programs → Office → Repair |
| Password prompts | Clear credentials: Control Panel → Credential Manager → Remove Office entries |
| Stuck in Outbox | Check file size (under 25MB?), check internet connection |
| No new mail | Press F9 to sync, check Focused Inbox, check Junk folder |

### Nuclear Option
If nothing works:
```
1. Close Outlook
2. Rename profile: %LOCALAPPDATA%\Microsoft\Outlook → Outlook.old
3. Reopen Outlook — it will create new profile
4. Re-add email account
```

---

## 3. VPN Won't Connect

**Frequency:** 🔥🔥🔥🔥

### Symptoms
- "VPN says connection failed"
- "Connected but can't access files"
- "VPN keeps disconnecting"

### Quick Fixes

| Check | Action |
|-------|--------|
| **Internet working?** | Can they browse Google? If no, fix internet first |
| **VPN client updated?** | Ensure latest version installed |
| **Correct server?** | Verify connecting to right VPN endpoint |
| **Credentials correct?** | Password might have changed |
| **MFA required?** | Check if they approved MFA prompt |
| **Firewall blocking?** | Temporarily disable personal firewall to test |

### Common VPN Fixes

```
1. Disconnect VPN
2. Restart VPN client
3. Restart computer (yes, really)
4. Try different VPN server/location
5. If home router: restart router
```

---

## 4. "My Computer is Slow"

**Frequency:** 🔥🔥🔥

### Symptoms
- "Everything takes forever"
- "Computer freezes"
- "Apps not responding"

### Quick Diagnosis

**Check Task Manager (Ctrl + Shift + Esc):**

| If This is High | Try This |
|-----------------|----------|
| **CPU at 100%** | Find process using CPU → End task or restart |
| **Memory at 100%** | Close unnecessary apps, check for memory leaks |
| **Disk at 100%** | Could be Windows update, antivirus scan, or dying disk |

### Quick Fixes

```
1. Restart computer (fixes 50% of issues)
2. Close unnecessary browser tabs (Chrome uses lots of RAM)
3. Check startup programs: Task Manager → Startup → Disable unnecessary
4. Run disk cleanup: cleanmgr
5. Check for Windows updates running in background
6. Check available disk space (need 10%+ free)
```

### If Still Slow
- Might need RAM upgrade
- Might need SSD upgrade
- Might need new computer

---

## 5. Can't Print

**Frequency:** 🔥🔥🔥

### Symptoms
- "Print job stuck"
- "Printer not found"
- "Prints blank pages"

### Quick Fixes

**Step 1:** Basic checks
```
☐ Printer powered on?
☐ Paper loaded?
☐ No paper jam?
☐ Ink/toner not empty?
☐ Printer connected to network?
```

**Step 2:** Clear print queue
```
1. Open: Services (services.msc)
2. Stop: Print Spooler
3. Delete files in: C:\Windows\System32\spool\PRINTERS
4. Start: Print Spooler
5. Try printing again
```

**Step 3:** Reinstall printer
```
1. Settings → Printers & Scanners
2. Remove the printer
3. Add printer again
```

---

## 6. "I Deleted an Important File"

**Frequency:** 🔥🔥🔥

### Symptoms
- "I accidentally deleted..."
- "File was here yesterday, now gone"
- "Saved over the wrong version"

### Quick Recovery Options

| Location | How to Recover |
|----------|----------------|
| **Recycle Bin** | Check Recycle Bin first! |
| **OneDrive** | OneDrive.com → Recycle Bin (keeps 30 days) |
| **SharePoint** | Site → Recycle Bin (keeps 93 days) |
| **Network Drive** | Contact IT — check backup/shadow copies |
| **Local File** | Right-click folder → Previous Versions |

### If Not in Recycle Bin
```
1. Check OneDrive/SharePoint Recycle Bin
2. Check backup system (talk to Tier 2)
3. Check "Previous Versions" (if enabled)
4. File might be gone — set expectations
```

---

## 7. Teams/Zoom Issues

**Frequency:** 🔥🔥🔥

### Symptoms
- "No audio in meeting"
- "Camera not working"
- "Can't share screen"
- "People can't hear me"

### Quick Fixes

| Issue | Fix |
|-------|-----|
| **No audio** | Check mute button, check speaker selection in app |
| **No microphone** | Check mute, check mic selection, test in Settings |
| **Camera not working** | Check privacy settings: Settings → Privacy → Camera → Allow apps |
| **Can't share screen** | Close other screen sharing apps, try sharing specific window |
| **Echo/feedback** | Mute when not talking, use headphones |

### Nuclear Option
```
1. Leave meeting
2. Restart Teams/Zoom
3. Restart computer
4. Rejoin meeting
```

---

## 8. "Can't Connect to Wi-Fi"

**Frequency:** 🔥🔥

### Symptoms
- "Wi-Fi not showing up"
- "Connected but no internet"
- "Keeps disconnecting"

### Quick Fixes

```
1. Toggle Wi-Fi off and on
2. Forget network and reconnect
3. Restart computer
4. Check if others have same issue (might be network problem, not user)
```

### If "Connected, No Internet"
```
1. Open Command Prompt (admin)
2. Run: ipconfig /release
3. Run: ipconfig /renew
4. Run: ipconfig /flushdns
5. Try again
```

---

## 9. Software Installation Request

**Frequency:** 🔥🔥

### Symptoms
- "I need [software] installed"
- "Can you add this app?"

### Process

**Step 1:** Check if approved
```
☐ Is this software on the approved list?
☐ Does user have license?
☐ Manager approval needed?
```

**Step 2:** Install options
```
Option A: Company portal/self-service (if available)
Option B: Remote install via management tool
Option C: Remote into user's computer and install
```

**Step 3:** Document
```
Log software installed, license used, date
```

---

## 10. New Equipment Setup

**Frequency:** 🔥🔥

### Symptoms
- "I got a new laptop"
- "Need to set up new monitor"
- "New employee starting"

### New Laptop Checklist
```
☐ Join to domain / Entra ID
☐ Install required software
☐ Configure email
☐ Set up VPN
☐ Install printers
☐ Transfer data from old device (if applicable)
☐ Enable BitLocker encryption
☐ Configure backup
☐ Enroll in MFA
☐ Test everything with user
```

### New Monitor
```
1. Connect cable (HDMI, DisplayPort, USB-C)
2. Windows key + P → Extend or Duplicate
3. Settings → Display → Arrange monitors
4. Adjust resolution if needed
```

---

## 🎯 Quick Reference Card

| Issue | First Thing to Try |
|-------|-------------------|
| Password | Verify identity → Reset in Entra ID |
| Outlook | Restart Outlook, then try Safe Mode |
| VPN | Restart VPN client, check internet |
| Slow PC | Restart computer, check Task Manager |
| Printer | Clear print queue, restart spooler |
| Deleted file | Check Recycle Bin, then OneDrive Recycle |
| Teams/Zoom audio | Check mute, check device selection |
| Wi-Fi | Toggle off/on, forget and reconnect |
| Software install | Check approved list, get approval |
| New equipment | Follow onboarding checklist |

---

## 💡 Golden Rule

**"Have you tried turning it off and on again?"**

It's a meme, but it genuinely fixes 50% of issues. Restarting clears memory, resets connections, and stops stuck processes.

---

*Next: [Password Reset Procedure](password-reset.md)*
