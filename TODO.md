# TODO – Professionelle Weiterentwicklung des Provoware Präzisions-Agent-Pakets

Datum: 2026-07-10
Status: Planungsliste für die nächste Arbeitsiteration

## 1. Ziel dieser Todo-Liste

Diese Liste übersetzt die vorhandenen Projektregeln in eine klare, priorisierte und effiziente Arbeitsfolge. Sie dient als Steuerdatei für kommende Änderungen und verhindert ungeplante Umbauten.

## 2. Analysegrundlage

Geprüfte Dateien:

- `AGENTS.md` – zentrale Arbeitsregeln, Qualitäts-Gates, Logging-, Backup-, GUI- und Validierungspflichten.
- `README.md` – Paketbeschreibung, Nutzungsablauf und Kernziel.
- `CODEX_KURZPROMPT.md` – kompakte Repo-Arbeitsanweisung.
- `MASTER_PROMPT_TOOLENTWICKLUNG.md` – vollständiger Ablauf für neue Tools und größere Umbauten.
- `GUI_UX_STANDARD.md` – UI-/UX-Regeln für moderne, laientaugliche Werkzeuge.
- `PERFORMANCE_EFFIZIENZ_STANDARD.md` – Regeln zu Code-Sparsamkeit, Startzeit, Dateioperationen und Ressourcenschonung.
- `VALIDIERUNG_QA_STANDARD.md` – Qualitäts-Gates, Testmatrix und Fehlermeldungsstandard.
- `PROJEKTSTRUKTUR_TEMPLATE.md` – Zielstruktur für Desktop-, HTML- und kleine Python-Tools.
- `CHECKLISTE_ABSCHLUSS.md` – Abschluss- und Übergabekriterien.
- `CHANGELOG_TEMPLATE.md` – Vorlage für Änderungsdokumentation.
- `TESTPROTOKOLL_TEMPLATE.md` – Vorlage für Prüfnachweise.
- `PAKETPRUEFUNG.md` – vorhandener Prüfbericht zum Dokumentationspaket.
- `DATEI_INDEX.txt` – bestehender Dateiindex.

## 3. Aktueller Projektzustand

- Das Repository ist aktuell ein Dokumentations- und Regelpaket, kein lauffähiges Softwaretool.
- Es gibt keinen Anwendungseinstieg wie `main.py`, `index.html` oder ein Paketmanifest.
- Es gibt keine produktive Logik, keine GUI, keine Tests und keine Abhängigkeiten.
- Die vorhandenen Standards decken die wichtigsten Qualitätsbereiche bereits gut ab.
- Es fehlt eine operative Aufgabenliste, die aus den Standards konkrete nächste Schritte ableitet.

## 4. Patch-Plan für diese Iteration

| Punkt | Entscheidung |
|---|---|
| Ziel | Eine detaillierte und priorisierte Todo-Liste ergänzen. |
| Betroffene Datei | `TODO.md` neu anlegen. |
| Betroffene Blöcke | Ganze Datei, da sie neu ist. |
| Patchgrund | Die vorhandenen Regeln brauchen eine praktische Arbeitsreihenfolge für Folgeiterationen. |
| Risiken | Gering: reine Dokumentation, keine Laufzeitlogik, keine bestehenden Dateien werden verändert. |
| Bewusste Nicht-Änderungen | Keine Umbenennungen, keine Strukturänderungen, keine neuen Code-Dateien, keine Templates ändern. |
| Validierung | Dateiliste prüfen, Markdown-Inhalt stichprobenartig lesen, Git-Diff prüfen. |

## 5. Priorisierte Aufgaben

### P0 – Sofort sinnvoll, geringes Risiko

#### 1. Paketprüfung neu erzeugen oder manuell aktualisieren

- Ziel: `PAKETPRUEFUNG.md` soll den neuen Dateiumfang korrekt nennen.
- Betroffene Datei: `PAKETPRUEFUNG.md`.
- Grund: Der Prüfbericht ist durch die neue Datei sonst nicht mehr vollständig.
- Risiko: gering bis mittel, wenn unklar ist, ob der Bericht automatisch erzeugt wurde.
- Validierung: Prüfen, ob alle Dateien im Bericht aufgeführt sind.
- Nicht ändern: Bewertung nur ändern, wenn neue Prüfung wirklich durchgeführt wurde.

### P1 – Hoher Nutzen für Folgearbeiten

#### 2. Echte Beispielstruktur ergänzen

- Ziel: Ein minimales Beispielprojekt zeigen, ohne das Regelpaket in ein Tool umzubauen.
- Mögliche Dateien: `examples/desktop_tool_minimal/README.md` oder `examples/single_html_minimal/README.md`.
- Grund: Nutzer verstehen die Standards schneller anhand eines konkreten Beispiels.
- Risiko: mittel, weil neue Struktur die Paketgröße erhöht.
- Vorbedingung: Entscheiden, ob Beispiele wirklich zum Paketumfang gehören sollen.
- Validierung: Beispiel muss vollständig, aber bewusst klein bleiben.
- Nicht ändern: Keine produktive App starten, solange nur Dokumentationspaket gewünscht ist.

#### 3. Checklisten stärker mit Qualitäts-Gates verbinden

- Ziel: `CHECKLISTE_ABSCHLUSS.md` und `VALIDIERUNG_QA_STANDARD.md` logisch angleichen.
- Betroffene Dateien: beide genannten Dokumente.
- Grund: Reduziert Doppelarbeit und macht Abschlussprüfungen eindeutiger.
- Risiko: mittel, weil doppelte Inhalte versehentlich widersprüchlich werden können.
- Validierung: Jede Gate-Kategorie muss exakt einer Prüfkategorie zuordenbar sein.
- Nicht ändern: Keine großflächige Umformulierung ohne konkreten Nutzen.

#### 4. Änderungsprotokoll als echte Datei vorbereiten

- Ziel: Neben `CHANGELOG_TEMPLATE.md` optional eine echte `CHANGELOG.md` anlegen.
- Grund: Künftige Änderungen können sofort dokumentiert werden.
- Risiko: gering.
- Vorbedingung: Entscheiden, ob das Paket selbst versioniert dokumentiert werden soll.
- Validierung: Datum, Version und Einträge müssen konsistent sein.
- Nicht ändern: Template nicht ersetzen.

### P2 – Qualitätsverbesserung mit moderatem Aufwand

#### 5. Konsistente Dateinamenstrategie festlegen

- Ziel: Klären, ob Paketdateien deutsch sprechend bleiben oder ob eine nummerierte Projektdatei-Konvention gelten soll.
- Betroffene Dateien: Dokumentation, vor allem `README.md`, `PROJEKTSTRUKTUR_TEMPLATE.md`, `AGENTS.md`.
- Grund: Aktuelle Paketdateien nutzen sprechende Namen, während die Tool-Konvention nummerierte Namen empfiehlt.
- Risiko: mittel, weil Umbenennungen Links und Nutzungsgewohnheiten brechen können.
- Empfehlung: Keine Umbenennung bestehender Paketdateien; stattdessen Regel präzisieren.
- Validierung: Alle Querverweise bleiben korrekt.

#### 6. Testprotokoll für Dokumentationspakete ergänzen

- Ziel: `TESTPROTOKOLL_TEMPLATE.md` enthält aktuell vor allem Tool-Tests; für reine Dokumentationspakete fehlt eine schlanke Variante.
- Betroffene Datei: `TESTPROTOKOLL_TEMPLATE.md` oder neue Vorlage.
- Grund: Dieses Repository ist aktuell ein Dokumentationspaket.
- Risiko: gering bis mittel.
- Validierung: Vorlage muss beide Fälle klar unterscheiden: Toolprüfung und Dokumentationsprüfung.
- Nicht ändern: Bestehende Tool-Testmatrix nicht schwächen.

#### 7. Fehlermeldungsstandard mit Beispielen erweitern

- Ziel: Mehr Beispiele für Datei-, Import-, Export-, GUI- und Berechtigungsfehler.
- Betroffene Datei: `VALIDIERUNG_QA_STANDARD.md`.
- Grund: Laientaugliche Fehlermeldungen sind ein Kernziel.
- Risiko: gering.
- Validierung: Beispiele müssen das Schema Problem, Ursache, Lösung, Status einhalten.
- Nicht ändern: Keine technischen Spezialfälle überladen.

### P3 – Optional, nur bei klarem Bedarf

#### 8. Automatisches Paketprüfskript entwickeln

- Ziel: Ein kleines Skript prüft Pflichtdateien, Zeichenzahlen, Kernbegriffe und Indexkonsistenz.
- Mögliche Datei: `tools/check_package.py`.
- Grund: `PAKETPRUEFUNG.md` wirkt automatisch erzeugt, aber das Erzeugungsskript fehlt.
- Risiko: mittel, weil erstmals Code in das Dokumentationspaket kommt.
- Vorbedingung: Klären, ob das Repository codefrei bleiben soll.
- Validierung: Skriptlauf erzeugt reproduzierbare Ausgabe.
- Nicht ändern: Keine externen Abhängigkeiten verwenden.

#### 9. Release-Checkliste ergänzen

- Ziel: Kurze Datei für Versionierung, Archivierung und Übergabe.
- Mögliche Datei: `RELEASE_CHECKLISTE.md`.
- Grund: Nützlich, wenn das Paket regelmäßig veröffentlicht wird.
- Risiko: gering.
- Validierung: Liste darf sich nicht unnötig mit `CHECKLISTE_ABSCHLUSS.md` doppeln.
- Nicht ändern: Keine CI/CD-Struktur ohne Auftrag.

## 6. Effiziente Reihenfolge für die nächste Iteration

1. Zuerst die verbleibende P0-Aufgabe prüfen.
2. Danach `git diff` prüfen.
3. Nur Markdown- und Indexkonsistenz validieren.
4. Ergebnis kurz im Änderungsprotokoll dokumentieren.
5. Erst nach Freigabe oder klarem Auftrag P1-Aufgaben beginnen.

## 7. Risiken und Gegenmaßnahmen

| Risiko | Gegenmaßnahme |
|---|---|
| Dokumente wachsen zu stark | Nur konkrete Lücken schließen, keine Wiederholungen einbauen. |
| Regeln widersprechen sich | Betroffene Regelstellen vor Änderung nebeneinander prüfen. |
| Dateiumbenennungen brechen Nutzung | Bestehende Dateinamen beibehalten, Querverweise nur ergänzen. |
| Code wird ohne Bedarf eingeführt | Automatisierung erst ab P3 und nur mit klarem Nutzen. |
| Prüfbericht wird ungenau | Nur dann aktualisieren, wenn eine echte Prüfung durchgeführt wurde. |

## 8. Bewusst nicht geplante Arbeiten

- Kein neues Softwaretool erstellen.
- Keine GUI bauen.
- Keine Ordnerstruktur für ein Beispieltool anlegen, solange das nicht ausdrücklich gewünscht ist.
- Keine bestehenden Standards großflächig umschreiben.
- Keine externen Abhängigkeiten hinzufügen.
- Keine automatisierten Tests für nicht vorhandenen Anwendungscode erstellen.

## 9. Definition of Done für diese Todo-Datei

- Die Datei beschreibt konkrete nächste Schritte.
- Jede Aufgabe hat Ziel, betroffene Datei, Grund, Risiko und Validierung.
- Aufgaben sind priorisiert.
- Nicht-Änderungen sind klar genannt.
- Die Liste kann ohne Zusatzwissen für die nächste Iteration genutzt werden.
