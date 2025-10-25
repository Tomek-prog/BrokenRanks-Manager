# ❓ Frequently Asked Questions (FAQ)

Common questions about BrokenRanks-Manager.

---

## 📋 Table of Contents

1. [General Questions](#general-questions)
2. [Licensing & Activation](#licensing--activation)
3. [Technical Questions](#technical-questions)
4. [Bot Functionality](#bot-functionality)
5. [Updates & Support](#updates--support)
6. [Safety & Security](#safety--security)

---

## 🤔 General Questions

### What is BrokenRanks-Manager?

BrokenRanks-Manager is a **desktop automation tool** for the Broken Ranks MMORPG. It uses advanced image recognition (OpenCV) to automatically farm instances and dungeons while you're away from keyboard (AFK).

**Key Features:**
- Auto-detection of enemies using template matching
- Intelligent boss fight strategies
- Automatic potion management
- Death recovery and respawn
- Multi-mode support (instances & dungeons)

### Is this an official tool?

**No.** BrokenRanks-Manager is a **third-party automation tool** and is **not affiliated** with or endorsed by the Broken Ranks development team.

**Use at your own risk.** Account suspension/ban is possible if detected.

### What platforms are supported?

- ✅ **Windows 10** (64-bit)
- ✅ **Windows 11** (64-bit)
- ❌ **macOS** - Not supported
- ❌ **Linux** - Not supported

### How much does it cost?

| Package | Duration | Price |
|---------|----------|-------|
| Trial | 24 hours | 9.99 PLN |
| Standard | 30 days | 49.99 PLN |
| Premium | 90 days | 124.99 PLN |
| Lifetime | Forever | 499.00 PLN |

Purchase at: [https://adminjaska.ovh](https://adminjaska.ovh)

### Do you offer refunds?

**Limited refunds available:**
- **Trial period:** Test before committing (24h for 9.99 PLN)
- **Refund window:** Within 24 hours of purchase
- **Condition:** Bot doesn't work for technical reasons (not user error)

See [Refund Policy](https://adminjaska.ovh/refund.html) for details.

---

## 🔑 Licensing & Activation

### How does licensing work?

Each license is **bound to your hardware** using a Hardware ID (HWID):
- HWID is a hash of: motherboard UUID, CPU ID, MAC address, Windows Product ID
- License can only be used on the PC where it was first activated
- **One license = One PC** (cannot share)

### Can I use my license on multiple PCs?

**No.** Licenses are HWID-bound and cannot be transferred or shared.

If you need multiple PCs:
- Purchase separate licenses
- Or contact support for multi-PC discounts

### What if I format my PC?

**HWID Reset Available:**
- Each license includes **1 free HWID reset**
- Contact support: support@adminjaska.ovh
- Provide your license key and reason
- Reset processed within 24-48 hours

**After the free reset:**
- Additional resets: 50 PLN each
- Or purchase a new license

### What if I upgrade my hardware?

**Minor upgrades** (RAM, GPU, storage):
- HWID remains the same
- License continues working

**Major upgrades** (motherboard, CPU):
- HWID changes
- License stops working
- Use your free HWID reset

### I lost my license key. Can I retrieve it?

**Yes!**
- Check your email (subject: "Your BrokenRanks-Manager License")
- Contact support with your purchase email
- We'll resend your license key

### Can I transfer my license to someone else?

**No.** Licenses are **non-transferable** and **personal**.

Attempting to share or sell your license violates the [LICENSE](../LICENSE) agreement and may result in:
- Immediate license revocation
- No refund
- Potential legal action

---

## 💻 Technical Questions

### What are the system requirements?

**Minimum:**
- Windows 10 (64-bit)
- 4 GB RAM
- 500 MB storage
- Internet connection

**Recommended:**
- Windows 11 (64-bit)
- 8 GB RAM
- 1 GB storage
- Stable internet

### Why does my antivirus block the bot?

This is a **false positive**. The bot uses:
- Screen capture (to read game state)
- Keyboard/mouse simulation (to control the game)
- Process monitoring (to detect game window)

These behaviors can trigger antivirus software.

**Solution:**
Add the bot folder to your antivirus **exclusions/exceptions**.

See [Installation Guide](INSTALLATION.md#antivirus-configuration) for detailed instructions.

### Can I run the bot on a virtual machine (VM)?

**Not recommended.**
- HWID may change on VM reboot
- VM performance degrades image recognition
- Some VM software is detected and blocked

If you must use a VM:
- Ensure stable HWID (fixed MAC, UUID)
- Use powerful host machine
- Test with Trial license first

### Does the bot work with Remote Desktop (RDP)?

**Limited support.**
- RDP may interfere with screen capture
- Input simulation may not work correctly
- Local desktop recommended

### Can I run multiple bot instances?

**No.** One bot instance per license.

Running multiple instances:
- Requires multiple licenses
- Not officially supported (high CPU usage)
- May cause detection issues

---

## 🤖 Bot Functionality

### What game modes does the bot support?

**Bot Jaska Mode:**
- Instance farming (dungeons with boss)
- Automatic enemy detection and targeting
- Boss fight strategies for 3 character types
- Death recovery and respawn

**Bot Rdzenie Mode:**
- Dungeon farming (rdzenie instances)
- Configurable rest strategies
- Custom enemy templates

### How does the bot detect enemies?

**OpenCV Template Matching:**
1. Bot takes screenshot every 50ms
2. Converts to grayscale for faster processing
3. Compares with enemy templates (`zdj_2/*.png`)
4. If match confidence >70%, clicks the enemy
5. Uses attack sequence (1, 2, 1, 2...)

**Accuracy:** ~98% detection rate in optimal conditions

### Does the bot use potions automatically?

**Yes!**
- Detects low HP/Mana/Konda bars
- Finds matching potion in inventory
- Clicks the appropriate potion
- Threshold: 85% confidence (to avoid false clicks)

**Supported potions:**
- HP: 200, 500, 1000, 2000
- Mana: 200, 500, 1000, 2000
- Konda: 200, 500, 1000, 2000

### Can I customize the bot behavior?

**Yes, several options:**
- **Character type:** Mosiek/UK, VD/Druid, Rycerz/Sheed
- **Rest strategy:** 6 different options
- **Attack sequence:** Configurable in `bot_rdzenie_config.py`
- **Thresholds:** Adjust image detection sensitivity

### What happens if I die?

**Auto-recovery:**
1. Bot detects death screen (karta.png)
2. Waits for respawn button
3. Clicks respawn
4. Returns to farming location
5. Resumes botting

### How fast does the bot farm?

**Typical performance:**
- **Instances/hour:** 15-25 (depends on difficulty)
- **Detection speed:** 50-80ms per screenshot
- **Attack speed:** Limited by game mechanics

**Factors affecting speed:**
- Character level and gear
- Instance difficulty
- PC performance
- Rest strategy chosen

---

## 🔄 Updates & Support

### How do I update the bot?

**Automatic updates:**
1. Bot checks GitHub Releases on startup
2. Shows notification if update available
3. Click "Update Now"
4. Download and install automatically
5. Bot restarts with new version

**Manual update:**
1. Download latest release from GitHub
2. Extract and replace old files
3. Keep your `.env` and `version.json`

### What's the difference between Stable and Beta channels?

**Stable Channel** (Recommended):
- Production-ready releases
- Thoroughly tested
- Updates every 2-4 weeks
- Lowest risk of bugs

**Beta Channel** (Early Access):
- New features first
- May have minor bugs
- Updates every few days
- For advanced users

Change channel in `.env`:
```
UPDATE_CHANNEL=stable  # or "beta"
```

### How do I get support?

**Discord (Fastest):**
- [https://discord.gg/bnMWW6km4Z](https://discord.gg/bnMWW6km4Z)
- Live support chat
- Community help
- Average response: 1-6 hours

**Email:**
- support@adminjaska.ovh
- Response time: 24-48 hours
- Include: License key (last 4 digits), error details, screenshots

**Self-Help:**
- [Installation Guide](INSTALLATION.md)
- [Troubleshooting](TROUBLESHOOTING.md)
- GitHub Issues (for bug reports)

### Can I request features?

**Yes!** We welcome feedback.

**How to request:**
1. Join our Discord
2. Go to #feature-requests channel
3. Describe your idea
4. Community votes on features

**Popular requests are prioritized** for future updates.

---

## 🔒 Safety & Security

### Is the bot safe to use?

**Technically safe:**
- ✅ No viruses or malware
- ✅ No keyloggers or spyware
- ✅ Open to VirusTotal scanning
- ✅ Encrypted license storage

**Game terms of service:**
- ⚠️ Automation tools may violate ToS
- ⚠️ Account suspension/ban possible
- ⚠️ Use at your own risk

**Our stance:**
We provide the tool as-is. Users are responsible for compliance with game rules.

### Can I get banned for using this?

**Possible, but unlikely.**

**Risk factors:**
- **Low:** If used moderately (few hours/day)
- **Medium:** If used excessively (24/7)
- **High:** If combined with other cheats/exploits

**Mitigation:**
- Use realistic play patterns
- Take breaks
- Don't brag in game chat
- Use Trial period to test safety

**We are not responsible** for account actions taken by game developers.

### What data does the bot collect?

**Local data:**
- License key (encrypted)
- Hardware ID (hashed)
- Usage statistics (runtime, errors)

**Sent to server:**
- License validation requests (HWID + key)
- Anonymous analytics (runtime, error count)
- No personal data, passwords, or game credentials

See [Privacy Policy](https://adminjaska.ovh/privacy.html) for details.

### Is my payment information secure?

**Yes!**
- Payments processed by **Stripe** (industry standard)
- We never see your credit card details
- PCI-DSS compliant
- End-to-end encryption

### Can you access my game account?

**No.**
- Bot runs locally on your PC
- We cannot access your game account
- We don't store game passwords
- Bot only simulates keyboard/mouse input

---

## 🛠️ Advanced Questions

### Can I modify the bot code?

**No.** This is **proprietary closed-source software.**

Reverse engineering, decompilation, or modification is **strictly prohibited** by the [LICENSE](../LICENSE) agreement and may result in:
- License revocation
- Legal action
- Criminal prosecution

### Can I create my own image templates?

**Yes!**
- Take screenshots in-game
- Crop to the element you want (enemy, button, etc.)
- Save as PNG in `zdj_2/` or `zdj_rdzenie/`
- Name it descriptively (e.g., `my_enemy.png`)
- Add to `bot_rdzenie_config.py`

**Tips:**
- Use grayscale or high contrast
- Avoid UI elements that change
- Test threshold values (0.6-0.9)

### How does HWID work technically?

**HWID Generation:**
```
Components collected:
- Motherboard UUID (via WMIC)
- CPU Processor ID
- MAC Address (first adapter)
- Windows Product ID
- Computer Name

Combined hash:
SHA-256(MB_UUID + CPU_ID + MAC + WIN_ID + NAME)
= 64-character hex string
```

**Why this method:**
- Cannot be easily spoofed
- Survives minor hardware changes
- Changes on major hardware upgrades

### Can I see the bot source code?

**No.** BrokenRanks-Manager is **proprietary software** with **all rights reserved**.

Source code is confidential and not available for viewing, even for educational purposes.

---

## 📞 Still Have Questions?

**We're here to help!**

- **Discord:** [https://discord.gg/bnMWW6km4Z](https://discord.gg/bnMWW6km4Z)
- **Email:** support@adminjaska.ovh
- **Website:** [https://adminjaska.ovh](https://adminjaska.ovh)

---

**Last Updated:** January 2025  
**Version:** 1.2.0

