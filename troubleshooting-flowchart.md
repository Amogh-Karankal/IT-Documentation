# Troubleshooting Flowchart

Visual decision trees for diagnosing common IT issues.

---

## 🔧 General Troubleshooting Approach

```
┌─────────────────────────────────────────────────────────┐
│                    USER REPORTS ISSUE                   │
└─────────────────────────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────┐
│              1. GATHER INFORMATION                      │
│                                                         │
│  • What exactly is the problem?                         │
│  • When did it start?                                   │
│  • What changed recently?                               │
│  • Error message? (exact text)                          │
│  • Can you reproduce it?                                │
└─────────────────────────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────┐
│              2. HAVE THEY RESTARTED?                    │
└─────────────────────────────────────────────────────────┘
                           │
              ┌────────────┴────────────┐
              ▼                         ▼
           [ NO ]                    [ YES ]
              │                         │
              ▼                         ▼
┌─────────────────────────┐  ┌─────────────────────────┐
│  "Try restarting and    │  │  Continue to specific   │
│   let me know if that   │  │  troubleshooting        │
│   fixes it"             │  │                         │
└─────────────────────────┘  └─────────────────────────┘
              │                         │
              ▼                         ▼
       Did restart fix it?     Use category flowcharts
              │                    below ⬇️
       ┌──────┴──────┐
       ▼             ▼
    [ YES ]       [ NO ]
       │             │
       ▼             ▼
   RESOLVED    Continue troubleshooting
```

---

## 🔐 Password / Login Issues

```
┌─────────────────────────────────────────────────────────┐
│                CAN'T LOG IN / PASSWORD ISSUE            │
└─────────────────────────────────────────────────────────┘
                           │
                           ▼
                 Is account locked out?
                           │
              ┌────────────┴────────────┐
              ▼                         ▼
           [ YES ]                    [ NO ]
              │                         │
              ▼                         ▼
    Wait 30 min OR           Does user know password?
    IT unlock in Entra              │
              │               ┌──────┴──────┐
              ▼               ▼             ▼
         Try again         [ NO ]        [ YES ]
                              │             │
                              ▼             ▼
                    SSPR or IT reset    Is MFA working?
                              │             │
                              ▼        ┌────┴────┐
                    Communicate new    ▼         ▼
                    password securely [NO]     [YES]
                                        │         │
                                        ▼         ▼
                               Re-register    Is Caps Lock on?
                               MFA device         │
                                             ┌────┴────┐
                                             ▼         ▼
                                          [ YES ]   [ NO ]
                                             │         │
                                             ▼         ▼
                                         Turn off   Check username
                                         Caps Lock  spelling
                                                       │
                                                       ▼
                                              Still not working?
                                                       │
                                                       ▼
                                              ESCALATE - Check
                                              account status
                                              in Entra ID
```

---

## 💻 Computer Won't Start

```
┌─────────────────────────────────────────────────────────┐
│                 COMPUTER WON'T START                    │
└─────────────────────────────────────────────────────────┘
                           │
                           ▼
             Does anything happen when pressing power?
                           │
              ┌────────────┴────────────┐
              ▼                         ▼
        [ NOTHING ]              [ SOMETHING ]
              │                         │
              ▼                         ▼
     Check power cable          What do you see?
     plugged in?                       │
              │                   ┌────┴────────────┐
         ┌────┴────┐              ▼                 ▼
         ▼         ▼        Lights/fans ON    Blue/Black screen
      [ NO ]    [ YES ]     but no display         │
         │         │              │                │
         ▼         ▼              ▼                ▼
    Plug in    Try different   Check monitor   Blue Screen:
    power      outlet          connection      Note error code
                  │               │            and escalate
                  ▼               ▼                │
             Still nothing?   Monitor on?          ▼
                  │               │           Hardware issue
                  ▼          ┌────┴────┐      or OS corrupt
            Try different    ▼         ▼          │
            power cable   [ NO ]    [ YES ]       ▼
                  │          │         │       ESCALATE
                  ▼          ▼         ▼
             ESCALATE    Turn on    Try external
             Hardware    monitor    monitor
```

---

## 📧 Email Not Working

```
┌─────────────────────────────────────────────────────────┐
│                   EMAIL NOT WORKING                     │
└─────────────────────────────────────────────────────────┘
                           │
                           ▼
              Can they access web mail?
              (outlook.office.com)
                           │
              ┌────────────┴────────────┐
              ▼                         ▼
           [ NO ]                    [ YES ]
              │                         │
              ▼                         ▼
    Account or server issue      Outlook app issue
              │                         │
              ▼                         ▼
    Check account status        Is Outlook showing
    in Entra ID                 "Connected"?
              │                         │
         ┌────┴────┐              ┌────┴────┐
         ▼         ▼              ▼         ▼
    Account OK  Account issue  [ NO ]    [ YES ]
         │           │            │         │
         ▼           ▼            ▼         ▼
    ESCALATE    Fix account   Clear       What's the
    to M365     (enable,      credentials  specific issue?
    admin       reset pwd)    or create        │
                              new profile  ┌───┴───────┐
                                           ▼           ▼
                                     Can't send  Missing emails
                                          │           │
                                          ▼           ▼
                                     Check Outbox  Check Junk
                                     (stuck?)      Check Focused
                                     Check size    Check filters
                                     limits
```

---

## 🌐 Can't Connect to Network / Internet

```
┌─────────────────────────────────────────────────────────┐
│              CAN'T CONNECT TO NETWORK                   │
└─────────────────────────────────────────────────────────┘
                           │
                           ▼
                 Wired or Wireless?
                           │
              ┌────────────┴────────────┐
              ▼                         ▼
         [ WIRED ]                [ WIRELESS ]
              │                         │
              ▼                         ▼
    Is cable plugged in?       Is Wi-Fi turned on?
              │                         │
         ┌────┴────┐              ┌────┴────┐
         ▼         ▼              ▼         ▼
      [ NO ]    [ YES ]        [ NO ]    [ YES ]
         │         │              │         │
         ▼         ▼              ▼         ▼
     Plug in    Try different  Turn on   Can see network?
     cable      port or cable  Wi-Fi          │
                    │                    ┌────┴────┐
                    ▼                    ▼         ▼
               Still no?             [ NO ]    [ YES ]
                    │                   │         │
                    ▼                   ▼         ▼
               Check link          Check Wi-Fi  Enter correct
               lights on NIC       is enabled   password
               and switch          on router        │
                                                   ▼
                                              Connected but
                                              no internet?
                                                   │
                                                   ▼
                                         ┌─────────────────┐
                                         │ ipconfig /release│
                                         │ ipconfig /renew  │
                                         │ ipconfig /flushdns│
                                         └─────────────────┘
                                                   │
                                                   ▼
                                              Still no?
                                                   │
                                                   ▼
                                         Are others affected?
                                                   │
                                              ┌────┴────┐
                                              ▼         ▼
                                           [ YES ]   [ NO ]
                                              │         │
                                              ▼         ▼
                                         Network    User's
                                         outage     device
                                         ESCALATE   issue
```

---

## 🖨️ Can't Print

```
┌─────────────────────────────────────────────────────────┐
│                     CAN'T PRINT                         │
└─────────────────────────────────────────────────────────┘
                           │
                           ▼
                 Is printer powered on?
                           │
              ┌────────────┴────────────┐
              ▼                         ▼
           [ NO ]                    [ YES ]
              │                         │
              ▼                         ▼
        Turn it on              Any error on printer
                                display?
                                       │
                                  ┌────┴────┐
                                  ▼         ▼
                               [ YES ]   [ NO ]
                                  │         │
                                  ▼         ▼
                            Fix error   Is printer showing
                            (paper jam, in Windows?
                            low ink,        │
                            etc.)      ┌────┴────┐
                                       ▼         ▼
                                    [ NO ]    [ YES ]
                                       │         │
                                       ▼         ▼
                                 Add printer  Print queue
                                              stuck?
                                                 │
                                            ┌────┴────┐
                                            ▼         ▼
                                         [ YES ]   [ NO ]
                                            │         │
                                            ▼         ▼
                            ┌────────────────────┐  Try test
                            │ Stop Print Spooler │  print
                            │ Delete PRINTERS    │     │
                            │ folder contents    │     ▼
                            │ Start Print Spooler│  ESCALATE
                            └────────────────────┘
                                       │
                                       ▼
                                  Try again
```

---

## 🐢 Computer is Slow

```
┌─────────────────────────────────────────────────────────┐
│                   COMPUTER IS SLOW                      │
└─────────────────────────────────────────────────────────┘
                           │
                           ▼
                   Have they restarted?
                           │
              ┌────────────┴────────────┐
              ▼                         ▼
           [ NO ]                    [ YES ]
              │                         │
              ▼                         ▼
        Restart and              Open Task Manager
        try again                (Ctrl+Shift+Esc)
                                       │
                                       ▼
                              What's using resources?
                                       │
                    ┌──────────────────┼──────────────────┐
                    ▼                  ▼                  ▼
               CPU 100%           Memory 100%        Disk 100%
                    │                  │                  │
                    ▼                  ▼                  ▼
             Find process        Close unused       Could be:
             using CPU           apps               • Windows Update
             End if safe         Too many           • Antivirus scan
                                 browser tabs?      • Failing HDD
                                                         │
                                                    ┌────┴────┐
                                                    ▼         ▼
                                              Let it    If persistent
                                              complete  ESCALATE
                                              (update/  (may need
                                              scan)     hardware)
                                       
                    If nothing obvious ──────────────────────┐
                                                             ▼
                                              ┌────────────────────┐
                                              │ • Check disk space │
                                              │ • Run Disk Cleanup │
                                              │ • Check startup    │
                                              │   programs         │
                                              │ • Check for malware│
                                              └────────────────────┘
                                                             │
                                                        Still slow?
                                                             │
                                                             ▼
                                               May need hardware
                                               upgrade (SSD/RAM)
                                               ESCALATE
```

---

## 📋 Quick Reference: First Steps

| Issue | First Thing to Try |
|-------|-------------------|
| Any issue | Restart |
| Can't log in | Check Caps Lock, check account status |
| No network | Check cable/Wi-Fi toggle |
| Email issues | Try web mail (outlook.office.com) |
| Slow computer | Check Task Manager |
| Can't print | Check printer is on, clear print queue |
| VPN fails | Check internet first |
| Software crash | Restart app, then restart computer |

---

## 💡 The Universal Fix

```
           ┌─────────────────────────────┐
           │                             │
           │  "Have you tried turning    │
           │   it off and on again?"     │
           │                             │
           └─────────────────────────────┘
                         │
                         ▼
              This fixes ~50% of issues
```

---

*Return to: [Common Issues & Quick Fixes](common-issues-quick-fixes.md)*
