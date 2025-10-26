# 🤖 BrokenRanks-Manager - Premium Gaming Automation

**Professional desktop application for Broken Ranks game automation with advanced image recognition and intelligent workflow management.**

[![License](https://img.shields.io/badge/License-Proprietary-red.svg)](LICENSE)
[![Discord](https://img.shields.io/badge/Discord-Join-7289da)](https://discord.gg/bnMWW6km4Z)
[![Website](https://img.shields.io/badge/Website-adminjaska.ovh-blue)](https://adminjaska.ovh)

---

## ✨ Features

### 🎯 Advanced Image Recognition
- **OpenCV-powered template matching** - Accurate enemy and object detection
- **Multi-template support** - Handles different character appearances
- **Smart threshold adjustment** - Adapts to lighting conditions
- **60+ FPS processing** - Real-time screen analysis

### ⚡ Intelligent Bot Logic
- **Automatic enemy detection** - Finds and targets enemies instantly
- **Boss fight strategies** - 3 character-specific strategies (Mosiek/UK, VD/Druid, Rycerz)
- **Death recovery** - Auto-respawn and return to farming
- **Combat markers** - Detects `<w>` in-combat indicators

### 🎮 Multi-Mode Support
- **Bot Jaska Mode** - Instance farming with full automation
- **Bot Rdzenie Mode** - Dungeon automation with configurable strategies
- **Configurable rest options** - 6 different rest strategies
- **Character profiles** - Save settings per character

### 💊 Smart Potion Management
- **Auto HP/Mana/Konda** - Detects low bars and uses appropriate potions
- **Priority system** - Uses the most suitable potion size
- **Confidence-based** - Only uses when confident (85%+ match)

### 🔒 Secure Licensing
- **HWID-based activation** - Bound to your hardware
- **Cloud validation** - Online license verification
- **No key sharing** - One license = one PC
- **Instant activation** - Activate within seconds

### 🔄 Auto-Updates
- **GitHub Releases integration** - Download updates directly from GitHub
- **Stable/Beta channels** - Choose your update frequency
- **One-click updates** - Automatic download and installation
- **Rollback support** - Safe update process

### 📊 Detailed Analytics
- **Runtime tracking** - See total time and daily usage
- **Success metrics** - Track successful runs vs errors
- **Session history** - Review past bot sessions
- **Statistics dashboard** - Visual performance data

---

## 💰 Pricing

| Package | Duration | Price | Best For |
|---------|----------|-------|----------|
| **Trial** | 24 hours | **9.99 PLN** | Testing features |
| **Standard** | 30 days | **49.99 PLN** | Casual users |
| **Premium** | 90 days | **124.99 PLN** | Regular players |
| **Lifetime** | Forever | **499.00 PLN** | Long-term investment |

**💳 Secure payments via Stripe**  
**🔗 Purchase at: [adminjaska.ovh](https://adminjaska.ovh)**

---

## 📥 Installation

### Requirements
- **Windows 10/11** (64-bit)
- **Broken Ranks** game client
- **Active license key** (purchase required)
- **4 GB RAM** minimum
- **Antivirus exception** (see [Troubleshooting](#troubleshooting))

### Quick Start

1. **Download** the latest release:
   - Go to [Releases](https://github.com/Tomek-prog/BrokenRanks-Manager/releases)
   - Download `BrokenRanks-Manager-v1.X.X.zip`

2. **Extract** the ZIP file to any folder (e.g. `C:\BrokenRanks-Manager\`)

3. **Add antivirus exception**:
   - Add the folder to Windows Defender exceptions
   - Required for bot to function properly

4. **Run** `main.exe` as Administrator

5. **Activate** with your license key:
   ```
   Format: XXXX-XXXX-XXXX-XXXX
   Example: A1B2-C3D4-E5F6-G7H8
   ```

6. **Configure** your character and preferences

7. **Start** botting! 🚀

For detailed instructions, see **[docs/INSTALLATION.md](docs/INSTALLATION.md)**

---

## 🚀 Usage

### First Launch

1. Enter your license key when prompted
2. Wait for online validation (2-5 seconds)
3. Main control panel will open

### Bot Configuration

**Character Selection:**
- Mosiek/UK (distance debuff strategy)
- VD/Druid (spell debuff strategy)
- Rycerz/Sheed (melee debuff strategy)

**Rest Strategy:**
- After every enemy group
- After every 3 groups
- Only before boss
- After each instance
- Only after death
- Use potions instead

**Mode Selection:**
- **Bot Jaska** - Instance farming
- **Bot Rdzenie** - Dungeon automation

### In-Game Setup

**Required Hotkeys:**
- `R` - Rest
- `Space` - End timer
- `1,2,3,4` - Attacks
- `Q,W` - Potions (optional)
- `P` - Potion panel

**Game Settings:**
- **Windowed mode** (NOT fullscreen)
- **1300x600 resolution** (bot will auto-resize)
- **Tactic 1** - Default tactic
- **Tactic 2** - Main combat tactic

---

## 🔄 Auto-Updates

The bot checks for updates automatically on startup:

### Update Channels

**Stable** (Recommended)
- Production-ready releases only
- Thoroughly tested
- Update every 2-4 weeks

**Beta** (Early Access)
- New features first
- May have minor bugs
- Update every few days

### How It Works

1. Bot checks GitHub Releases on startup
2. If update available, shows notification
3. Click "Update Now" to download
4. Automatic installation (bot restarts)
5. Done! 🎉

---

## 📚 Documentation

- **[Installation Guide](docs/INSTALLATION.md)** - Detailed setup instructions
- **[FAQ](docs/FAQ.md)** - Frequently asked questions
- **[Troubleshooting](docs/TROUBLESHOOTING.md)** - Common issues and fixes

---

## 💬 Support

Need help? We're here for you!

- **Discord Community:** [https://discord.gg/bnMWW6km4Z](https://discord.gg/bnMWW6km4Z)
  - Live support chat
  - Community tips and tricks
  - Beta testing announcements

- **Email Support:** support@adminjaska.ovh
  - Response time: 24-48 hours
  - Technical assistance
  - License issues

- **Website:** [adminjaska.ovh](https://adminjaska.ovh)
  - Purchase licenses
  - Check server status
  - Latest news

---

## ⚠️ Legal Notice

**This is proprietary commercial software. All rights reserved.**

- ❌ **NOT open source** - Source code is confidential
- ❌ **No reverse engineering** - Strictly prohibited by law
- ❌ **No redistribution** - License is personal and non-transferable
- ✅ **Licensed use only** - Valid license key required

Unauthorized copying, distribution, reverse engineering, or use without a valid license is **strictly prohibited** and may result in:
- Immediate license revocation
- Legal action for damages
- Criminal prosecution

See **[LICENSE](LICENSE)** for full terms.

---

## 🔒 Security & Privacy

We take your security seriously:

- ✅ **Hardware-based licensing** - HWID binding prevents key sharing
- ✅ **Encrypted local storage** - License data encrypted with Fernet (AES-128)
- ✅ **Secure HTTPS communication** - All API calls use TLS 1.3
- ✅ **No password storage** - Only license keys are stored locally
- ✅ **Regular security audits** - Codebase reviewed for vulnerabilities

**Privacy:**
- We collect minimal analytics (runtime, error counts)
- No personal data is transmitted beyond license validation
- HWID is hashed and cannot be reverse-engineered
- See our [Privacy Policy](https://adminjaska.ovh/privacy.html)

**Report Security Issues:**
- Email: security@adminjaska.ovh
- Responsible disclosure appreciated
- Security bounties available for critical findings

---

## 🎮 Game Compatibility

**Supported Game:** Broken Ranks (BrokenRanks.exe)

**Tested Versions:**
- ✅ Current live version (2025)
- ✅ Previous major updates

**Not Officially Endorsed:**
- This is a third-party tool
- Use at your own risk
- We are not affiliated with Broken Ranks developers

---

## 📝 Changelog

### [1.2.0] - 2025-01-XX (Upcoming)
- ✨ GitHub Releases integration for updates
- ✨ Stable/Beta channel selection
- 🐛 Fixed memory leak in image processing
- 🐛 Fixed Unicode encoding in console
- ⚡ 40% faster screenshot processing

### [1.1.0] - 2024-12-XX
- ✨ Bot Rdzenie mode for dungeon automation
- ✨ Configurable rest strategies
- ✨ Analytics tracking
- 🐛 Multiple bug fixes

### [1.0.0] - 2024-11-XX
- 🎉 Initial release
- ✨ Bot Jaska for instance farming
- ✨ License activation system
- ✨ Stripe payment integration

See full **[CHANGELOG.md](CHANGELOG.md)**

---

## 🏆 Why AdminJaska?

### vs Manual Farming
- ⏱️ **24/7 automation** - Farm while you sleep
- 🎯 **Perfect accuracy** - Never misses enemies
- 💊 **Smart potion use** - Never runs out of HP/Mana
- 📊 **Track progress** - See exactly how much you farmed

### vs Other Bots
- 🔒 **Secure licensing** - No license theft
- 🔄 **Auto-updates** - Always latest features
- 💬 **Active support** - Discord community + email
- 🛡️ **Regular updates** - Bug fixes and improvements

---

## ❓ FAQ

**Q: Is this safe to use?**  
A: The bot uses image recognition (screen reading) and simulated inputs. Use at your own discretion.

**Q: Can I use one license on multiple PCs?**  
A: No, licenses are HWID-bound. One license = one PC.

**Q: What if I format my PC?**  
A: Contact support for HWID reset (1 reset per license allowed).

**Q: Do you offer refunds?**  
A: Yes, 24-hour trial allows testing before committing. See [Refund Policy](https://adminjaska.ovh/refund.html).

**Q: How do I update the bot?**  
A: Updates are automatic! Bot checks GitHub on startup and prompts you to update.

**Q: My antivirus blocks the bot!**  
A: This is a false positive. Add the folder to your antivirus exceptions. See [Troubleshooting](docs/TROUBLESHOOTING.md).

More questions? Check **[docs/FAQ.md](docs/FAQ.md)**

---

## 📞 Contact

**General Inquiries:** support@adminjaska.ovh  
**License Issues:** support@adminjaska.ovh  
**Security Reports:** security@adminjaska.ovh  
**Discord:** https://discord.gg/bnMWW6km4Z  
**Website:** https://adminjaska.ovh

---

<div align="center">

**Made with ❤️ by BrokenRanks-Manager Team**

⭐ **Star this repo if you love it!** ⭐

[Buy License](https://adminjaska.ovh) • [Join Discord](https://discord.gg/bnMWW6km4Z) • [Report Bug](https://discord.gg/bnMWW6km4Z)

</div>
