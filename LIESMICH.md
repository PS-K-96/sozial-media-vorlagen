# sozial-media-vorlagen

Ablage für **Blender-Vorschauen**, die ElevenLabs als Referenzvideo abholt.
Projekt „Sozial-Media“ (claude.ai), Auto- und Natur-Account. Gepflegt von Claude.

## Wozu
ElevenLabs kann Dateien nur über eine direkte https-Adresse übernehmen.
Claude rendert die Vorschau, legt sie hier ab und hängt den Rohlink
(`raw.githubusercontent.com/...`) in den Upload-Knoten des Flows.

## Aufbau
- `main`: nur Regeln (diese Datei) und `knoten.md` (welche Datei in welchem Flow-Knoten steckt).
- `medien`: nur Vorschauen. Pfad `<reihe>/<video-id>/blender-<name>.mp4` plus `lageliste.txt`.
  Reihe: `auto` oder `natur`. Kleinbuchstaben, Bindestriche, keine Versionsnummer.

## Was hinein darf
- Graue Blender-Klötzchen ohne Marken, Logos, Kennzeichen oder Personen.
- Lagelisten (Fahrzeuge je Einstellung in Prozent).

## Was nie hinein darf
API-Schlüssel und Zugangsdaten, echte Generierungen, Fahrzeugblätter, Händler- oder
Pressefotos, Personen, E-Mail-Adressen. Das Repo ist **öffentlich**.

## Dateien
- MP4, H.264, ohne Ton, 9:16, 24 fps, 720 × 1280, höchstens ca. 6 MB.
- Eine Datei wird nicht überschrieben, sondern unter neuem Namen abgelegt
  (`blender-berg-kurz.mp4`), damit ein laufender Flow seine Vorlage behält.

## Links
- Rohlink mit Commit-Kennung statt Zweigname verwenden: `raw.githubusercontent.com/PS-K-96/sozial-media-vorlagen/<commit>/<pfad>`.
  Grund: Wird ein Zweig-Link vor dem Hochladen einmal abgerufen, liefert der Zwischenspeicher einige Minuten lang 404.
  Der Commit-Link ist sofort gültig und ändert sich nie.

## Pflege
- Ist das Video gepostet, werden seine Vorlagen aus `medien` gelöscht.
- Wird `medien` größer als ca. 300 MB, setzt Claude den Zweig neu auf (ohne Altlasten);
  laufende Links vorher in `knoten.md` prüfen.
- Jede Änderung an `medien` wird in `knoten.md` nachgetragen.
