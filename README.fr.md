<p align="center">
  <img src="https://www.io-backup.com/assets/img/logo.png" alt="IO Backup" width="96">
</p>

<h1 align="center">IO Backup</h1>

<p align="center">L'évolution naturelle de Cobian Backup.<br>Sauvegardes incrémentales façon Time Machine avec suivi du système de fichiers en temps réel — sans scans complets.</p>

<p align="center">
  <a href="https://www.io-backup.com"><img src="https://img.shields.io/badge/website-io--backup.com-0A84FF" alt="website"></a>
  <a href="https://github.com/mavksoft/io-backup-releases/releases/latest"><img src="https://img.shields.io/github/v/release/mavksoft/io-backup-releases?label=latest" alt="latest release"></a>
  <img src="https://img.shields.io/badge/platform-macOS%20%C2%B7%20Windows%20%C2%B7%20Linux-black" alt="platforms">
  <img src="https://img.shields.io/badge/license-commercial-orange" alt="commercial license">
</p>

<p align="center"><a href="https://mavksoft.github.io/io-backup-releases/"><img src="https://img.shields.io/badge/docs-mavksoft.github.io%2Fio-backup-releases-blue" alt="docs"></a></p>

<p align="center">🌍 <a href="README.es.md">🇪🇸 Español</a> · <a href="README.md">🇬🇧 English</a> · <a href="README.de.md">🇩🇪 Deutsch</a> · <strong>🇫🇷 Français</strong> · <a href="README.it.md">🇮🇹 Italiano</a> · <a href="README.pt.md">🇵🇹 Português</a></p>

> **Ce dépôt publie uniquement les releases officielles** — le code source est privé. Téléchargements signés, sommes de contrôle et flux de mise à jour automatique.

## Téléchargement

| | |
|---|---|
| 🍎 **macOS 12+** | [IO-Backup.dmg](https://www.io-backup.com/api/dl.php?p=macos&s=github) — toujours la dernière version ; auto-update inclus |
| 🪟 **Windows** | [IO-Backup-Setup.exe](https://github.com/mavksoft/io-backup-releases/releases/latest) — installateur avec service en arrière-plan |
| 🌍 **Site officiel** | [www.io-backup.com](https://www.io-backup.com) — portail utilisateur, licences et assistance |

## Qu'est-ce que c'est

IO Backup est le successeur spirituel de Cobian Backup : des sauvegardes incrémentales qui produisent des snapshots navigables — chaque exécution est un point de restauration complet duquel récupérer un fichier, un dossier ou toute l'arborescence. Un watcher du système d'exploitation n'enregistre que ce qui change, donc chaque passage ne touche que le nouveau.

<p align="center"><img src="./screenshots/website.png" width="640" alt="screenshot"></p>

## Fonctionnalités

- **Pas de scans complets** — USN Journal (Windows), FSEvents (macOS) et inotify (Linux) n'enregistrent que les changements.
- **Snapshots navigables** — chaque exécution crée un point de restauration complet ; restaurez un fichier, un dossier ou tout.
- **Reprise réelle** — si le réseau coupe ou la machine s'éteint, le run suivant continue le *même* snapshot là où il s'était arrêté, même au milieu d'un fichier (reprise par octets en FTP).
- **Destinations** — disque local, SMB, FTP/FTPS, SFTP ; WebDAV, S3, Google Drive et OneDrive en développement.
- **Moteur Rust + apps Flutter** — daemon natif Windows, macOS et Linux ; clients bureau et mobile (iOS/Android) pour piloter vos PC et serveurs à distance.
- **Index à historique complet** — chaque version de chaque fichier, quand il a changé et quel snapshot le restaure.
- **Auto-mise à jour** — l'app vérifie les nouvelles versions toutes les 6 h et se met à jour toute seule.

## Mode d'emploi

1. Installez IO Backup (DMG sous macOS, Setup sous Windows) et créez un compte gratuit dans l'app ou sur io-backup.com.
2. Créez votre première tâche : choisissez les dossiers à copier et la destination (disque externe, NAS via SMB/FTP, SFTP…).
3. Programmez fréquence et rétention — le daemon tourne en arrière-plan sans fenêtre.
4. Liez l'app mobile pour surveiller vos sauvegardes et lancer des tâches à distance depuis iPhone/Android.
5. Pour restaurer : ouvrez un snapshot, parcourez l'arborescence comme un Finder et récupérez ce qu'il vous faut.

## Configuration requise

macOS 12+ · Windows 10+ · daemon Linux disponible · Le DMG est signé Developer ID et notarisé par Apple.

## Contenu de ce dépôt

- `IO-Backup-<version>.dmg` — installateur macOS signé + notarisé
- `IO-Backup-<version>.zip` — archive d'auto-mise à jour macOS
- `IO-Backup-Setup-<version>.exe` / `IO-Backup-Setup.exe` — installateur Windows (service + app)
- `IO-Backup-<version>-Windows-Portable.zip` — build portable Windows
- `iobackupd.exe` — daemon Windows headless
- `version.json` — flux de version pour l'auto-updater

[Dernière version](https://github.com/mavksoft/io-backup-releases/releases/latest)

## Questions fréquentes

**Mes sauvegardes vont-elles dans votre cloud ?**  
Pas par défaut — vous choisissez la destination (votre disque, votre NAS, votre FTP). Vos sauvegardes vous appartiennent et vivent où vous décidez.

**Que se passe-t-il si une sauvegarde est interrompue ?**  
Le run suivant reprend le même snapshot exactement là où il s'était arrêté — même au milieu d'un fichier vers un FTP.

**Est-ce gratuit ?**  
L'édition Personal est gratuite ; les plans Pro et Cloud+ débloquent des fonctions avancées — voir io-backup.com.

## Assistance

- Site et contact : [www.io-backup.com](https://www.io-backup.com)
- Portail utilisateur, licences et assistance depuis le portail.

---
<p align="center"><sub>IO Backup · © MavkSoft / IT-Systems</sub></p>
