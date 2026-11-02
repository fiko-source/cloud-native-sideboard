
# Roadmap – Cloud-Native Sideboard Manufacturer

## 1. Projektübersicht

Ziel des Projekts ist die Entwicklung einer **Cloud-Native Web-Anwendung für einen fiktiven Sideboard-Hersteller** im Rahmen des Moduls *Cloud-based Web Application Development*.

Die Anwendung wird in mehrere fachlich getrennte Webservices aufgeteilt und mithilfe einer hierarchischen Multi-Agent-Architektur entwickelt.

Dabei werden zwei Systeme unterschieden:

- **System A – Cloud-Native Web-Anwendung:** Frontend, eigenständige Backend-Webservices, Datenhaltung und Docker Compose.
- **System B – Multi-Agent-Entwicklungsumgebung:** Hermes Agent als zentraler Orchestrator, spezialisierte Hermes-Subagents und Codex CLI als Coding-Agent.

Die Erfüllung der offiziellen Prüfungsanforderungen hat Vorrang vor dem Multi-Agent-Experiment.

### 1.1 Technische Umgebung

| Komponente | Technologie |
|---|---|
| Entwicklungsrechner | MacBook Air M3, 16 GB RAM |
| Hauptagent | Hermes Agent |
| Coding-Agent | OpenAI Codex CLI |
| Versionskontrolle | Git / GitHub |
| Frontend | HTML, CSS, JavaScript |
| Backend | Node.js |
| Datenhaltung | MySQL, MinIO, Redis (nach Bedarf) |
| Containerisierung | Docker / Docker Compose |
| Kommunikation | REST APIs / OpenAPI |

Die konkrete Technologieverteilung wird im Rahmen der Architekturplanung festgelegt.

### 1.2 Geplante Multi-Agent-Architektur

```text
Du (Product Owner)
│
└── Hermes Main Agent
    │   Planung, Koordination und Integration
    │
    ├── Frontend-Subagent
    │   └── Codex CLI
    │
    ├── Service-A-Subagent
    │   └── Codex CLI
    │
    └── Service-B-Subagent
        └── Codex CLI
```

Die dargestellten Subagents sind exemplarisch. Ihre konkreten Verantwortlichkeiten werden nach der Festlegung der Microservice-Architektur definiert.

Hermes Main koordiniert die Entwicklung. Spezialisierte Subagents übernehmen abgegrenzte Aufgaben und können Codex für die Implementierung einsetzen.

---

## 2. Projektphasen und Meilensteine

### Phase 1 – Anforderungen und Themenwahl

**Status:** Abgeschlossen  
**Geschätzter Aufwand:** 2–3 Tage

**Aufgaben:**

- [x] Prüfungsanforderungen analysieren
- [x] `REQUIREMENTS.md` als Anforderungsbasis erstellen
- [x] Einzelprojektthema auswählen
- [x] Themenwahl gegenüber der Gruppenprojektarbeit abgrenzen
- [x] Architekturvorlagen aus Relax für die Abgabe vormerken
- [x] Grundlegenden Funktionsumfang festlegen

**Ergebnis:**

Das Projektthema **Sideboard Manufacturer** wurde ausgewählt.

Die Anwendung umfasst einen grafischen Sideboard-Konfigurator, eine Bestellfunktion, einen Zubehör-Shop mit Warenkorb, Impressionen und eine Community-Funktion.

Das AI-Feature ist für die Einzelprojektarbeit optional.

**Meilenstein:** Vollständiger, festgelegter Projektumfang.

---

### Phase 2 – Lokale Agentenumgebung

**Status:** Abgeschlossen  
**Geschätzter Aufwand:** 2–4 Tage

**Aufgaben:**

- [x] Hermes Agent und Codex CLI auf macOS installieren
- [x] Hermes und Codex aktualisieren
- [x] Modellanbieter und Authentifizierung konfigurieren
- [x] Git-Repository initialisieren und mit GitHub verbinden
- [x] Mitgelieferten Hermes-Codex-Skill überprüfen
- [x] Direkte Delegation von Hermes an Codex testen
- [x] Hierarchische Delegation über Hermes-Subagent testen
- [x] Automatisierte Codegenerierung überprüfen
- [x] Testausführung und Ergebnisvalidierung überprüfen

**Integrationstest 1 – Direkte Delegation:**

```text
Hermes Main → Codex CLI → Implementierung → Tests
```

- Implementierung einer JavaScript-Funktion `isPrime(number)`
- 8 von 8 Unit-Tests bestanden
- Ergebnis erfolgreich durch Hermes validiert

**Integrationstest 2 – Hierarchische Delegation:**

```text
Hermes Main → Hermes-Subagent → Codex CLI
                                  ↓
                             Implementierung
                                  ↓
                              Unit-Tests
                                  ↓
                            Ergebnisbericht
```

- Implementierung einer JavaScript-Funktion `calculateTotal(items)`
- 7 von 7 Unit-Tests bestanden
- Erfolgreiche Rückmeldung an Hermes Main
- Erneute Validierung durch den Hauptagenten

**Meilenstein:** Hermes kann Codex direkt und über einen Subagenten beauftragen und die Ergebnisse überprüfen.

---

### Phase 3 – Microservice-Architektur

**Status:** Offen – Nächste Phase  
**Geschätzter Aufwand:** 4–6 Tage

**Aufgaben:**

- [ ] Anwendung in fachlich sinnvolle Webservices aufteilen
- [ ] Verantwortlichkeiten und Datenhoheit pro Service festlegen
- [ ] REST-Schnittstellen mit OpenAPI definieren
- [ ] Datenhaltung und Kommunikation zwischen Services planen
- [ ] Fehlerbehandlung und Abhängigkeiten konzipieren
- [ ] Frontend- und Backend-Architektur festlegen
- [ ] Docker-Compose-Architektur entwerfen
- [ ] Architekturdiagramm erstellen
- [ ] Wesentliche Architekturentscheidungen dokumentieren

**Meilenstein:** Freigegebene Microservice-Architektur mit verbindlich definierten API-Verträgen.

---

### Phase 4 – Skills und Subagent-Orchestrierung

**Status:** Offen  
**Geschätzter Aufwand:** 4–6 Tage

**Aufgaben:**

- [ ] Servicespezifische Hermes-Subagent-Rollen definieren
- [ ] Regeln für die Delegation an Codex festlegen
- [ ] Gemeinsame Skills entwickeln und einzeln testen
- [ ] Parallele Ausführung mehrerer Subagents testen
- [ ] Git-Worktree-Isolation einrichten
- [ ] Codex-Aufrufe auf maximal zwei gleichzeitige Prozesse begrenzen
- [ ] Freigabe- und Sicherheitsregeln konfigurieren
- [ ] Automatische Fehlerkorrektur und Eskalation definieren
- [ ] Einheitliche Aufgabenübergaben und Abschlussberichte festlegen

**Meilenstein:** Spezialisierte Subagents können eigenständig und kontrolliert an abgegrenzten Services arbeiten.

---

### Phase 5 – Implementierung der Webservices

**Status:** Offen  
**Geschätzter Aufwand:** 2–3 Wochen

**Aufgaben:**

- [ ] Backend-Webservices entlang der definierten API-Verträge implementieren
- [ ] Datenmodelle und Datenbankanbindungen entwickeln
- [ ] Frontend und grafischen Sideboard-Konfigurator erstellen
- [ ] Konfigurationsmöglichkeiten für Größen, Farben und Varianten integrieren
- [ ] Bestellfunktion implementieren
- [ ] Zubehör-Shop mit Warenkorb entwickeln
- [ ] Impressionen mit Bildern und Videos integrieren
- [ ] Community-Funktion zur Anzeige von Sideboard-Entwürfen entwickeln
- [ ] Frontend mit den Webservices verbinden
- [ ] Unit-Tests und Service-Integrationstests erstellen

Die Implementierung soll überwiegend durch spezialisierte Hermes-Subagents erfolgen, die Codex für konkrete Entwicklungsaufgaben einsetzen.

**Meilenstein:** Sämtliche verpflichtenden Funktionen sind implementiert.

---

### Phase 6 – Gesamtsystem und Qualitätssicherung

**Status:** Offen  
**Geschätzter Aufwand:** 5–7 Tage

**Aufgaben:**

- [ ] Webservices über Docker Compose integrieren
- [ ] Container-Konfigurationen und Abhängigkeiten überprüfen
- [ ] API-Integrationstests ausführen
- [ ] End-to-End-Tests durchführen
- [ ] Automatischen Start aus einem frisch entpackten Projektverzeichnis prüfen
- [ ] Fehlerfälle und Service-Ausfälle testen
- [ ] Architektur und Implementierung abgleichen
- [ ] Anforderungen systematisch validieren

**Zentrale Prüfungsanforderung:**

Das gesamte System muss auf einer laufenden Docker Engine mit folgendem Befehl vollständig und funktionsfähig gestartet werden können:

```bash
docker compose up
```

**Meilenstein:** Die vollständige Anwendung startet reproduzierbar und sämtliche Pflichtfunktionen sind getestet.

---

### Phase 7 – Evaluation des Multi-Agent-Systems

**Status:** Offen  
**Geschätzter Aufwand:** 3–5 Tage

**Aufgaben:**

- [ ] Tokenverbrauch und Modellkosten dokumentieren
- [ ] Ausführungszeiten erfassen
- [ ] Erfolgreiche und fehlgeschlagene Delegationen auswerten
- [ ] Automatische Korrekturschleifen untersuchen
- [ ] Manuelle Eingriffe dokumentieren
- [ ] Erfolgsquote abgeschlossener Entwicklungsaufgaben bestimmen
- [ ] Wiederverwendung eigener Skills analysieren
- [ ] Erkenntnisse über die Multi-Agent-Orchestrierung zusammenfassen

**Ziel:**

Untersuchen, in welchem Umfang die hierarchische Multi-Agent-Architektur die Entwicklung unterstützen und eigenständig Aufgaben übernehmen kann.

Diese Evaluation ist ein persönliches Lernziel und keine zusätzliche Prüfungsanforderung.

**Meilenstein:** Nachvollziehbare Auswertung des Agenten-Entwicklungsworkflows.

---

### Phase 8 – Dokumentation und Prüfungsabgabe

**Status:** Offen  
**Geschätzter Aufwand:** 3–5 Tage

**Aufgaben:**

- [ ] Architekturdiagramm und Dokumentation finalisieren
- [ ] Architekturvorlagen aus Relax berücksichtigen
- [ ] Dokumentation und Diagramm als PDF bereitstellen
- [ ] Quellcode und Docker-Compose-Datei zusammenstellen
- [ ] Nicht benötigte Dateien und `node_modules` ausschließen
- [ ] README mit Startanleitung überprüfen
- [ ] Vollständige ZIP-Datei erstellen
- [ ] ZIP-Abgabe aus einem sauberen Ausgangszustand testen
- [ ] Ergebnisse fristgerecht einreichen

**Meilenstein:** Vollständiges und erfolgreich geprüftes Abgabepaket.

---

## 3. Geplante Skills

Die folgenden Skills sollen schrittweise entwickelt beziehungsweise auf Grundlage vorhandener Hermes-Skills erweitert werden.

| Skill | Aufgabe | Priorität |
|---|---|---|
| `codex-delegation` | Standardisierte Aufgabenübergabe, Ergebnisprüfung und Fehlerbehandlung | Sehr hoch |
| `api-contract-validator` | OpenAPI-Spezifikationen und Schnittstellenkompatibilität prüfen | Sehr hoch |
| `requirements-validator` | Implementierung gegen die Prüfungsanforderungen kontrollieren | Hoch |
| `docker-compose-validator` | Containerstart, Erreichbarkeit und Funktionsfähigkeit prüfen | Hoch |

Bei Bedarf können weitere Skills wie `architecture-review` oder `test-generation` ergänzt werden.

Skills sollen wiederverwendbare Vorgehensweisen bereitstellen und nach Möglichkeit reproduzierbare Prüfskripte enthalten.

---

## 4. Regeln für das Multi-Agent-System

| Bereich | Regel |
|---|---|
| Orchestrierung | Hermes Main trägt die Gesamtverantwortung |
| Implementierung | Coding-Subagents dürfen Codex beauftragen |
| Parallelität | Anfangs maximal zwei Hermes-Subagents und zwei Codex-Prozesse |
| Verantwortlichkeiten | Jeder Coding-Agent arbeitet an einem abgegrenzten Service |
| Code-Isolation | Parallele Schreibarbeiten erfolgen in getrennten Git-Worktrees |
| API-Verträge | Änderungen an freigegebenen Schnittstellen benötigen Zustimmung |
| Qualität | Entwicklungsaufgaben werden erst nach erfolgreicher Validierung abgeschlossen |
| Fehlerbehandlung | Nach maximal drei erfolglosen Korrekturschleifen erfolgt eine Eskalation |
| Skills | Neue oder geänderte Skills müssen vor Aktivierung überprüft werden |
| Sicherheit | Keine unkontrollierten Löschaktionen oder sicherheitskritischen Operationen |

Hermes soll eigenständig koordinieren können, während sämtliche Änderungen und Entscheidungen nachvollziehbar bleiben.

---

## 5. Projektdokumentation

Die Dokumentation wird auf mehrere Dateien verteilt, um Verantwortlichkeiten klar zu trennen.

| Datei | Zweck |
|---|---|
| `AGENTS.md` | Regeln für Hermes, Codex und die Subagents |
| `docs/REQUIREMENTS.md` | Offizielle Prüfungsanforderungen |
| `docs/PROJECT_CONTEXT.md` | Projektspezifische Architektur und Entscheidungen |
| `docs/ARCHITECTURE.md` | Technische Architektur und Zusammenhänge |
| `docs/ROADMAP.md` | Projektphasen, Meilensteine und Gesamtfortschritt |
| `docs/FILE_OVERVIEW.md` | Übersicht der Projektdateien |
| `TASKS.md` | Konkrete Entwicklungsaufgaben und deren Bearbeitungsstatus |

Weitere Dokumente, insbesondere OpenAPI-Spezifikationen und Ergebnisse der Agenten-Evaluation, werden bei Bedarf ergänzt.

---

## 6. Erfolgskriterien

### 6.1 Prüfungsleistung

- [ ] Alle Pflichtfunktionen des Sideboard-Manufacturer-Themas umgesetzt
- [ ] Fachlich getrennte und funktionsfähige Webservices
- [ ] Vollständiger Systemstart über `docker compose up`
- [ ] Architekturdiagramm und dokumentierte Architekturentscheidungen
- [ ] Vollständige und getestete ZIP-Abgabe

### 6.2 Multi-Agent-Experiment

- [x] Hermes delegiert Aufgaben direkt an Codex
- [x] Hermes-Subagents können Codex eigenständig beauftragen
- [ ] Parallele Agentenentwicklung mit isolierten Arbeitsbereichen
- [ ] Mindestens zwei eigene Skills erfolgreich entwickelt und getestet
- [ ] Automatisierter Implementierungs-, Test- und Review-Workflow
- [ ] Tokenverbrauch, Laufzeiten und manuelle Eingriffe dokumentiert

---

## 7. Gesamtstatus

| Phase | Bezeichnung | Status |
|---|---|---|
| 1 | Anforderungen und Themenwahl | Abgeschlossen |
| 2 | Lokale Agentenumgebung | Abgeschlossen |
| 3 | Microservice-Architektur | Nächste Phase |
| 4 | Skills und Subagent-Orchestrierung | Offen |
| 5 | Implementierung der Webservices | Offen |
| 6 | Gesamtsystem und Qualitätssicherung | Offen |
| 7 | Evaluation des Multi-Agent-Systems | Offen |
| 8 | Dokumentation und Prüfungsabgabe | Offen |

**Aktuelle Phase: Phase 3 – Microservice-Architektur**

---

## 8. Vorgehensweise

Die Entwicklung erfolgt schrittweise.

1. Projektumfang und Anforderungen festlegen.
2. Hermes und Codex integrieren.
3. Microservice-Architektur und API-Verträge definieren.
4. Einen ersten Service vollständig durch die Agenten entwickeln lassen.
5. Skills und Subagent-Orchestrierung erweitern.
6. Weitere Services implementieren und integrieren.
7. Gesamtsystem validieren und Agenten-Workflow evaluieren.
8. Prüfungsabgabe vorbereiten.

Die Phasen müssen nicht vollständig sequenziell bearbeitet werden. Insbesondere Architekturentscheidungen, Dokumentation und Agenten-Evaluation sollen während der Entwicklung fortlaufend aktualisiert werden.

**Grundsatz:** Die Erfüllung der Prüfungsanforderungen hat stets Vorrang vor der Erweiterung des Multi-Agent-Systems.
