# Projektstruktur-Template

## 1. Standardstruktur für Desktop-Tools

```text
/Projektname
├── main.py
├── config.py
├── requirements.txt
├── README.md
├── AGENTS.md
├── CHANGELOG.md
├── TESTPROTOKOLL.md
├── modules/
│   ├── __init__.py
│   ├── app_controller.py
│   ├── ui_main.py
│   ├── ui_components.py
│   ├── storage.py
│   ├── validators.py
│   ├── logger_setup.py
│   ├── workers.py
│   └── helpers.py
├── data/
│   └── .gitkeep
├── imports/
│   └── .gitkeep
├── exports/
│   └── .gitkeep
├── logs/
│   └── .gitkeep
├── backups/
│   └── .gitkeep
├── assets/
│   └── .gitkeep
├── trash/
│   └── .gitkeep
└── tests/
    ├── __init__.py
    └── test_basic.py
```

---

## 2. Dateizwecke

| Datei/Ordner | Zweck |
|---|---|
| `main.py` | Startpunkt der Anwendung |
| `config.py` | zentrale Einstellungen, Pfade, Konstanten |
| `requirements.txt` | Abhängigkeiten |
| `README.md` | Bedienung, Installation, Zweck |
| `AGENTS.md` | Arbeitsregeln für Entwicklungsagenten |
| `CHANGELOG.md` | Änderungsverlauf |
| `TESTPROTOKOLL.md` | dokumentierte Tests |
| `modules/app_controller.py` | Verbindung zwischen UI, Logik und Daten |
| `modules/ui_main.py` | Hauptfenster |
| `modules/ui_components.py` | wiederverwendbare GUI-Komponenten |
| `modules/storage.py` | Speichern, Laden, Export, Import |
| `modules/validators.py` | Eingabeprüfung |
| `modules/logger_setup.py` | Logging |
| `modules/workers.py` | lange Prozesse/Threads |
| `modules/helpers.py` | kleine Hilfsfunktionen |
| `data/` | lokale Arbeitsdaten |
| `imports/` | Importquellen oder Kopien |
| `exports/` | Ausgaben |
| `logs/` | Logdateien |
| `backups/` | Sicherungen |
| `assets/` | Bilder, Icons, Vorlagen |
| `trash/` | sicherer Papierkorb |
| `tests/` | Tests |

---

## 3. Namensregeln

Neue Projektdateien:

```text
Projektname_001_main.py
Projektname_002_config.py
Projektname_003_ui.py
Projektname_004_storage.py
Projektname_005_validators.py
Projektname_006_workers.py
Projektname_007_tests.py
```

Exportdateien:

```text
Projektname_Export_YYYYMMDD_HHMMSS.json
Projektname_Backup_YYYYMMDD_HHMMSS.zip
Projektname_Log_YYYYMMDD.txt
```

---

## 4. Minimalstruktur für Single-HTML-Tools

```text
/Projektname
├── index.html
├── README.md
├── CHANGELOG.md
├── TESTPROTOKOLL.md
├── exports/
├── backups/
└── examples/
```

Regeln für Single-HTML:

- CSS, HTML und JS klar trennen durch kommentierte Abschnitte
- localStorage absichern
- Export/Import einbauen
- keine externen CDNs, wenn Offline gefordert
- Fehler sichtbar anzeigen
- Autosave mit Status anzeigen

---

## 5. Minimalstruktur für kleine Python-Tools

```text
/Projektname
├── main.py
├── README.md
├── CHANGELOG.md
├── logs/
├── exports/
└── backups/
```

Nur verwenden, wenn das Tool wirklich klein bleibt.

---

## 6. Erweiterungspunkte

Neue Module sollen immer so eingebunden werden, dass:

- sie deaktivierbar sind
- sie eigene Validierung haben
- sie eigene Hilfetexte haben
- sie keine anderen Module unnötig beschädigen
- sie im Log erkennbar sind
- sie dokumentiert werden

---

## 7. Projektstart-Check

Beim ersten Start prüfen:

1. Projektordner vorhanden?
2. Unterordner vorhanden?
3. Schreibrechte vorhanden?
4. Konfiguration vorhanden?
5. Logdatei schreibbar?
6. Datenbank oder Speicherdatei vorhanden?
7. fehlende Ordner automatisch anlegen?
8. Nutzer verständlich informieren?
