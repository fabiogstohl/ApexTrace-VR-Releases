# Bekannte Probleme

[English version](KNOWN_ISSUES.md)

## Einschraenkungen der oeffentlichen Beta

- Die aktuellen Dateien sind nicht mit Authenticode signiert. Windows SmartScreen kann
  deshalb vor einem unbekannten Herausgeber warnen. Nur von der Releases-Seite dieses
  Repositorys herunterladen und die bereitgestellte SHA-256-Pruefsumme vergleichen.
- Die Akzeptanz durch Online-RaceControl und Easy Anti-Cheat muss fuer jeden ApexTrace-
  und LMU-Build neu geprueft werden. Der aktuelle Build wird nicht als allgemein
  online-sicher beworben.
- In einigen LMU-VR-Menues koennen flackernde Geometrie oder dunkle Wellen am Bildrand
  auftreten. Zuerst **Menueflackern beheben** verwenden. Quest-Link-Nutzer koennen danach
  **Meta ASW deaktivieren** fuer die aktuelle Meta-Sitzung testen und spaeter die
  automatische Einstellung wiederherstellen.
- Ein OpenXR-API-Layer bleibt geladen, bis LMU vollstaendig neu gestartet wurde. LMU vor
  Installation, Update, Aktivierung oder Deaktivierung des Layers schliessen.
- Die Positionstaste am Lenkrad verwendet DirectInput ohne exklusiven Zugriff. Nicht in
  Kompatibilitaetsberichten aufgefuehrte Lenkradmodelle sind noch ungeprueft.
- HUD-Positionen werden fuer die Anwendung gespeichert, noch nicht getrennt nach Fahrzeug
  oder Headset.

## Wiederherstellung

Wenn LMU nach einem Update das Menue nicht mehr erreicht, im Windows-Startmenue
**ApexTrace VR - OpenXR-Layer deaktivieren (Wiederherstellung)** ausfuehren. Dadurch wird
nur der VR-Layer abgeschaltet; Anwendung, Einstellungen und Bestzeiten bleiben erhalten.
LMU danach vollstaendig neu starten.

Vor einem Fehlerbericht [Support](SUPPORT.md) lesen.
