# Kesselklang Festival – Increment Sprint 1

Web-App (PWA) der Stoßtruppschicht für die Sprint-Simulation „Agiles Projektmanagement“ (HdM, WiSe 26/27).
Alle Festivaldaten sind erfunden.

**Sprint Goal 1:** Besuchende finden auch ohne Internet, was wann wo läuft und wo die nächste Toilette und das nächste Essen ist.

| PBI | Was die App kann |
| --- | --- |
| 1 Programm nach Tag und Bühne | 2 Tage, 3 Bühnen, 20 Acts, Filter nach Tag und Bühne, „Läuft gerade“ |
| 2 Geländeplan | Bühnen, Toiletten, Essen, Getränke, Wasser, Erste Hilfe, Filter nach Kategorie, nächster Ort mit Gehzeit |
| beide | Funktioniert im Flugmodus, nachdem die App einmal geladen wurde |

## Dateien

| Datei | Zweck |
| --- | --- |
| `index.html` | Die komplette App inklusive Beispieldaten |
| `sw.js` | Service Worker: speichert die App für den Offline-Betrieb |
| `manifest.webmanifest` | Name und Icon, damit man die App installieren kann |
| `icon-192.png`, `icon-512.png` | App-Icons |

## Veröffentlichen mit GitHub Pages

1. Auf github.com ein neues Repository anlegen, z. B. `festival-app`, Sichtbarkeit **Public**.
2. „Add file › Upload files“: alle Dateien aus diesem Ordner hochladen, „Commit changes“.
3. „Settings › Pages“: Source „Deploy from a branch“, Branch `main`, Ordner `/ (root)`, „Save“.
4. Nach 1–2 Minuten ist die App online: `https://<benutzername>.github.io/festival-app/`
5. Teammitglieder unter „Settings › Collaborators“ einladen.

## Offline testen (Definition of Done)

1. Die Adresse einmal mit Netz auf dem Handy öffnen. Oben rechts steht dann „Offline bereit“.
2. Optional installieren: Android „Zum Startbildschirm hinzufügen“, iPhone Teilen › „Zum Home-Bildschirm“.
3. Flugmodus an, App neu öffnen: alles funktioniert, oben steht „Kein Netz · läuft offline“.

## Änderungen veröffentlichen

1. Geänderte `index.html` hochladen.
2. In `sw.js` die Zeile `const VERSION = 'v1';` hochzählen (`v2`, `v3`, …) und ebenfalls hochladen.
3. Beim nächsten Öffnen mit Netz holt sich das Handy die neue Version und zeigt „Neue Version verfügbar“.
