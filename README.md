# IO Backup

**La evolución natural de Cobian Backup** — copias de seguridad
incrementales estilo *Time Machine* con rastreo de cambios del
filesystem en tiempo real (sin escaneos completos), instantáneas
navegables y control remoto desde el móvil.

🌐 Web oficial: **[www.io-backup.com](https://www.io-backup.com)**

## Descargar

| Plataforma | Instalador |
|---|---|
| macOS 12+ | **[IO-Backup-1.0.0.dmg](https://github.com/mavksoft/io-backup-releases/releases/download/v1.0.0/IO-Backup-1.0.0.dmg)** — arrastra a Aplicaciones; auto-update incluido |

El DMG va firmado con Developer ID y notarizado por Apple. La app se
actualiza sola (comprueba nuevas versiones cada 6 h).

## Qué hace distinto a IO Backup

- **Sin escaneos completos** — un watcher del SO (USN Journal / FSEvents /
  inotify) registra solo lo que cambia; cada pasada toca lo nuevo.
- **Instantáneas navegables** — cada ejecución crea un punto de
  restauración completo; restaura un fichero, una carpeta o todo.
- **Reanudación real** — si se corta la red o cierras el equipo, el
  siguiente run continúa la *misma* instantánea donde se quedó, incluso
  a nivel de fichero (resume por bytes en FTP).
- **Destinos** — disco local, SMB, FTP/FTPS, SFTP; WebDAV, S3,
  Google Drive y OneDrive en desarrollo.
- **Motor Rust + apps Flutter** — daemon nativo para Windows, macOS y
  Linux; clientes de escritorio y móvil (iOS/Android) que controlan tus
  PCs y servidores a distancia.
- **Índice con histórico completo** — cada versión de cada fichero,
  cuándo cambió y desde qué instantánea restaurarla.

## Soporte

- Web y contacto: [www.io-backup.com](https://www.io-backup.com)
- Panel de usuario, licencias y soporte desde el portal.

---
IO Backup · © IT-Systems
