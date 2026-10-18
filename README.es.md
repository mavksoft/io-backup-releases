<p align="center">
  <img src="https://www.io-backup.com/assets/img/logo.png" alt="IO Backup" width="96">
</p>

<h1 align="center">IO Backup</h1>

<p align="center">La evolución natural de Cobian Backup.<br>Copias incrementales estilo Time Machine con rastreo del filesystem en tiempo real — sin escaneos completos.</p>

<p align="center">
  <a href="https://www.io-backup.com"><img src="https://img.shields.io/badge/website-io--backup.com-0A84FF" alt="website"></a>
  <a href="https://github.com/mavksoft/io-backup-releases/releases/latest"><img src="https://img.shields.io/github/v/release/mavksoft/io-backup-releases?label=latest" alt="latest release"></a>
  <img src="https://img.shields.io/badge/platform-macOS%20%C2%B7%20Windows%20%C2%B7%20Linux-black" alt="platforms">
  <img src="https://img.shields.io/badge/license-commercial-orange" alt="commercial license">
</p>

<p align="center">🌍 <strong>🇪🇸 Español</strong> · <a href="README.md">🇬🇧 English</a> · <a href="README.de.md">🇩🇪 Deutsch</a> · <a href="README.fr.md">🇫🇷 Français</a> · <a href="README.it.md">🇮🇹 Italiano</a> · <a href="README.pt.md">🇵🇹 Português</a></p>

> **Este repositorio publica únicamente releases oficiales** — el código fuente es privado. Descargas firmadas, checksums y feeds de auto-actualización.

## Descarga

| | |
|---|---|
| 🍎 **macOS 12+** | [IO-Backup.dmg](https://www.io-backup.com/api/dl.php?p=macos&s=github) — siempre la última versión; auto-update incluido |
| 🪟 **Windows** | [IO-Backup-Setup.exe](https://github.com/mavksoft/io-backup-releases/releases/latest) — instalador con servicio en segundo plano |
| 🌍 **Web oficial** | [www.io-backup.com](https://www.io-backup.com) — portal de usuario, licencias y soporte |

## Qué es

IO Backup es el sucesor espiritual de Cobian Backup: copias de seguridad incrementales que crean instantáneas navegables — cada ejecución es un punto de restauración completo del que puedes recuperar un fichero, una carpeta o todo el árbol. Un watcher del sistema operativo registra solo lo que cambia, así que cada pasada toca únicamente lo nuevo.

## Funciones

- **Sin escaneos completos** — USN Journal (Windows), FSEvents (macOS) e inotify (Linux) registran solo lo que cambia; cada pasada toca lo nuevo.
- **Instantáneas navegables** — cada ejecución crea un punto de restauración completo; restaura un fichero, una carpeta o todo.
- **Reanudación real** — si se corta la red o cierras el equipo, el siguiente run continúa la *misma* instantánea donde se quedó, incluso a nivel de fichero (resume por bytes en FTP).
- **Destinos** — disco local, SMB, FTP/FTPS, SFTP; WebDAV, S3, Google Drive y OneDrive en desarrollo.
- **Motor Rust + apps Flutter** — daemon nativo para Windows, macOS y Linux; clientes de escritorio y móvil (iOS/Android) que controlan tus PCs y servidores a distancia.
- **Índice con histórico completo** — cada versión de cada fichero, cuándo cambió y desde qué instantánea restaurarla.
- **Auto-actualización** — la app comprueba nuevas versiones cada 6 h y se actualiza sola.

## Cómo se usa

1. Instala IO Backup (DMG en macOS, Setup en Windows) y créate una cuenta gratuita en la app o en io-backup.com.
2. Crea tu primera tarea: elige qué carpetas copiar y el destino (disco externo, NAS por SMB/FTP, SFTP…).
3. Programa la frecuencia y la retención — el daemon corre en segundo plano sin abrir ventana.
4. Vincula la app móvil para vigilar tus copias y lanzar tareas a distancia desde el iPhone/Android.
5. Para restaurar: abre cualquier instantánea, navega el árbol como un Finder y recupera lo que necesites.

## Requisitos

macOS 12+ · Windows 10+ · daemon Linux disponible · El DMG va firmado con Developer ID y notarizado por Apple.

## Qué contiene este repositorio

- `IO-Backup-<versión>.dmg` — instalador macOS firmado + notarizado
- `IO-Backup-<versión>.zip` — archivo de auto-actualización macOS
- `IO-Backup-Setup-<versión>.exe` / `IO-Backup-Setup.exe` — instalador Windows (servicio + app)
- `IO-Backup-<versión>-Windows-Portable.zip` — build portable para Windows
- `iobackupd.exe` — daemon headless de Windows
- `version.json` — feed de versión para el auto-actualizador

[Última release](https://github.com/mavksoft/io-backup-releases/releases/latest)

## Preguntas frecuentes

**¿Mis copias van a vuestra nube?**  
No por defecto — tú eliges el destino (tu disco, tu NAS, tu FTP). Las copias son tuyas y viven donde tú decides.

**¿Qué pasa si se corta una copia a la mitad?**  
El siguiente run reanuda la misma instantánea exactamente donde se quedó — incluso a mitad de fichero en destinos FTP.

**¿Es gratis?**  
La edición Personal es gratuita; existen planes Pro y Cloud+ para funciones avanzadas — consulta io-backup.com.

## Soporte

- Web y contacto: [www.io-backup.com](https://www.io-backup.com)
- Panel de usuario, licencias y soporte desde el portal.

---
<p align="center"><sub>IO Backup · © MavkSoft / IT-Systems</sub></p>
