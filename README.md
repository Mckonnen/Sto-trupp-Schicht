# Kesselklang Festival – Website, Increment Sprint 1

Website der Stoßtruppschicht für die Sprint-Simulation „Agiles Projektmanagement“ (HdM, WiSe 26/27).
Das Festival, das Gelände und alle Acts sind frei erfunden.

**Sprint Goal 1:** Besuchende finden auch ohne Internet, was wann wo läuft und wo die nächste Toilette und das nächste Essen ist.

## Seiten

| Seite | Adresse | Inhalt |
| --- | --- | --- |
| Jetzt | `#start` | Was gerade auf jeder Bühne läuft, was danach kommt, nächste Toilette, Essen, Wasser, Erste Hilfe |
| Programm | `#programm` | 20 Acts an 2 Tagen auf 3 Bühnen, Filter nach Tag und Bühne, Ansicht als Liste oder Zeitplan |
| Geländeplan | `#plan` | Bühnen, Toiletten, Essen, Getränke, Wasser, Erste Hilfe, Filter nach Kategorie, Standort, Entfernungen |
| Infos | `#infos` | Termine, Bühnen, Hinweise, wie man die Seite offline nutzt |
| Technik-Check | `#technik` | Prüft auf dem Gerät, ob die Seite offline gespeichert ist (für den Offline-Test) |

## Sprint Backlog: was umgesetzt ist

| Nr | Aufgabe | Stand |
| --- | --- | --- |
| 3 | Beispiel-Festival festlegen | Kesselklang Festival, 9.–10. Juli 2027, 3 Bühnen, 20 Acts, Gelände mit 15 Orten |
| 4 | Website, die nach dem ersten Laden offline läuft | Service Worker in `sw.js`, Statusanzeige oben rechts |
| 5 | Programm mit Filter nach Tag und Bühne | Seite „Programm“ |
| 6 | Geländeplan mit Filter nach Kategorie | Seite „Geländeplan“ |
| 7 | Offline-Test auf 3 Handys | Vorlage in `Testprotokoll-Offline.md`, Hilfe über `#technik` |
| 8 | Prüfung gegen Acceptance Criteria und DoD | `Pruefung-AC-DoD.md` |
| 9 | Review vorbereiten | `Review-Vorbereitung.md` |

## Dateien

| Datei | Zweck | Ins Repository? |
| --- | --- | --- |
| `index.html` | Die komplette Website inklusive Beispieldaten | ja |
| `sw.js` | Service Worker für den Offline-Betrieb | ja |
| `manifest.webmanifest` | Name und Icon für „Zum Home-Bildschirm“ | ja |
| `icon-192.png`, `icon-512.png` | Icons | ja |
| `README.md` | Diese Beschreibung | ja |
| `*.md` (Test, Prüfung, Review) | Unterlagen für den Sprint | optional |

## Aktualisieren auf GitHub Pages

1. Im Repository „Add file › Upload files“ und `index.html`, `sw.js` und `manifest.webmanifest` hochladen (vorhandene Dateien werden ersetzt), „Commit changes“.
2. Nach 1–2 Minuten ist die neue Version online.
3. Auf Handys, die die alte Version gespeichert haben, erscheint beim nächsten Öffnen mit Netz „Neue Version verfügbar“ › „Neu laden“.

Bei jeder späteren Änderung an `index.html` in `sw.js` die Zeile `const VERSION = 'v2';` hochzählen (`v3`, `v4`, …), sonst zeigen die Handys weiter die alte gespeicherte Version.

## Daten ändern

Alle Beispieldaten stehen oben im `<script>` von `index.html`:
`FEST` (Name, Ort, Termine), `STAGES` (Bühnen), `ACTS` (Programm), `POIS` (Orte im Gelände), `LANDMARKS` (Auswahl „Ich stehe bei …“).
Koordinaten im Plan sind Meter: x von 0 bis 400 (West nach Ost), y von 0 bis 560 (Nord nach Süd).
