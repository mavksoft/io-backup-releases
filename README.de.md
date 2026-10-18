<p align="center">
  <img src="https://www.io-backup.com/assets/img/logo.png" alt="IO Backup" width="96">
</p>

<h1 align="center">IO Backup</h1>

<p align="center">Die natürliche Evolution von Cobian Backup.<br>Inkrementelle Backups im Time-Machine-Stil mit Echtzeit-Dateisystem-Tracking — ohne Vollscans.</p>

<p align="center">
  <a href="https://www.io-backup.com"><img src="https://img.shields.io/badge/website-io--backup.com-0A84FF" alt="website"></a>
  <a href="https://github.com/mavksoft/io-backup-releases/releases/latest"><img src="https://img.shields.io/github/v/release/mavksoft/io-backup-releases?label=latest" alt="latest release"></a>
  <img src="https://img.shields.io/badge/platform-macOS%20%C2%B7%20Windows%20%C2%B7%20Linux-black" alt="platforms">
  <img src="https://img.shields.io/badge/license-commercial-orange" alt="commercial license">
</p>

<p align="center"><a href="https://mavksoft.github.io/io-backup-releases/"><img src="https://img.shields.io/badge/docs-mavksoft.github.io%2Fio-backup-releases-blue" alt="docs"></a></p>

<p align="center">🌍 <a href="README.es.md">🇪🇸 Español</a> · <a href="README.md">🇬🇧 English</a> · <strong>🇩🇪 Deutsch</strong> · <a href="README.fr.md">🇫🇷 Français</a> · <a href="README.it.md">🇮🇹 Italiano</a> · <a href="README.pt.md">🇵🇹 Português</a></p>

> **Dieses Repository veröffentlicht ausschließlich offizielle Binär-Releases** — der Quellcode ist privat. Signierte Downloads, Prüfsummen und Auto-Update-Feeds.

## Download

| | |
|---|---|
| <img src='https://raw.githubusercontent.com/mavksoft/io-backup-releases/main/icons/apple.svg' width='15' style='vertical-align:-2px' alt='apple'> **macOS 12+** | [IO-Backup.dmg](https://www.io-backup.com/api/dl.php?p=macos&s=github) — immer die neueste Version; Auto-Update inklusive |
| <img src='https://raw.githubusercontent.com/mavksoft/io-backup-releases/main/icons/windows.svg' width='15' style='vertical-align:-2px' alt='windows'> **Windows** | [IO-Backup-Setup.exe](https://github.com/mavksoft/io-backup-releases/releases/latest) — Installer mit Hintergrunddienst |
| <img src='https://www.io-backup.com/assets/img/logo.png' width='15' style='vertical-align:-2px'> **Website** | [www.io-backup.com](https://www.io-backup.com) — Nutzerportal, Lizenzen und Support |

## Was ist das

IO Backup ist der geistige Nachfolger von Cobian Backup: inkrementelle Backups, die durchsuchbare Snapshots erzeugen — jeder Lauf ist ein vollständiger Wiederherstellungspunkt, aus dem du eine Datei, einen Ordner oder den ganzen Baum zurückholen kannst. Ein Watcher auf Betriebssystemebene protokolliert nur Änderungen, sodass jeder Durchlauf nur das Neue anfasst.

<p align="center"><img src="./screenshots/website.png" width="640" alt="screenshot"></p>

## Funktionen

- **Keine Vollscans** — USN Journal (Windows), FSEvents (macOS) und inotify (Linux) protokollieren nur Änderungen.
- **Durchsuchbare Snapshots** — jeder Lauf erzeugt einen kompletten Wiederherstellungspunkt; stelle eine Datei, einen Ordner oder alles wieder her.
- **Echte Wiederaufnahme** — bei Netzabbruch oder Shutdown setzt der nächste Lauf *denselben* Snapshot fort, sogar mitten in der Datei (Byte-Resume bei FTP).
- **Ziele** — lokale Platte, SMB, FTP/FTPS, SFTP; WebDAV, S3, Google Drive und OneDrive in Entwicklung.
- **Rust-Engine + Flutter-Apps** — nativer Daemon für Windows, macOS und Linux; Desktop- und Mobil-Clients (iOS/Android) steuern PCs und Server aus der Ferne.
- **Index mit Vollhistorie** — jede Version jeder Datei, wann sie sich änderte und welcher Snapshot sie wiederherstellt.
- **Auto-Update** — die App prüft alle 6 h auf neue Versionen und aktualisiert sich selbst.

## So wird es verwendet

1. IO Backup installieren (DMG unter macOS, Setup unter Windows) und ein kostenloses Konto in der App oder auf io-backup.com erstellen.
2. Erste Aufgabe anlegen: Ordner und Ziel wählen (externe Platte, NAS per SMB/FTP, SFTP…).
3. Frequenz und Aufbewahrung festlegen — der Daemon läuft fensterlos im Hintergrund.
4. Mobile App verknüpfen, um Backups zu überwachen und Aufgaben vom iPhone/Android fernzustarten.
5. Wiederherstellen: einen Snapshot öffnen, den Baum wie im Finder durchsuchen und zurückholen, was du brauchst.

## Voraussetzungen

macOS 12+ · Windows 10+ · Linux-Daemon verfügbar · Das DMG ist Developer-ID-signiert und von Apple notarisiert.

## Was dieses Repository enthält

- `IO-Backup-<Version>.dmg` — signiertes + notarisiertes macOS-Installationsprogramm
- `IO-Backup-<Version>.zip` — macOS-Auto-Update-Archiv
- `IO-Backup-Setup-<Version>.exe` / `IO-Backup-Setup.exe` — Windows-Installer (Dienst + App)
- `IO-Backup-<Version>-Windows-Portable.zip` — portabler Windows-Build
- `iobackupd.exe` — headless Windows-Daemon
- `version.json` — Versions-Feed für den Auto-Updater

[Neueste Version](https://github.com/mavksoft/io-backup-releases/releases/latest)

## Häufige Fragen

**Gehen meine Backups in eure Cloud?**  
Nicht standardmäßig — du wählst das Ziel (deine Platte, dein NAS, dein FTP). Deine Backups gehören dir und liegen, wo du es bestimmst.

**Was passiert, wenn ein Backup abbricht?**  
Der nächste Lauf setzt denselben Snapshot exakt an der Stelle fort — sogar mitten in der Datei bei FTP-Zielen.

**Ist es kostenlos?**  
Die Personal-Edition ist kostenlos; Pro- und Cloud+-Pläne schalten erweiterte Funktionen frei — siehe io-backup.com.

## Support

- Website & Kontakt: [www.io-backup.com](https://www.io-backup.com)
- Nutzerportal, Lizenzen und Support über das Portal.

---
<p align="center"><sub>IO Backup · © MavkSoft / IT-Systems</sub></p>
