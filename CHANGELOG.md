# Changelog

All notable changes to BrokenRanks-Manager will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [Unreleased]

### Planned Features
- Multi-language support (English, Polish)
- Web dashboard for license management
- Mobile notifications for bot status
- Cloud statistics sync
- Auto-potion buying from NPC

---

## [1.2.0] - 2025-01-XX

### Added
- **GitHub Releases Integration** - Updates now downloaded from GitHub instead of private server
- **Stable/Beta Channel Selection** - Choose between stable releases or early access beta versions
- **Improved Death Detection** - Added multiple death card templates for better reliability
- **Boss Fight Logic v2** - Enhanced boss strategies for 3 character types:
  - Mosiek/UK (distance debuff optimization)
  - VD/Druid (spell debuff focus)
  - Rycerz/Sheed/Barba (melee debuff tactics)
- **Version Comparison** - Smart semantic versioning with fallback methods
- **Release Metadata** - Shows release date, changelog, and file size in update dialog

### Changed
- **Auto-updater** - Migrated from VPS to GitHub Releases API
- **Screenshot Processing** - Reduced processing time by 40% (grayscale optimization)
- **Memory Management** - Explicit cleanup of PIL images to prevent memory leaks
- **Update Channel** - Users can now choose update frequency (stable/beta)
- **Logging** - Improved debug output for easier troubleshooting

### Fixed
- **Memory Leak** - Fixed screenshot objects not being properly disposed
- **Unicode Encoding** - Resolved garbled Polish characters in console output
- **Potion Detection** - Reduced false positives with higher threshold (0.9)
- **Boss Fight Timing** - Fixed zegar.png timing issues causing missed attacks
- **Rest Strategy** - Corrected "after death" option not triggering properly

### Security
- **Update Verification** - Added download URL validation for GitHub releases
- **Fallback Server** - Maintains backward compatibility with legacy update server
- **Error Handling** - Improved error messages without exposing sensitive data

---

## [1.1.0] - 2024-12-15

### Added
- **Bot Rdzenie Mode** - Full dungeon automation support
- **Configurable Rest Strategies** - 6 different rest options:
  - After every enemy group
  - After every 3 groups
  - Only before boss
  - After each instance
  - Only after death
  - Use potions instead of resting
- **Character Configuration** - Save per-character settings (hotkeys, tactics)
- **Analytics Tracking** - Local and server-side usage statistics
- **Statistics Dashboard** - View runtime, success rate, error counts
- **GUI Improvements** - Modern dark theme with CustomTkinter
- **Session Tracking** - Detailed session history with timestamps

### Changed
- **Image Recognition** - Switched to multi-template matching for better accuracy
- **Combat Logic** - Improved enemy targeting with offset clicks
- **Potion System** - Best-match algorithm for potion selection
- **Error Recovery** - Better handling of unexpected game states

### Fixed
- **Window Resizing** - Fixed game window not resizing correctly on some systems
- **Frozen Builds** - Corrected path handling for Nuitka compiled executables
- **Template Loading** - Fixed "file not found" errors in zdj_2 folder
- **Combat Marker** - Improved `<w>` marker detection accuracy

---

## [1.0.0] - 2024-11-20

### Added
- **Initial Release** 🎉
- **Bot Jaska Mode** - Automated instance farming
- **License System** - HWID-based activation with online validation
- **Stripe Integration** - Secure payment processing
- **Image Recognition** - OpenCV template matching for enemy detection
- **Auto-Rest** - Configurable rest after battles
- **Death Recovery** - Automatic respawn and return to farming
- **Potion Management** - Auto-use HP/Mana/Konda potions
- **GUI Application** - CustomTkinter-based control panel
- **Update System** - Auto-check and install updates from server
- **Email Service** - Automated license key delivery
- **Admin Dashboard** - Web-based license management

### Security
- **HWID Binding** - License locked to hardware ID (5 component hash)
- **Encrypted Storage** - Local license data encrypted with Fernet
- **HTTPS Communication** - All API calls secured with TLS
- **Rate Limiting** - Protection against brute force attacks
- **IP Blacklist** - Automatic blocking after failed attempts

---

## [0.9.0-beta] - 2024-10-30 (Private Beta)

### Added
- **Beta Testing Program** - Limited release to 20 testers
- **Core Bot Logic** - Basic enemy detection and combat
- **Manual Potion System** - Hotkey-based potion usage
- **Basic GUI** - Tkinter interface for configuration

### Known Issues
- Memory leak after 2+ hours
- Unicode encoding problems
- Window resizing unreliable
- No auto-update system

---

## Version History

| Version | Release Date | Major Features |
|---------|--------------|----------------|
| **1.2.0** | 2025-01-XX | GitHub updates, beta channel |
| **1.1.0** | 2024-12-15 | Rdzenie mode, analytics |
| **1.0.0** | 2024-11-20 | Initial public release |
| 0.9.0-beta | 2024-10-30 | Private beta |

---

## Upgrade Guide

### From 1.1.0 to 1.2.0

**New Configuration Required:**
Add to your `.env` file:
```env
GITHUB_REPO=Tomek-prog/BrokenRanks-Manager
UPDATE_CHANNEL=stable
```

**Breaking Changes:**
- None - fully backward compatible

**Recommended Actions:**
1. Update to 1.2.0 via auto-updater
2. Configure your preferred update channel (stable/beta)
3. Restart bot to apply new settings

### From 1.0.0 to 1.1.0

**New Features to Configure:**
- Choose your rest strategy in GUI
- Set up character-specific profiles
- Enable analytics if desired

**No Manual Action Required:**
- Settings migrate automatically

---

## Support

Found a bug? Have a feature request?

- **Discord:** https://discord.gg/bnMWW6km4Z
- **Email:** support@adminjaska.ovh
- **Website:** https://adminjaska.ovh

---

**Note:** Versions prior to 1.0.0 were not publicly released.

