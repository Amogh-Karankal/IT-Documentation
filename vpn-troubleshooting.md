# VPN Troubleshooting Guide

Diagnose and fix common VPN connection issues.

---

## 📋 What is a VPN?

**VPN = Virtual Private Network**

It creates a secure "tunnel" between the user's computer and the company network, allowing remote access to internal resources.

```
[User's Laptop] ----🔒 Encrypted Tunnel 🔒----> [Company Network]
     at Home                                      Servers, Files, Apps
```

---

## 🔥 Most Common VPN Issues

| Issue | Frequency |
|-------|-----------|
| "VPN won't connect" | 🔥🔥🔥🔥🔥 |
| "Connected but can't access anything" | 🔥🔥🔥🔥 |
| "VPN keeps disconnecting" | 🔥🔥🔥 |
| "VPN is slow" | 🔥🔥 |
| "Can't find VPN app" | 🔥 |

---

## 🔧 Troubleshooting: VPN Won't Connect

### Step 1: Check Internet Connection First

```
Can the user access Google.com?
├── NO → Fix internet first (not a VPN issue)
└── YES → Continue troubleshooting
```

### Step 2: Basic Checks

| Check | Action |
|-------|--------|
| VPN client open? | Launch the VPN app |
| Correct server selected? | Verify server/region |
| Username correct? | Should be email or domain\username |
| Password correct? | Recently changed? |
| MFA approved? | Check phone for prompt |

### Step 3: Restart VPN Client

```
1. Disconnect VPN (if stuck "connecting")
2. Close VPN application completely
3. Wait 10 seconds
4. Reopen VPN application
5. Try connecting again
```

### Step 4: Restart Computer

Yes, really. This fixes many VPN issues by:
- Clearing stuck network states
- Resetting network adapters
- Releasing old connections

### Step 5: Check Firewall/Antivirus

```
Personal firewall or antivirus might block VPN.

Test:
1. Temporarily disable firewall/antivirus
2. Try VPN connection
3. If works → Add VPN exception to firewall
4. Re-enable firewall
```

### Step 6: Check for VPN Client Updates

```
Outdated VPN client → Connection failures

Update process (varies by client):
• Check app for "Check for Updates"
• Download latest from company portal
• Reinstall if needed
```

---

## 🔧 Troubleshooting: Connected But Can't Access Resources

VPN shows "Connected" but can't reach internal sites/files.

### Step 1: Verify VPN is Actually Connected

```
Command Prompt:
ipconfig

Look for VPN adapter with internal IP (e.g., 10.x.x.x or 192.168.x.x)
If no VPN adapter → Not actually connected
```

### Step 2: Test Internal Access

```
Command Prompt:
ping internalserver.company.local

If ping works → DNS or application issue
If ping fails → VPN routing issue
```

### Step 3: Check Split Tunnel vs Full Tunnel

| Type | Behavior |
|------|----------|
| **Split tunnel** | Only company traffic goes through VPN |
| **Full tunnel** | ALL traffic goes through VPN |

Some resources require full tunnel. Check with IT admin.

### Step 4: Flush DNS

```
Command Prompt (admin):
ipconfig /flushdns
ipconfig /release
ipconfig /renew
```

### Step 5: Try Different Resources

```
☐ Can access SharePoint?
☐ Can access internal website?
☐ Can access file share?
☐ Can ping internal IP directly?

If some work and some don't → Specific resource issue
If none work → VPN tunnel issue
```

---

## 🔧 Troubleshooting: VPN Keeps Disconnecting

### Common Causes

| Cause | Solution |
|-------|----------|
| **Unstable internet** | Switch to wired connection, move closer to router |
| **ISP blocking VPN** | Try different VPN protocol (if available) |
| **Power settings** | Disable Wi-Fi power saving |
| **Idle timeout** | VPN disconnects after inactivity (normal) |
| **IP conflict** | Change home network IP range |

### Fix: Disable Wi-Fi Power Saving

```
1. Device Manager → Network Adapters
2. Right-click Wi-Fi adapter → Properties
3. Power Management tab
4. Uncheck "Allow computer to turn off this device"
5. OK
```

### Fix: Check Home Router

```
• Restart home router
• Check if router firmware needs update
• Some routers block VPN — may need config change
```

---

## 🔧 Troubleshooting: VPN is Slow

### Step 1: Test Speed Without VPN

```
1. Disconnect VPN
2. Run speed test (speedtest.net)
3. Note download/upload speeds

Slow without VPN → ISP issue, not VPN
```

### Step 2: Test Speed With VPN

```
1. Connect VPN
2. Run speed test again
3. Compare results

Expected: 10-30% slower than without VPN (encryption overhead)
If 50%+ slower → VPN server issue
```

### Solutions

| Issue | Fix |
|-------|-----|
| All VPN users slow | VPN server overloaded, contact IT |
| Only this user slow | Try different VPN server/region |
| Slow at certain times | Peak hours, try off-peak |
| Always slow | Check ISP plan, consider wired connection |

---

## 📱 Mobile VPN Issues

### iOS / iPhone

```
If VPN won't connect on iPhone:
1. Settings → General → VPN & Device Management
2. Tap VPN profile
3. Delete and re-add profile
4. Or: Settings → General → Reset → Reset Network Settings
```

### Android

```
If VPN won't connect on Android:
1. Settings → Network → VPN
2. Delete VPN profile
3. Re-add VPN profile
4. Or: Clear VPN app cache/data
```

---

## 🔐 VPN Authentication Issues

### "Invalid Credentials"

```
☐ Username typed correctly?
☐ Password recently changed?
☐ Caps Lock on?
☐ Domain prefix needed? (domain\username)
☐ Account locked?
☐ Account disabled?
```

### "Certificate Error"

```
☐ System date/time correct?
☐ VPN certificate expired?
☐ Need to reinstall VPN client?
```

### "MFA Failed"

```
☐ Phone has signal/connectivity?
☐ Authenticator app time synced?
☐ Push notification sent but not seen?
☐ Try SMS/call backup method?
```

---

## 📋 VPN Troubleshooting Checklist

```
VPN TROUBLESHOOTING

User: _______________________________
Issue: ______________________________

BASIC CHECKS
☐ Internet working? (Can access Google)
☐ VPN client installed and updated?
☐ Correct server selected?
☐ Credentials correct?
☐ MFA approved?

TRIED
☐ Restart VPN client
☐ Restart computer
☐ Disable firewall temporarily
☐ Flush DNS
☐ Try different VPN server

RESULTS
☐ VPN connects now
☐ Need escalation to network team

Notes: _______________________________
____________________________________
```

---

## 🚨 When to Escalate

Escalate to Tier 2 / Network team if:

| Situation | Action |
|-----------|--------|
| Multiple users affected | Possible VPN server issue |
| User tried everything | Infrastructure problem |
| Certificate issues | Network admin needed |
| New VPN setup required | Needs admin access |
| Consistent disconnects | May need packet analysis |

---

## 💡 User Tips to Share

1. **Use wired connection when possible** — More stable than Wi-Fi
2. **Restart before calling IT** — Fixes most issues
3. **Keep VPN client updated** — Prevents compatibility issues
4. **Don't connect to public Wi-Fi without VPN** — Security risk
5. **Disconnect VPN when not needed** — Saves bandwidth

---

*Next: [Email & Outlook Troubleshooting](outlook-troubleshooting.md)*
