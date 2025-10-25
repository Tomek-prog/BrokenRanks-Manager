# 📥 Installation Guide - BrokenRanks-Manager

Complete step-by-step installation instructions for BrokenRanks-Manager.

---

## 📋 Table of Contents

1. [System Requirements](#system-requirements)
2. [Pre-Installation](#pre-installation)
3. [Download & Extract](#download--extract)
4. [Antivirus Configuration](#antivirus-configuration)
5. [First Launch](#first-launch)
6. [License Activation](#license-activation)
7. [In-Game Setup](#in-game-setup)
8. [Troubleshooting](#troubleshooting)

---

## 💻 System Requirements

### Minimum Requirements
- **OS:** Windows 10 (64-bit) or Windows 11
- **RAM:** 4 GB
- **Storage:** 500 MB free space
- **Game:** Broken Ranks (latest version)
- **Internet:** Required for license validation

### Recommended Requirements
- **OS:** Windows 11 (64-bit)
- **RAM:** 8 GB or more
- **Storage:** 1 GB free space
- **Resolution:** 1920x1080 or higher

### Additional Requirements
- **Administrator Rights:** Required for first installation
- **Antivirus Exception:** Must add bot folder to exceptions
- **.NET Framework:** 4.7.2 or newer (usually pre-installed)
- **Visual C++ Redistributable:** 2015-2022 (usually pre-installed)

---

## 🛠️ Pre-Installation

### Step 1: Purchase a License

1. Visit [https://adminjaska.ovh](https://adminjaska.ovh)
2. Choose your package (Trial/Standard/Premium/Lifetime)
3. Complete payment via Stripe (secure checkout)
4. Check your email for license key

**License Key Format:**
```
XXXX-XXXX-XXXX-XXXX
Example: A1B2-C3D4-E5F6-G7H8
```

### Step 2: Prepare Installation Folder

Choose a location for the bot:
- ✅ **Good:** `C:\BrokenRanks-Manager\`
- ✅ **Good:** `C:\Games\BrokenRanks-Manager\`
- ✅ **Good:** `D:\Bot\BrokenRanks-Manager\`
- ❌ **Bad:** Desktop (clutters desktop)
- ❌ **Bad:** Downloads (may get deleted)
- ❌ **Bad:** Temporary folders (unstable)

### Step 3: Check Game Installation

Ensure Broken Ranks is installed and working:
1. Launch the game normally
2. Log in successfully
3. Note the game window title (e.g., "BrokenRanks")
4. Close the game

---

## 📥 Download & Extract

### Download from GitHub Releases

1. Go to [Releases Page](https://github.com/YOUR_USERNAME/brokenranks-manager/releases)
2. Find the latest release (e.g., `v1.2.0`)
3. Download the ZIP file: `BrokenRanks-Manager-v1.X.X.zip`
4. **File size:** ~50-80 MB

### Extract Files

1. Right-click the downloaded ZIP file
2. Select **"Extract All..."**
3. Choose your installation folder (e.g., `C:\BrokenRanks-Manager\`)
4. Click **"Extract"**

### Verify Extraction

Your folder should contain:
```
C:\BrokenRanks-Manager\
├── main.exe               # Main application (50+ MB)
├── zdj_2\                 # Image templates folder
│   ├── przeciwnik_1.png
│   ├── boss.png
│   ├── hp500.png
│   └── ... (46 files)
├── zdj_rdzenie\           # Dungeon mode templates
│   └── ... (25 files)
├── .env                   # Configuration file
├── version.json           # Version information
└── README.md              # Quick start guide
```

**Missing Files?**
- Re-extract the ZIP completely
- Don't extract partial files
- Check antivirus didn't quarantine files

---

## 🛡️ Antivirus Configuration

**⚠️ CRITICAL STEP - Bot will NOT work without this!**

### Why is This Needed?

The bot uses:
- **Screen capture** - To read game state
- **Keyboard/mouse simulation** - To play the game
- **Process monitoring** - To detect game window

These behaviors can trigger false positives in antivirus software.

### Windows Defender (Windows 10/11)

1. Open **Windows Security**
   - Press `Win + I` → **Update & Security** → **Windows Security**
   - Click **"Virus & threat protection"**

2. Click **"Manage settings"** under Virus & threat protection settings

3. Scroll down to **"Exclusions"**

4. Click **"Add or remove exclusions"**

5. Click **"Add an exclusion"** → **"Folder"**

6. Browse to your bot folder (e.g., `C:\BrokenRanks-Manager\`)

7. Click **"Select Folder"**

8. **Verify:** The folder should now appear in exclusions list

### Other Antivirus Software

#### Avast / AVG

1. Open Avast → **Menu** → **Settings**
2. Go to **General** → **Exceptions**
3. Click **"Add Exception"**
4. Browse to `C:\BrokenRanks-Manager\`
5. Click **"Add Exception"**

#### Kaspersky

1. Open Kaspersky → **Settings** → **Additional** → **Threats and Exclusions**
2. Click **"Manage Exclusions"** → **"Add"**
3. Choose **"Folder"** and browse to bot folder
4. Check **"Do not scan"**
5. Click **"Add"**

#### Norton

1. Open Norton → **Settings** → **Antivirus**
2. Click **"Scans and Risks"** → **"Exclusions/Low Risks"**
3. Click **"Configure"** next to Items to Exclude
4. Click **"Add Folders"**
5. Browse to bot folder and click **"OK"**

#### Bitdefender

1. Open Bitdefender → **Protection** → **Antivirus**
2. Click **"Exclusions"** (or **"Settings"** → **"Exclusions"**)
3. Click **"Add"** → **"Browse"**
4. Select bot folder
5. Click **"Add"**

---

## 🚀 First Launch

### Launch as Administrator

1. Right-click `main.exe`
2. Select **"Run as administrator"**
3. Click **"Yes"** on UAC prompt

### Windows SmartScreen Warning

If you see "Windows protected your PC":
1. Click **"More info"**
2. Click **"Run anyway"**

**Why this happens:**
- New executable not yet widely recognized
- Not a virus - you can verify with VirusTotal if concerned
- Warning will disappear after more people use the bot

### First Run Initialization

The bot will:
1. Initialize folders and check dependencies
2. Look for `zdj_2` and `zdj_rdzenie` folders
3. Create configuration files if missing
4. Check for missing image templates

**Expected console output:**
```
[DEBUG] Running as compiled executable
[DEBUG] Executable directory: C:\BrokenRanks-Manager
[DEBUG] Found zdj_2 at: C:\BrokenRanks-Manager\zdj_2
✅ All required images found
```

### License Activation Window

A GUI window will appear with:
- **License key input field**
- **"Activate License"** button
- **"Buy License"** button (opens website)

---

## 🔑 License Activation

### Enter Your License Key

1. Paste your license key from email:
   ```
   Format: XXXX-XXXX-XXXX-XXXX
   Example: A1B2-C3D4-E5F6-G7H8
   ```

2. Click **"Activate License"**

3. Wait for online validation (2-5 seconds)

### Activation Process

The bot will:
1. Connect to license server (adminjaska.ovh)
2. Verify the license key is valid
3. Generate your Hardware ID (HWID)
4. Bind the license to your PC
5. Save encrypted license locally

**Status Messages:**

✅ **Success:**
```
License activated successfully!
Type: Standard (30 days)
Expires: 2025-02-24
HWID: abc123... (bound to this PC)
```

❌ **Errors:**
```
"License not found" → Invalid key, check for typos
"Already activated on another device" → Contact support for HWID reset
"Server error" → Check internet connection
"Invalid format" → Use format XXXX-XXXX-XXXX-XXXX
```

### Post-Activation

After successful activation:
1. License window closes automatically
2. Main bot control panel opens
3. License status shows in top bar
4. You're ready to configure the bot!

---

## 🎮 In-Game Setup

### Required Hotkeys

Configure these in Broken Ranks settings:

| Action | Hotkey | Required? |
|--------|--------|-----------|
| Rest | `R` | ✅ Required |
| End Timer | `Space` | ✅ Required |
| Attack 1 | `1` | ✅ Required |
| Attack 2 | `2` | ✅ Required |
| Attack 3 | `3` | Optional |
| Attack 4 | `4` | Optional |
| HP Potion | `Q` | Optional |
| Mana Potion | `W` | Optional |
| Potion Panel | `P` | ✅ Required |

### Tactic Setup

1. **Tactic 1:** Default tactic (for when attack zone disabled)
2. **Tactic 2:** Main combat tactic (your primary attack sequence)

### Game Settings

**Window Mode:**
- ✅ **Windowed** mode (NOT fullscreen)
- Resolution: 1300x600 (bot will auto-resize)
- Position: Top-left corner (0, 0)

**Graphics:**
- No specific requirements
- Higher FPS = better bot performance
- Disable screen shake if possible

**Positioning in Game:**
- Stand at instance entrance
- Face the entrance NPC/portal
- Clear your path (no NPCs blocking)
- Ensure you have enough potions

---

## 🔧 Troubleshooting

### Bot Won't Start

**Problem:** Double-clicking `main.exe` does nothing

**Solutions:**
1. Run as administrator
2. Check antivirus didn't quarantine the file
3. Verify all DLL files extracted correctly
4. Install Visual C++ Redistributable 2015-2022

### "zdj_2 folder not found"

**Problem:** Bot can't find image templates

**Solutions:**
1. Ensure `zdj_2\` folder is in same directory as `main.exe`
2. Re-extract the ZIP file completely
3. Don't move `main.exe` outside the extracted folder

### License Activation Fails

**Problem:** "Cannot connect to server"

**Solutions:**
1. Check your internet connection
2. Disable VPN/proxy temporarily
3. Check firewall isn't blocking the bot
4. Try again in a few minutes (server may be restarting)

**Problem:** "License already activated"

**Solutions:**
1. If you formatted your PC, contact support for HWID reset
2. Each license can be reset once
3. Email: support@adminjaska.ovh with your license key

### Bot Doesn't Detect Enemies

**Problem:** Bot runs but doesn't click enemies

**Solutions:**
1. Verify game is in windowed mode (NOT fullscreen)
2. Check game resolution is 1300x600
3. Ensure `zdj_2\` folder has all 46 PNG files
4. Try re-downloading update in case templates changed
5. Check if `przeciwnik_1.png` matches your character level range

### High CPU Usage

**Problem:** Bot uses 50-80% CPU

**This is normal** - image processing is CPU-intensive

**To reduce:**
- Close other programs
- Lower game graphics settings
- Use "stable" FPS limiter in game

### Bot Stops After 1-2 Hours

**Problem:** Bot becomes unresponsive

**Possible causes:**
1. Game window lost focus
2. Memory leak (fixed in v1.2.0)
3. Network disconnect

**Solutions:**
1. Update to latest version
2. Don't minimize game window
3. Disable "Away" status in game

---

## 🆘 Need More Help?

### Support Channels

**Discord (Fastest):**
- [https://discord.gg/bnMWW6km4Z](https://discord.gg/bnMWW6km4Z)
- Live chat support
- Community help
- Beta testing announcements

**Email Support:**
- support@adminjaska.ovh
- Response time: 24-48 hours
- Include: License key (last 4 digits), error message, screenshots

**Documentation:**
- [FAQ](FAQ.md) - Frequently asked questions
- [Troubleshooting](TROUBLESHOOTING.md) - Common problems

---

## ✅ Installation Checklist

Before starting the bot, verify:

- [ ] Windows 10/11 (64-bit)
- [ ] Downloaded latest release from GitHub
- [ ] Extracted all files to permanent folder
- [ ] Added folder to antivirus exceptions
- [ ] Ran `main.exe` as administrator
- [ ] Activated license successfully
- [ ] Game installed and working
- [ ] Configured required hotkeys (`R`, `Space`, `1`, `2`)
- [ ] Set up Tactics 1 and 2
- [ ] Game in windowed mode (not fullscreen)
- [ ] Standing at instance entrance

**All checked?** You're ready to bot! 🎉

---

**Last Updated:** January 2025  
**Version:** 1.2.0

