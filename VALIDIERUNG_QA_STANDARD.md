# Validierungs- und QA-Standard

## 1. Ziel

Jede Änderung muss beweisbar sicherer, besser oder funktionaler sein.

Ein Tool gilt nicht als fertig, nur weil Code geschrieben wurde. Es gilt erst als fertig, wenn es geprüft, dokumentiert und realistisch benutzbar ist.

---

## 2. Qualitäts-Gates

### Gate 1 – Verständnis

Bestanden, wenn:

- Zweck verstanden
- relevante Dateien gefunden
- Datenfluss erkannt
- GUI-Logik erkannt
- Risiken benannt

### Gate 2 – Struktur

Bestanden, wenn:

- Module sinnvoll getrennt
- Dateinamen klar
- keine unnötigen Dateien
- keine Duplikate
- keine unklaren Abhängigkeiten

### Gate 3 – Code

Bestanden, wenn:

- Syntax korrekt
- Imports korrekt
- Variablen definiert
- Funktionen vollständig
- Fehlerbehandlung vorhanden
- kein toter Code ohne Grund

### Gate 4 – Daten

Bestanden, wenn:

- Eingaben validiert
- Speicherfehler abgefangen
- keine ungewollte Überschreibung
- Import/Export geprüft
- Backup/Papierkorb bei Risiko

### Gate 5 – GUI

Bestanden, wenn:

- Hauptfunktion sichtbar
- Status sichtbar
- Fehlermeldungen verständlich
- Oberfläche nicht blockiert
- Layout bleibt stabil
- Texte sind lesbar

### Gate 6 – Performance

Bestanden, wenn:

- keine unnötigen Dauerschleifen
- keine blockierenden Langläufer
- große Daten sparsam behandelt
- externe Prozesse kontrolliert
- Start plausibel schnell

### Gate 7 – Dokumentation

Bestanden, wenn:

- README aktuell
- Changelog aktuell
- Testprotokoll vorhanden
- offene Punkte genannt
- nächste Schritte benannt

---

## 3. Validierung von Nutzereingaben

Prüfe immer:

| Eingabeart | Prüfung |
|---|---|
| Text | leer, zu lang, Sonderzeichen, Duplikat |
| Zahl | leer, Bereich, Typ, negativ, Nullfall |
| Datei | Existenz, Endung, Rechte, Größe |
| Ordner | Existenz, Schreibrechte, Erstellbarkeit |
| Import | Format, Pflichtfelder, beschädigte Daten |
| Export | Zielordner, Dateiname, Überschreibung |
| Medien | unterstütztes Format, lesbar, Größe |
| Datenbank | Verbindung, Tabelle, Spalten, Transaktion |

---

## 4. Fehlermeldungsstandard

Jede Fehlermeldung muss laientauglich sein.

Schema:

```text
Problem: Was ist passiert?
Ursache: Warum ist es wahrscheinlich passiert?
Lösung: Was soll der Nutzer tun?
Status: Wurde etwas gespeichert oder abgebrochen?
```

Beispiel:

```text
Problem: Die Datei konnte nicht importiert werden.
Ursache: Das Format wird nicht unterstützt oder die Datei ist beschädigt.
Lösung: Bitte eine gültige JSON- oder TXT-Datei wählen.
Status: Der Import wurde abgebrochen. Bestehende Daten wurden nicht verändert.
```

---

## 5. Testmatrix

### Start

- Programm startet normal
- fehlende Ordner werden erstellt
- Log wird angelegt
- Konfiguration wird geladen
- fehlende Konfiguration wird mit Standardwerten erstellt

### Standardnutzung

- Hauptfunktion läuft
- Speichern funktioniert
- Laden funktioniert
- Export funktioniert
- Import funktioniert
- Suche/Filter funktioniert, falls vorhanden

### Fehlerfälle

- leere Eingabe
- ungültige Datei
- fehlender Ordner
- keine Schreibrechte
- doppelte Namen
- Sonderzeichen
- Abbruch durch Nutzer
- beschädigte Konfiguration

### GUI

- Fenster kleiner ziehen
- Fenster größer ziehen
- Buttons prüfen
- Tooltips prüfen
- Statusmeldungen prüfen
- lange Texte prüfen
- Fehlerdialog prüfen

### Stabilität

- Neustart nach Speichern
- Mehrfachausführung
- wiederholter Import
- wiederholter Export
- Abbruch während Prozess
- große Datenmenge, falls relevant

---

## 6. Testprotokoll-Pflicht

Nach jeder größeren Änderung dokumentieren:

```text
Datum:
Aufgabe:
Geänderte Dateien:
Getestete Funktionen:
Ergebnis:
Gefundene Fehler:
Korrekturen:
Nicht getestet:
Bekannte Risiken:
Nächster Schritt:
```

---

## 7. Selbstprüfung vor Ausgabe

Vor Abschluss diese Fragen beantworten:

1. Habe ich das Ziel vollständig verstanden?
2. Habe ich unnötige Änderungen vermieden?
3. Habe ich alle betroffenen Dateien genannt?
4. Habe ich Syntax und Imports geprüft?
5. Habe ich kritische Eingaben validiert?
6. Habe ich Speicherfehler abgesichert?
7. Habe ich GUI-Feedback berücksichtigt?
8. Habe ich Performancefallen vermieden?
9. Habe ich Tests dokumentiert?
10. Habe ich bekannte Grenzen ehrlich genannt?

---

## 8. Abbruchregel

Wenn ein Qualitäts-Gate fehlschlägt:

1. Fehler klar benennen.
2. Ursache erklären.
3. Korrektur planen.
4. Korrektur umsetzen.
5. Gate erneut prüfen.
6. Rest-Risiko dokumentieren.

Nicht erlaubt:

- Fehler ignorieren
- Prüfung überspringen
- Erfolg behaupten ohne Grundlage
- offene Probleme verstecken
