# 🔧 Troubleshooting Guide

Solutions to common problems with BrokenRanks-Manager.

---

## 📋 Quick Navigation

- [Installation Problems](#installation-problems)
- [License & Activation](#license--activation)
- [Bot Performance Issues](#bot-performance-issues)
- [Game Interaction Problems](#game-interaction-problems)
- [Update & Network Issues](#update--network-issues)
- [Advanced Troubleshooting](#advanced-troubleshooting)

---

## 🚨 Installation Problems

### Problem: Bot Won't Start (Nothing Happens)

**Symptoms:**
- Double-click `main.exe` does nothing
- No window appears
- No error message

**Solutions:**

1. **Run as Administrator**
   ```
   Right-click main.exe → Run as administrator → Click "Yes"
   ```

2. **Check Antivirus Quarantine**
   - Open your antivirus (Windows Defender, Avast, etc.)
   - Check quarantine/history
   - If `main.exe` is quarantined, restore it
   - Add folder to exceptions (see [Installation Guide](INSTALLATION.md#antivirus-configuration))

3. **Verify All Files Extracted**
   ```
   Required files:
   ✓ main.exe (50+ MB)
   ✓ python310.dll
   ✓ zdj_2\ folder (46 PNG files)
   ✓ zdj_rdzenie\ folder (25 PNG files)
   ```
   
   **Missing files?** Re-extract the ZIP completely.

4. **Install Visual C++ Redistributable**
   - Download from [Microsoft](https://aka.ms/vs/17/release/vc_redist.x64.exe)
   - Install and restart PC

5. **Check Windows Event Viewer**
   ```
   1. Press Win+R
   2. Type: eventvwr.msc
   3. Go to Windows Logs → Application
   4. Look for errors from "main.exe"
   ```

---

### Problem: "zdj_2 folder not found" Error

**Error Message:**
```
❌ zdj_2 NOT FOUND in any location!
Could not find zdj_2 directory
```

**Cause:** Bot can't locate image template folder.

**Solutions:**

1. **Verify Folder Exists**
   - Open bot installation folder
   - Check `zdj_2\` folder is present
   - Check it contains 46 PNG files

2. **Don't Move main.exe**
   - `main.exe` must stay in same folder as `zdj_2\`
   - Don't create shortcuts to other locations
   - Run from original extracted location

3. **Re-Extract Completely**
   - Delete partial extraction
   - Extract entire ZIP again
   - Don't extract individual files

4. **Check File Permissions**
   ```
   Right-click zdj_2 folder → Properties → Security
   Ensure "Users" have Read & Execute permissions
   ```

---

### Problem: Windows SmartScreen Blocks Bot

**Message:** "Windows protected your PC"

**This is normal** for new/unsigned executables.

**Solution:**
```
1. Click "More info"
2. Click "Run anyway"
```

**Why this happens:**
- Bot is new and not widely recognized yet
- Not signed with expensive code signing certificate ($300+/year)
- **Not a virus** - you can verify on VirusTotal

**Still concerned?**
- Upload `main.exe` to [VirusTotal.com](https://www.virustotal.com)
- Should show 0-2 false positives (maximum)
- 3+ detections = contact support immediately

---

## 🔑 License & Activation

### Problem: "License not found"

**Error:** `404: License not found`

**Causes:**
1. Typo in license key
2. License not yet generated (payment pending)
3. License revoked

**Solutions:**

1. **Double-Check Key Format**
   ```
   Correct:  A1B2-C3D4-E5F6-G7H8
   Wrong:    a1b2c3d4e5f6g7h8 (no dashes)
   Wrong:    A1B2C3D4E5F6G7H8 (no dashes)
   ```

2. **Check Email**
   - Subject: "Your BrokenRanks-Manager License"
   - Wait 5-10 minutes after payment
   - Check spam folder

3. **Verify Payment Completed**
   - Check Stripe receipt
   - Payment status: "Succeeded"
   - If "Pending": wait or contact support

4. **Contact Support**
   - Email: support@adminjaska.ovh
   - Include: Payment receipt, purchase email

---

### Problem: "License already activated on another device"

**Error:** `License already activated on another device`

**Cause:** License is HWID-bound to another PC.

**Solutions:**

1. **First Activation:** You ARE on the correct PC
   - This shouldn't happen
   - Clear local license: Delete `C:\Users\<YourName>\.license\license.json`
   - Try activating again

2. **You Changed Hardware**
   - Major hardware change (motherboard/CPU) = new HWID
   - Use your **1 free HWID reset**
   - Contact support with license key

3. **You Formatted PC**
   - Reinstalling Windows = new HWID
   - Use your **1 free HWID reset**
   - Email: support@adminjaska.ovh

4. **Already Used Free Reset**
   - Additional resets: 50 PLN
   - Or purchase new license

---

### Problem: "Connection timeout - server not responding"

**Error:** `Cannot connect to license server`

**Causes:**
- No internet connection
- Firewall blocking bot
- Server maintenance
- VPN/proxy interference

**Solutions:**

1. **Check Internet**
   ```
   Open browser → Visit https://adminjaska.ovh
   If site loads: Internet OK
   If not: Fix internet connection
   ```

2. **Disable VPN/Proxy**
   - Temporarily disable VPN
   - Disable proxy in Windows settings
   - Try activation again

3. **Check Firewall**
   ```
   Windows Firewall:
   1. Control Panel → Windows Defender Firewall
   2. Allow an app through firewall
   3. Click "Change settings"
   4. Find "main.exe" or click "Allow another app"
   5. Browse to bot folder → Select main.exe
   6. Check "Private" and "Public"
   7. Click "Add" → OK
   ```

4. **Wait and Retry**
   - Server may be restarting (rare)
   - Wait 5-10 minutes
   - Try again

5. **Check Server Status**
   - Discord: [https://discord.gg/bnMWW6km4Z](https://discord.gg/bnMWW6km4Z)
   - #status channel for announcements

---

## 🤖 Bot Performance Issues

### Problem: Bot is Slow / Laggy

**Symptoms:**
- Takes 5+ seconds to detect enemies
- Bot freezes periodically
- High CPU usage (80-100%)

**Solutions:**

1. **Close Other Programs**
   - Close Chrome/Firefox (memory hogs)
   - Close Discord (if not needed)
   - Close other games

2. **Lower Game Graphics**
   ```
   In Broken Ranks settings:
   - Lower texture quality
   - Disable shadows
   - Reduce effects
   - Lock FPS to 30
   ```

3. **Check PC Resources**
   ```
   Press Ctrl+Shift+Esc (Task Manager)
   Performance tab:
   - CPU should be <80%
   - RAM should be <90%
   - Disk should not be 100%
   ```

4. **Update Graphics Drivers**
   - NVIDIA: [GeForce Experience](https://www.nvidia.com/geforce/geforce-experience)
   - AMD: [Radeon Software](https://www.amd.com/en/support)

5. **Reduce Bot Workload**
   - Use "stable" update channel (less aggressive)
   - Increase threshold in config (less sensitive)

---

### Problem: High CPU Usage (70-90%)

**Symptoms:**
- CPU fan loud
- PC gets hot
- Other programs slow

**This is normal** - Image processing is CPU-intensive.

**Why?**
- Screenshots every 50ms (20 FPS)
- Template matching with OpenCV
- Multiple templates per frame
- Running 24/7

**To reduce:**

1. **Accept 50-70% as Normal**
   - Image recognition requires compute power
   - Modern CPUs can handle this safely

2. **Optimize Bot Settings**
   ```python
   # In bot_rdzenie_config.py
   ITERATION_DELAY = 3.0  # Increase from 2.0
   ```

3. **Close Background Programs**
   - Windows Update
   - Antivirus scans
   - Cloud sync (OneDrive, Dropbox)

4. **Better Cooling**
   - Clean PC dust filters
   - Improve airflow
   - Consider better CPU cooler

---

### Problem: Bot Stops After 1-2 Hours

**Symptoms:**
- Bot runs fine initially
- After 1-2 hours, becomes unresponsive
- No error message

**Causes:**
1. Memory leak (fixed in v1.2.0)
2. Game crash/disconnect
3. Power settings suspending PC

**Solutions:**

1. **Update to Latest Version**
   - Memory leak fixed in v1.2.0+
   - Update via auto-updater

2. **Check Game Status**
   - Is game still running?
   - Did you get disconnected?
   - Check for game errors

3. **Disable Sleep Mode**
   ```
   Windows Settings:
   1. System → Power & Sleep
   2. Screen: Never
   3. Sleep: Never (when plugged in)
   4. Additional settings → "Put hard disk to sleep": Never
   ```

4. **Increase Virtual Memory**
   ```
   1. Control Panel → System → Advanced settings
   2. Performance → Settings → Advanced
   3. Virtual memory → Change
   4. Set custom size: 8192-16384 MB
   ```

---

## 🎮 Game Interaction Problems

### Problem: Bot Doesn't Detect Enemies

**Symptoms:**
- Bot runs but doesn't click anything
- Console shows "No enemy found"
- Enemies are visible on screen

**Solutions:**

1. **Verify Game in Windowed Mode**
   ```
   ❌ Fullscreen mode doesn't work
   ✅ Windowed mode required
   
   In Broken Ranks:
   Settings → Graphics → Window Mode: Windowed
   ```

2. **Check Game Resolution**
   ```
   Bot expects: 1300x600
   
   If different:
   - Bot will try to resize automatically
   - If fails, manually resize game window
   ```

3. **Verify Templates Exist**
   ```
   Check zdj_2\ folder contains:
   - przeciwnik_1.png
   - przeciwnik_2.png
   - ... (all enemy templates)
   ```

4. **Test Template Matching**
   ```
   1. Take screenshot of game
   2. Compare with przeciwnik_1.png
   3. Do they look similar?
   4. If not, templates may be outdated
   ```

5. **Lower Threshold**
   ```python
   # In bot_rdzenie_config.py
   ENEMY_THRESHOLD = 0.6  # Lower from 0.75
   ```

6. **Update Templates**
   - Check Discord for updated zdj_2.zip
   - Game graphics may have changed
   - Download new templates

---

### Problem: Bot Clicks Wrong Things

**Symptoms:**
- Clicks players instead of enemies
- Clicks UI elements
- Clicks empty space

**Causes:**
- Templates too generic
- Threshold too low
- UI overlap

**Solutions:**

1. **Increase Threshold**
   ```python
   # In bot_rdzenie_config.py
   ENEMY_THRESHOLD = 0.85  # Increase from 0.75
   ```

2. **Update Templates**
   - Use more specific enemy screenshots
   - Include unique parts (name, level indicator)

3. **Check Click Offset**
   ```python
   # In bot_rdzenie_config.py
   CLICK_OFFSET_Y = 30  # Increase from 20
   # Clicks higher above detected sprite
   ```

4. **Disable Overlays**
   - Turn off game overlays (Discord, MSI Afterburner)
   - Close browser over game area
   - Move chat window away

---

### Problem: Bot Doesn't Use Potions

**Symptoms:**
- Low HP/Mana but bot doesn't click potions
- Bot tries but clicks wrong thing
- "Potion not found" in console

**Solutions:**

1. **Open Potion Panel**
   ```
   Press 'P' in game to open potion panel
   Bot can't detect potions if panel closed
   ```

2. **Check Potion Images**
   ```
   zdj_2\ folder must have:
   - hp200.png, hp500.png, hp1000.png, hp2000.png
   - mana200.png, mana500.png, mana1000.png, mana2000.png
   - konda200.png, etc.
   ```

3. **Ensure Potions Visible**
   - Potion panel must be on screen
   - Not covered by other UI
   - Not minimized

4. **Lower Potion Threshold**
   ```python
   # In code (advanced users only)
   potion_threshold = 0.8  # Lower from 0.9
   ```

5. **Update Potion Templates**
   - Game may have changed potion graphics
   - Download updated zdj_2.zip from Discord

---

### Problem: Bot Dies Repeatedly

**Symptoms:**
- Bot detects death
- Respawns correctly
- But dies again immediately

**Causes:**
- Not healing after respawn
- Running back into dangerous area
- Equipment broke

**Solutions:**

1. **Configure Rest After Death**
   ```
   In GUI:
   Rest Strategy → "After death"
   This heals before continuing
   ```

2. **Check Equipment Durability**
   - Broken equipment = can't fight
   - Repair before starting bot

3. **Verify Rest Hotkey**
   ```
   Game settings:
   Rest = 'R' key
   
   If different, update config
   ```

4. **Lower Instance Difficulty**
   - Bot can't handle very hard content
   - Use appropriate level instances

---

## 🔄 Update & Network Issues

### Problem: "No updates available" but New Version Exists

**Symptoms:**
- New version on GitHub
- Bot says "No updates available"

**Causes:**
- Cached update info
- GitHub API rate limit
- Wrong update channel

**Solutions:**

1. **Check Your Channel**
   ```
   .env file:
   UPDATE_CHANNEL=stable  # or "beta"
   
   GitHub Release marked as "pre-release"? Only beta channel sees it.
   ```

2. **Manual Update**
   - Download latest from GitHub Releases
   - Extract and replace old files
   - Keep `.env` and `version.json`

3. **Clear Update Cache**
   - Close bot
   - Delete `C:\Users\<Name>\.license\update_cache.json` (if exists)
   - Restart bot

4. **Check GitHub Repo Setting**
   ```
   .env file:
   GITHUB_REPO=YOUR_USERNAME/brokenranks-manager
   
   Make sure this matches your actual repo!
   ```

---

### Problem: Update Download Fails

**Error:** `Failed to download update file`

**Solutions:**

1. **Check Internet Speed**
   - Update is 50-80 MB
   - Slow connection may timeout
   - Try again on better connection

2. **Disable VPN**
   - GitHub may block some VPNs
   - Disable temporarily

3. **Check Disk Space**
   - Need 500 MB free
   - Clean temp files if needed

4. **Manual Download**
   - Go to GitHub Releases
   - Download ZIP manually
   - Extract to bot folder

---

## 🔬 Advanced Troubleshooting

### Enable Debug Logging

**To get detailed logs:**

1. Open `client/.env`
2. Add line:
   ```
   LOG_LEVEL=DEBUG
   ```
3. Restart bot
4. Check `license_client.log` for details

### Check License File

**Location:**
```
C:\Users\<YourName>\.license\license.json
```

**File encrypted** - but you can verify it exists.

**If corrupted:**
```
1. Delete license.json
2. Restart bot
3. Re-activate license
```

### Test Image Recognition

**Manually test template matching:**

```python
# Run in Python console
import cv2
import numpy as np

# Load screenshot and template
screenshot = cv2.imread('screenshot.png', cv2.IMREAD_GRAYSCALE)
template = cv2.imread('zdj_2/przeciwnik_1.png', cv2.IMREAD_GRAYSCALE)

# Match
result = cv2.matchTemplate(screenshot, template, cv2.TM_CCOEFF_NORMED)
min_val, max_val, min_loc, max_loc = cv2.minMaxLoc(result)

print(f"Confidence: {max_val}")  # Should be >0.7 for good match
```

### Collect Support Information

**When contacting support, include:**

1. **License Info**
   - Last 4 digits of key (e.g., `****-****-****-G7H8`)
   - License type (Trial/Standard/Premium)

2. **System Info**
   - Windows version: `winver`
   - Bot version: Check `version.json`
   - Antivirus: Name and version

3. **Error Details**
   - Full error message (copy from console)
   - Screenshot of error
   - When it happens (always, sometimes, specific scenario)

4. **Logs**
   - `license_client.log` (last 50 lines)
   - Console output (if visible)

### Factory Reset

**Last resort - clears all settings:**

```
1. Close bot
2. Delete:
   - C:\Users\<Name>\.license\
   - bot_statistics.json
   - Any *.log files
3. Keep:
   - main.exe
   - zdj_2\
   - zdj_rdzenie\
4. Restart bot
5. Re-activate license
```

---

## 📞 Still Stuck?

**We're here to help!**

**Discord (Fastest):**
- [https://discord.gg/bnMWW6km4Z](https://discord.gg/bnMWW6km4Z)
- #support channel
- Live help from community
- Response time: 1-6 hours

**Email Support:**
- support@adminjaska.ovh
- Response time: 24-48 hours
- Include all info from "Collect Support Information"

**Before Contacting:**
1. Read this guide completely
2. Check [FAQ](FAQ.md)
3. Search Discord #support-archive
4. Try basic fixes first

**Emergency (Critical Security Issue):**
- security@adminjaska.ovh
- For exploits, vulnerabilities only

---

**Last Updated:** January 2025  
**Version:** 1.2.0

