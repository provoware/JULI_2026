# Performance- und Effizienzstandard

## 1. Ziel

Software soll schnell starten, flüssig reagieren, wenig Ressourcen verbrauchen und trotzdem robust bleiben.

Effizienz bedeutet:

- weniger unnötiger Code
- klare Datenwege
- schnelle Bedienung
- keine blockierende Oberfläche
- keine unnötigen Abhängigkeiten
- keine riskanten Abkürzungen

---

## 2. Code-Sparsamkeit

Pflicht:

1. Keine Funktion ohne klaren Zweck.
2. Keine doppelte Logik.
3. Keine unnötigen Klassen.
4. Keine riesigen Dateien, wenn Module sinnvoller sind.
5. Keine übermäßige Verschachtelung.
6. Keine Bibliothek für triviale Aufgaben.
7. Keine globale Magie.
8. Keine versteckten Seiteneffekte.

Gute Regel:

> Erst einfach, dann robust, dann schnell. Nicht umgekehrt.

---

## 3. Startgeschwindigkeit

Optimieren:

- schwere Imports nur laden, wenn nötig
- große Dateien nicht beim Start komplett einlesen
- Datenbanken nur initial prüfen
- Vorschauen später laden
- Konfiguration klein halten
- Startlog kurz halten

Nicht tun:

- komplette Medienordner beim Start scannen
- große Thumbnails sofort generieren
- externe Programme sofort starten
- lange Netzwerk- oder Dateiprüfungen blockierend ausführen

---

## 4. GUI-Reaktionsgeschwindigkeit

Bei Desktop-GUI:

- Hauptthread frei halten
- lange Aufgaben in Worker auslagern
- Fortschritt anzeigen
- Abbruch ermöglichen
- Buttons während Prozess sinnvoll sperren
- UI nach Prozess sauber wieder aktivieren
- Fehler aus Worker zurück an GUI melden

Typische lange Aufgaben:

- FFmpeg-Konvertierung
- Import großer Dateien
- Export vieler Daten
- Thumbnail-Erzeugung
- Medienanalyse
- Backup-ZIP
- große Suchläufe

---

## 5. Dateioperationen

Schnell und sicher:

- vor Verarbeitung Existenz prüfen
- Dateigröße prüfen, wenn relevant
- nur benötigte Daten laden
- Schreibrechte prüfen
- temporäre Datei nutzen und dann atomar ersetzen, wenn sinnvoll
- nie ohne Schutz überschreiben
- bei Fehler Teildateien bereinigen

---

## 6. Datenhaltung

Bei SQLite:

- Verbindung sauber öffnen/schließen
- Tabellen beim Start prüfen
- Transaktionen für mehrere Schreibvorgänge
- Indexe für Suchfelder, wenn Daten wachsen
- keine großen BLOBs ohne Grund in DB speichern
- Dateipfade statt Mediendateien speichern, wenn sinnvoll

Bei JSON:

- vor dem Schreiben Backup oder temporäre Datei
- JSON-Fehler abfangen
- Standardstruktur reparieren, wenn möglich
- große JSON-Dateien vermeiden

Bei localStorage:

- Datenmenge begrenzen
- Exportfunktion anbieten
- Import validieren
- Autosave entprellen

---

## 7. Logging-Effizienz

Logs sollen helfen, nicht bremsen.

Regeln:

- keine Logflut bei Schleifen
- Wiederholungsfehler zusammenfassen
- Logdateien rotieren oder begrenzen
- Debug-Logging abschaltbar machen
- Nutzermeldungen kurz halten
- technische Details in Log, klare Meldung in GUI

---

## 8. Medienverarbeitung

Für Audio, Bild, Video:

- Thumbnails statt Vollbilder in Übersichten
- Bildvorschau skalieren
- große Dateien nicht unnötig kopieren
- FFmpeg-Prozesse sequentiell oder kontrolliert parallel
- Fortschritt anzeigen
- Zielnamen automatisch kollisionssicher erzeugen
- Ergebnisdatei nach Prozess prüfen

Nach FFmpeg:

- existiert Ausgabedatei?
- Dateigröße > 0?
- Prozesscode 0?
- Fehlerausgabe leer oder erklärbar?
- Log speichern?

---

## 9. Performance-Prüfung

Vor Abschluss prüfen:

1. Startet das Tool schnell genug?
2. Blockiert die Oberfläche?
3. Gibt es unnötige Dauerschleifen?
4. Werden große Daten unnötig geladen?
5. Gibt es doppelte Berechnungen?
6. Werden Fehler unnötig oft geloggt?
7. Gibt es Cache-Bedarf?
8. Sind externe Prozesse kontrolliert?
9. Werden Ressourcen nach Nutzung freigegeben?
10. Bleibt Code trotz Optimierung lesbar?

---

## 10. Prioritäten

Reihenfolge bei Optimierung:

1. Abstürze verhindern
2. Datenverlust verhindern
3. Bedienblockaden verhindern
4. Startzeit verbessern
5. Hauptaktionen beschleunigen
6. Speicherverbrauch senken
7. Code vereinfachen
8. kosmetische Optimierung

---

## 11. Verbotene Performance-Fehler

Nicht erlaubt:

- GUI im Hauptthread blockieren
- komplette Ordner ohne Bedarf scannen
- jede Sekunde unnötig speichern
- riesige Logs schreiben
- große Originalbilder in Listen anzeigen
- Imports auf Verdacht einbauen
- neue Abhängigkeiten ohne klaren Nutzen
- Fehler ignorieren, um schneller zu wirken
