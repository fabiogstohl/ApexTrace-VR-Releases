# ApexTrace VR

**Telemetry-HUD fuer Le Mans Ultimate**

[English instructions](README.md)

> Oeffentliche Beta-Software. Lies vor Online-Sitzungen die Beta-Einschraenkungen.

## Download

Oeffne auf GitHub den Bereich **Releases** und lade die neueste Datei
`ApexTrace-VR-...-windows-x64.zip` herunter. Verwende nicht die automatisch von GitHub
erzeugten `Source code`-Archive; sie enthalten die Anwendung nicht.

Zu jedem Release gehoert eine `.sha256`-Datei, mit der sich der Download vor dem Start
pruefen laesst.

## Anzeigen

- Brems- und Gasverlauf mit aktuellem Brems-Peak
- Lenkrichtung und aktuelle Geschwindigkeit
- Gang, ABS und Traktionskontrolle
- Progressive Drehzahlleuchten und Schaltblitz
- Delta zur besten Runde mit einstellbarem Bereich
- Englische und deutsche Texte im Einstellfenster

Das HUD funktioniert als Desktop-Overlay und als native OpenXR-Composition-Layer in
VR. Der VR-Modus verwendet die bereits von LMU genutzte OpenXR-Laufzeit und stellt die
System-Laufzeit nicht um.

## Voraussetzungen

- Windows 10 oder Windows 11, 64 Bit
- Le Mans Ultimate mit aktivierten Shared-Memory-Plugins
- Fuer VR: funktionierende 64-Bit-OpenXR-Laufzeit und eine D3D11-VR-Sitzung von LMU

## Installation

1. LMU beenden.
2. Das vollstaendige ZIP in einen dauerhaften Ordner entpacken, zum Beispiel
   `Dokumente\ApexTrace VR`. Die EXE nicht direkt im ZIP starten.
3. `ApexTrace VR.exe` einmal starten. Es sollten keine Administratorrechte verlangt
   werden.
4. In LMU `Settings -> Gameplay -> Enable Plugins` aktivieren.
5. Meta Quest Link, Steam Link oder SteamVR wie gewohnt starten und danach LMU normal
   starten.
6. Ins Auto gehen. ApexTrace VR oeffnet die Einstellungen auf dem Desktop und zeigt
   das HUD im aktiven Ausgabemodus.

Beim ersten Start wird eine OpenXR-API-Layer nur fuer den aktuellen Windows-Benutzer
installiert. Ausserdem kann der normale Benutzer-Autostart aktiviert werden. Solange
dieser aktiv ist, darf der entpackte Programmordner nicht verschoben werden.

## Aktualisierung

LMU und ApexTrace VR schliessen, die entpackten Dateien durch den neuen Release
ersetzen und `ApexTrace VR.exe` einmal starten. Dadurch werden die OpenXR-Dateien
aktualisiert.

## Deinstallation

Unter **Diagnose** die **OpenXR-Layer deinstallieren**, den Windows-Autostart
deaktivieren und ApexTrace VR beenden. Danach kann der Programmordner geloescht werden.

## Beta-Einschraenkungen

- Die aktuelle Beta kann unsigniert sein; Windows SmartScreen kann deshalb warnen.
- Online- und Easy-Anti-Cheat-Kompatibilitaet muss fuer jeden Release erneut geprueft
  werden.
- Nicht in den Testhinweisen genannte Headset-/Runtime-Kombinationen sind ungeprueft.
- Bei Problemen unter **Diagnose** ein Support-Paket erzeugen. Vor dem Teilen pruefen,
  weil Diagnoseinformationen lokale Pfade und Systemdetails enthalten koennen.

## Quellcode

Die Beta-Binaries sind unter der beigefuegten Binary-Lizenz kostenlos nutzbar. Der
Quellcode der Anwendung wird derzeit nicht veroeffentlicht. Drittanbieter-Komponenten
behalten ihre eigenen Lizenzen und Hinweise.

ApexTrace VR ist ein unabhaengiges, inoffizielles Tool und steht in keiner Verbindung
zu Studio 397, Motorsport Games, Le Mans Ultimate, Valve oder Meta.
