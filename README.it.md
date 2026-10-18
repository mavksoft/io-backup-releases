<p align="center">
  <img src="https://www.io-backup.com/assets/img/logo.png" alt="IO Backup" width="96">
</p>

<h1 align="center">IO Backup</h1>

<p align="center">L'evoluzione naturale di Cobian Backup.<br>Backup incrementali in stile Time Machine con tracciamento del filesystem in tempo reale — senza scansioni complete.</p>

<p align="center">
  <a href="https://www.io-backup.com"><img src="https://img.shields.io/badge/website-io--backup.com-0A84FF" alt="website"></a>
  <a href="https://github.com/mavksoft/io-backup-releases/releases/latest"><img src="https://img.shields.io/github/v/release/mavksoft/io-backup-releases?label=latest" alt="latest release"></a>
  <img src="https://img.shields.io/badge/platform-macOS%20%C2%B7%20Windows%20%C2%B7%20Linux-black" alt="platforms">
  <img src="https://img.shields.io/badge/license-commercial-orange" alt="commercial license">
</p>

<p align="center"><a href="https://mavksoft.github.io/io-backup-releases/"><img src="https://img.shields.io/badge/docs-mavksoft.github.io%2Fio-backup-releases-blue" alt="docs"></a></p>

<p align="center">🌍 <a href="README.es.md">🇪🇸 Español</a> · <a href="README.md">🇬🇧 English</a> · <a href="README.de.md">🇩🇪 Deutsch</a> · <a href="README.fr.md">🇫🇷 Français</a> · <strong>🇮🇹 Italiano</strong> · <a href="README.pt.md">🇵🇹 Português</a></p>

> **Questo repository pubblica solo release binarie ufficiali** — il codice sorgente è privato. Download firmati, checksum e feed di aggiornamento automatico.

## Download

| | |
|---|---|
| 🍎 **macOS 12+** | [IO-Backup.dmg](https://www.io-backup.com/api/dl.php?p=macos&s=github) — sempre l'ultima versione; auto-update incluso |
| 🪟 **Windows** | [IO-Backup-Setup.exe](https://github.com/mavksoft/io-backup-releases/releases/latest) — installer con servizio in background |
| 🌍 **Sito ufficiale** | [www.io-backup.com](https://www.io-backup.com) — portale utente, licenze e assistenza |

## Che cos'è

IO Backup è il successore spirituale di Cobian Backup: backup incrementali che producono snapshot navigabili — ogni esecuzione è un punto di ripristino completo da cui recuperare un file, una cartella o l'intero albero. Un watcher del sistema operativo registra solo ciò che cambia, quindi ogni passata tocca solo le novità.

<p align="center"><img src="./screenshots/website.png" width="640" alt="screenshot"></p>

## Funzionalità

- **Niente scansioni complete** — USN Journal (Windows), FSEvents (macOS) e inotify (Linux) registrano solo ciò che cambia.
- **Snapshot navigabili** — ogni esecuzione crea un punto di ripristino completo; ripristina un file, una cartella o tutto.
- **Ripresa reale** — se la rete cade o spegni il computer, il run successivo continua lo *stesso* snapshot da dove si era fermato, anche a metà file (resume per byte su FTP).
- **Destinazioni** — disco locale, SMB, FTP/FTPS, SFTP; WebDAV, S3, Google Drive e OneDrive in sviluppo.
- **Motore Rust + app Flutter** — daemon nativo per Windows, macOS e Linux; client desktop e mobile (iOS/Android) per controllare PC e server a distanza.
- **Indice con storico completo** — ogni versione di ogni file, quando è cambiata e da quale snapshot ripristinarla.
- **Auto-aggiornamento** — l'app controlla le nuove versioni ogni 6 h e si aggiorna da sola.

## Come si usa

1. Installa IO Backup (DMG su macOS, Setup su Windows) e crea un account gratuito nell'app o su io-backup.com.
2. Crea il primo task: scegli le cartelle da copiare e la destinazione (disco esterno, NAS via SMB/FTP, SFTP…).
3. Programma frequenza e retention — il daemon gira in background senza finestre.
4. Collega l'app mobile per sorvegliare i backup e lanciare task a distanza da iPhone/Android.
5. Per ripristinare: apri uno snapshot, naviga l'albero come un Finder e recupera ciò che serve.

## Requisiti

macOS 12+ · Windows 10+ · daemon Linux disponibile · Il DMG è firmato Developer ID e notarizzato da Apple.

## Cosa contiene questo repository

- `IO-Backup-<versione>.dmg` — installer macOS firmato + notarizzato
- `IO-Backup-<versione>.zip` — archivio di auto-aggiornamento macOS
- `IO-Backup-Setup-<versione>.exe` / `IO-Backup-Setup.exe` — installer Windows (servizio + app)
- `IO-Backup-<versione>-Windows-Portable.zip` — build portable Windows
- `iobackupd.exe` — daemon Windows headless
- `version.json` — feed di versione per l'auto-updater

[Ultima release](https://github.com/mavksoft/io-backup-releases/releases/latest)

## Domande frequenti

**I miei backup vanno sul vostro cloud?**  
Non di default — scegli tu la destinazione (il tuo disco, il tuo NAS, il tuo FTP). I backup sono tuoi e vivono dove decidi tu.

**Cosa succede se un backup si interrompe?**  
Il run successivo riprende lo stesso snapshot esattamente da dove si era fermato — anche a metà file verso destinazioni FTP.

**È gratis?**  
L'edizione Personal è gratuita; i piani Pro e Cloud+ sbloccano funzioni avanzate — vedi io-backup.com.

## Assistenza

- Sito e contatti: [www.io-backup.com](https://www.io-backup.com)
- Portale utente, licenze e assistenza dal portale.

---
<p align="center"><sub>IO Backup · © MavkSoft / IT-Systems</sub></p>
