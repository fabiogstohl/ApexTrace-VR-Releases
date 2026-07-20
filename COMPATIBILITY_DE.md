# Kompatibilitaet

[English version](COMPATIBILITY.md)

ApexTrace VR ist eine oeffentliche Beta fuer Windows x64. **Geprueft** bedeutet, dass die
aufgefuehrte Kombination den beschriebenen Test abgeschlossen hat. Das ist keine Garantie
fuer andere Treiber, Headsets, OpenXR-Runtimes oder zukuenftige LMU-Versionen.

## Gepruefte Kombinationen

| Ausgabe | Runtime / Verbindung | System | Test | Status |
| --- | --- | --- | --- | --- |
| OpenXR VR | SteamVR OpenXR mit Meta Quest Link | Windows 11, NVIDIA GeForce RTX 5070 | LMU-Menue, HUD im Auto, Pause und Sitzungsende | Geprueft |
| Desktop | Windows-Desktop-Compositor | Windows 11, NVIDIA GeForce RTX 5070 | Demo, LMU-Telemetrie und einzelne HUD-Fenster | Geprueft |
| OpenXR VR | Virtuelles SteamVR-HMD | Windows 11, 72 / 90 / 120 Hz | Automatisierte Compositor- und Wiederherstellungstests | Geprueft (virtuelles HMD) |

Beim echten Meta-Quest-Test war die Umgehung fuer die LMU-Menuehintergrundanimation
notwendig. Bei Quest Link kann ausserdem das Abschalten von Meta ASW fuer die aktuelle
Sitzung schwarze Wellen am Bildrand entfernen. Beide Aktionen befinden sich unter
**Status** und **Diagnose**, muessen bewusst ausgefuehrt werden und sind umkehrbar.

## Noch nicht geprueft

- AMD- und Intel-Grafikkarten
- Direkte Verwendung der Meta-OpenXR-Runtime ohne SteamVR
- Vive, Pimax, Varjo, Windows Mixed Reality, Virtual Desktop und ALVR
- Jedes Meta-Quest-Modell und jede kabelgebundene oder drahtlose Link-Konfiguration
- Online-RaceControl und Easy-Anti-Cheat-Akzeptanz fuer genau diesen Build
- DirectInput-Positionstasten aller Lenkrad- und Button-Box-Hersteller

Nicht geprueft bedeutet nicht automatisch inkompatibel. Es liegt lediglich noch kein
reproduzierbares Testergebnis vor. Mit einem
[Headset-Kompatibilitaetsbericht](https://github.com/fabiogstohl/ApexTrace-VR-Releases/issues/new?template=headset_compatibility.yml)
kann eine getestete Kombination ergaenzt werden.

## Angaben fuer einen Bericht

- ApexTrace-VR- und LMU-Version
- Headset sowie kabelgebundene oder drahtlose Verbindung
- Aktive OpenXR-Runtime
- Grafikkarte, Treiber- und Windows-Version
- Bildrate und ungefaehre Testdauer
- Ergebnis in Menue, Ladebildschirm, Auto, Pause und beim Sitzungsende
- Offline-Sitzung oder RaceControl / Easy Anti-Cheat

Ein Diagnose-Support-Bundle vor dem Teilen kontrollieren, da es lokale Pfade und
Systeminformationen enthalten kann.
