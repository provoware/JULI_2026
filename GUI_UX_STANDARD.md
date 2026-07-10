# GUI- und UX-Standard für moderne Provoware-Tools

## 1. Ziel

Die Oberfläche soll schnell erfassbar, modern, kompakt, kontrastreich, flexibel und laientauglich sein.

Die GUI ist nicht Dekoration. Sie ist Arbeitsgeschwindigkeit.

---

## 2. Grundregeln

1. Hauptfunktionen sofort sichtbar machen.
2. Nebenfunktionen sinnvoll gruppieren.
3. Keine Scroll-Hölle erzeugen.
4. Keine überlappenden Elemente.
5. Keine kryptischen Icons ohne Text.
6. Status immer sichtbar machen.
7. Fehler immer mit Lösung erklären.
8. Wichtige Aktionen nicht verstecken.
9. Gefährliche Aktionen absichern.
10. Design muss bei Fenstergrößenänderung stabil bleiben.

---

## 3. Empfohlene Dashboard-Struktur

```text
┌──────────────────────────────────────────────────────────────┐
│ HEADER: Projekt | Status | Speicherstand | Suche | Hilfe     │
├───────────────┬───────────────────────────────┬──────────────┤
│ MODUL-LISTE   │ HAUPTARBEITSBEREICH           │ KONTEXT      │
│ Navigation    │ Editor / Grid / Vorschau      │ Details      │
│ Filter        │ wichtigste Funktionen         │ Aktionen     │
├───────────────┴───────────────────────────────┴──────────────┤
│ STATUS / LOG / HINWEISE / FORTSCHRITT                         │
└──────────────────────────────────────────────────────────────┘
```

Für 3x3-Modultools:

```text
┌────────────── Header-Dashboard ──────────────┐
│ Projekt | Schnellaktionen | Speicherstatus   │
├──── Sidebar ┬──────── 3x3 Grid ───────┬──────┤
│ Module      │ [1] [2] [3]             │ Info │
│ Profile     │ [4] [5] [6]             │ Log  │
│ Settings    │ [7] [8] [9]             │ Help │
├─────────────┴─────────────────────────┴──────┤
│ Mini-Log | Fortschritt | letzte Aktion        │
└───────────────────────────────────────────────┘
```

---

## 4. Layout-Regeln

### Größen

- Header: kompakt, nicht dominierend
- Seitenleisten: einklappbar
- Hauptbereich: größter Bereich
- Logbereich: klein, aber sichtbar
- Buttons: groß genug für sichere Bedienung

### Abstände

- einheitliche Innenabstände
- klare Trennung zwischen Modulen
- keine gequetschten Texte
- kompakte, aber lesbare Kacheln

### Gruppen

Funktionen in Gruppen bündeln:

- Projekt
- Dateien
- Bearbeiten
- Export
- Module
- Einstellungen
- Hilfe
- Debug

---

## 5. Farben und Kontrast

Pflicht:

- Text muss klar lesbar sein
- Buttons müssen sich vom Hintergrund abheben
- Warnungen deutlich markieren
- Erfolg, Fehler und Hinweis optisch unterscheidbar machen
- keine Farbinformation ohne Textzusatz

Empfohlene Zustände:

- Erfolg: „Erfolgreich gespeichert“
- Warnung: „Achtung: Datei existiert bereits“
- Fehler: „Fehler: Pfad nicht gefunden“
- Info: „Bereit“
- Aktiv: „Modul aktiv“
- Inaktiv: „Modul ausgeblendet“

---

## 6. Barrierearme Bedienung

Einbauen, wenn möglich:

- Schriftgröße einstellbar
- hoher Kontrast
- klare Fokusrahmen
- Tastaturbedienung
- Tooltips
- kurze Hilfetexte
- keine winzigen Klickflächen
- keine rein farbliche Bedeutung
- keine blinkenden Elemente
- keine überladenen Animationen

---

## 7. Nutzerfeedback

Jede Aktion braucht Rückmeldung:

| Aktion | Rückmeldung |
|---|---|
| Speichern | „Gespeichert um HH:MM“ |
| Import | „12 Einträge importiert, 2 übersprungen“ |
| Export | Zielpfad anzeigen |
| Fehler | Ursache + Lösung |
| langer Prozess | Fortschritt + Abbruchmöglichkeit |
| AutoSave | dezenter Speicherstatus |

---

## 8. Moderne Oberfläche

Modern bedeutet:

- klare Kacheln
- gute Typografie
- reduzierte Linien
- konsistente Buttons
- dezente Schatten oder Rahmen
- klare Zustände
- kompakte Werkzeugleisten
- flexible Panels
- responsive Anordnung

Modern bedeutet nicht:

- alles bunt machen
- zu viele Effekte
- Icons ohne Erklärung
- verschachtelte Menüs
- versteckte Hauptfunktionen

---

## 9. GUI-Validierung

Vor Abschluss prüfen:

1. Ist die Hauptfunktion sofort erkennbar?
2. Sind alle Texte lesbar?
3. Gibt es sichtbares Feedback?
4. Sind Fehler verständlich?
5. Sind Buttons eindeutig?
6. Funktioniert die Oberfläche bei kleinerem Fenster?
7. Wird nichts verdeckt?
8. Gibt es Hilfe für Laien?
9. Sind gefährliche Aktionen abgesichert?
10. Bleibt die Oberfläche bei langen Prozessen bedienbar?

---

## 10. Spezialregeln für deine Tool-Arbeit

Für Content-, Musik-, Songtext-, Medien- und Modul-Tools:

- schneller Zugriff auf Vorlagen
- Drag-and-drop, wenn sinnvoll
- Suchfeld bei Listen
- Favoriten oder Schnellbuttons
- Export immer sichtbar
- Clipboard-Funktionen klar beschriften
- Dateinamen sicher erzeugen
- Vorschau für Medien
- Log sichtbar, aber nicht störend
- Projektpfad immer erkennbar
