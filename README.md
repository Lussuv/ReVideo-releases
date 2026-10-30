# ReVideo

Schlanker Video-Player und Trimmer für Windows und Linux.

- Spielt MP4, MKV, MOV, AVI, WebM und mehr direkt ab, mit Hardware-Dekodierung
- Videos zuschneiden: verlustfrei im Original oder kleiner für Discord (unter 10 MB)
- Einzelbilder als PNG speichern, durch den Ordner blättern, Videos in den Papierkorb legen

## Download

Die aktuelle Version liegt unter [Releases](https://github.com/Lussuv/ReVideo-releases/releases/latest).

**Windows:** `ReVideo-<version>-setup.exe` herunterladen und ausführen. Administratorrechte
sind nicht nötig. Danach steht ReVideo im Startmenü und unter „Öffnen mit“.

**Linux:** `ReVideo-<version>-x86_64.flatpak` herunterladen und installieren. ReVideo
braucht die KDE-Laufzeitumgebung von Flathub; ist Flathub noch nicht eingerichtet, zuerst:

```sh
flatpak remote-add --user --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
```

Dann:

```sh
flatpak install --user ReVideo-*-x86_64.flatpak
```

## Updates

Gibt es eine neue Version, zeigt ReVideo oben rechts einen Update-Knopf. Ein Klick lädt
sie herunter, prüft sie und installiert sie; danach startet ReVideo neu. Das gilt für
Windows und für das Flatpak.

Flatpak bis Version 3.2: Hier öffnet der Knopf nur die Download-Seite. Die neue Datei
einmal wie oben installieren, danach geht es auch dort mit einem Klick.

## Tasten

| Taste | Funktion |
|---|---|
| `Leertaste` | Abspielen / Pause |
| `←` / `→` | 5 Sekunden zurück / vor |
| `,` / `.` | Ein Bild zurück / vor |
| `Entf` | Video löschen (Papierkorb) |
| `F11` | Vollbild |
| `Esc` | Vollbild verlassen |

## Open-Source-Komponenten

ReVideo nutzt freie Software, die unter ihren eigenen Lizenzen steht:

| Komponente | Lizenz | Verwendung |
|---|---|---|
| [Qt](https://www.qt.io) | LGPL-3.0 | Oberfläche |
| [mpv](https://mpv.io) (libmpv) | LGPL-2.1+ | Wiedergabe |
| [FFmpeg](https://ffmpeg.org) | LGPL-2.1+ | Wiedergabe (Bibliotheken) |
| FFmpeg mit [x264](https://www.videolan.org/developers/x264.html) | GPL-2.0+ | Export, Vorschaubilder, Einzelbilder (eigenständiges Programm `ffmpeg`) |
| [Inter](https://rsms.me/inter/), [JetBrains Mono](https://www.jetbrains.com/lp/mono/) | OFL-1.1 | Schriften |

Die Bibliotheken liegen als eigene, austauschbare Dateien bei. Den vollständigen
Quellcode genau der mitgelieferten Versionen enthält jedes Release:
`ReVideo-<version>-windows-sources.tar` und `ReVideo-<version>-linux-sources.tar`.
Unter Windows stehen die Lizenztexte im Installationsordner unter `licenses\`.
