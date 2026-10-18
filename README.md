<p align="center">
  <img src="https://www.io-backup.com/assets/img/logo.png" alt="IO Backup" width="96">
</p>

<h1 align="center">IO Backup</h1>

<p align="center">The natural evolution of Cobian Backup.<br>Incremental, Time-Machine-style backups with real-time filesystem tracking — no full scans.</p>

<p align="center">
  <a href="https://www.io-backup.com"><img src="https://img.shields.io/badge/website-io--backup.com-0A84FF" alt="website"></a>
  <a href="https://github.com/mavksoft/io-backup-releases/releases/latest"><img src="https://img.shields.io/github/v/release/mavksoft/io-backup-releases?label=latest" alt="latest release"></a>
  <img src="https://img.shields.io/badge/platform-macOS%20%C2%B7%20Windows%20%C2%B7%20Linux-black" alt="platforms">
  <img src="https://img.shields.io/badge/license-commercial-orange" alt="commercial license">
</p>

<p align="center">🌍 <a href="README.es.md">🇪🇸 Español</a> · <strong>🇬🇧 English</strong> · <a href="README.de.md">🇩🇪 Deutsch</a> · <a href="README.fr.md">🇫🇷 Français</a> · <a href="README.it.md">🇮🇹 Italiano</a> · <a href="README.pt.md">🇵🇹 Português</a></p>

> **This repository publishes official binary releases only** — the source code is private. Signed downloads, checksums and auto-update feeds.

## Download

| | |
|---|---|
| 🍎 **macOS 12+** | [IO-Backup.dmg](https://www.io-backup.com/api/dl.php?p=macos&s=github) — always the latest version; auto-update included |
| 🪟 **Windows** | [IO-Backup-Setup.exe](https://github.com/mavksoft/io-backup-releases/releases/latest) — installer with background service |
| 🌍 **Website** | [www.io-backup.com](https://www.io-backup.com) — user portal, licenses and support |

## What it is

IO Backup is the spiritual successor of Cobian Backup: incremental backups that produce browsable snapshots — every run is a complete restore point from which you can recover a file, a folder or the whole tree. An OS-level watcher records only what changes, so each pass touches only what's new.

<p align="center"><img src="./screenshots/website.png" width="640" alt="screenshot"></p>

## Features

- **No full scans** — USN Journal (Windows), FSEvents (macOS) and inotify (Linux) record only what changes; every pass touches just the new data.
- **Browsable snapshots** — every run creates a complete restore point; restore a file, a folder or everything.
- **True resume** — if the network drops or you shut down, the next run continues the *same* snapshot where it left off, even mid-file (byte-level resume on FTP).
- **Destinations** — local disk, SMB, FTP/FTPS, SFTP; WebDAV, S3, Google Drive and OneDrive in development.
- **Rust engine + Flutter apps** — native daemon for Windows, macOS and Linux; desktop and mobile clients (iOS/Android) that control your PCs and servers remotely.
- **Full-history index** — every version of every file, when it changed and which snapshot restores it.
- **Auto-update** — the app checks for new versions every 6 h and updates itself.

## How to use it

1. Install IO Backup (DMG on macOS, Setup on Windows) and create a free account in the app or at io-backup.com.
2. Create your first task: choose which folders to copy and the destination (external drive, NAS over SMB/FTP, SFTP…).
3. Schedule frequency and retention — the daemon runs in the background with no window.
4. Link the mobile app to watch your backups and launch tasks remotely from iPhone/Android.
5. To restore: open any snapshot, browse the tree like a Finder and recover what you need.

## Requirements

macOS 12+ · Windows 10+ · Linux daemon available · The DMG is Developer-ID signed and notarized by Apple.

## What's in this repository

- `IO-Backup-<version>.dmg` — signed + notarized macOS installer
- `IO-Backup-<version>.zip` — macOS auto-update archive
- `IO-Backup-Setup-<version>.exe` / `IO-Backup-Setup.exe` — Windows installer (service + app)
- `IO-Backup-<version>-Windows-Portable.zip` — portable Windows build
- `iobackupd.exe` — headless Windows daemon
- `version.json` — version feed for the auto-updater

[Latest release](https://github.com/mavksoft/io-backup-releases/releases/latest)

## FAQ

**Do my backups go to your cloud?**  
Not by default — you choose the destination (your disk, your NAS, your FTP). Your backups are yours and live where you decide.

**What if a backup is cut short?**  
The next run resumes the same snapshot exactly where it stopped — even mid-file on FTP destinations.

**Is it free?**  
The Personal edition is free; Pro and Cloud+ plans unlock advanced features — see io-backup.com.

## Support

- Website & contact: [www.io-backup.com](https://www.io-backup.com)
- User portal, licenses and support from the portal.

---
<p align="center"><sub>IO Backup · © MavkSoft / IT-Systems</sub></p>
