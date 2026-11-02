---
name: lecture-analysis
description: Analysiert PDF-Vorlesungsunterlagen mithilfe von Hermes-Subagents. Extrahiert projektrelevante Anforderungen, Architekturprinzipien und technische Konzepte unter Berücksichtigung der REQUIREMENTS.md. Erstellt kapitelbezogene Markdown-Analysen und eine konsolidierte Wissensbasis mit Quellenangaben.
---

# Lecture Analysis

## Ziel

Analysiere die Vorlesungsunterlagen des Moduls
*Cloud-based Web Application Development*.

Extrahiere alle Inhalte, die für die Architektur,
Implementierung und Qualitätssicherung der
Cloud-Native Sideboard-Webanwendung relevant sind.

Erstelle eine nachvollziehbare Wissensbasis,
die bei der weiteren Entwicklung verwendet werden kann.

## 1. Projektkontext

Lies vor Beginn:

- `docs/REQUIREMENTS.md`
- `docs/PROJECT_CONTEXT.md`, sofern vorhanden

Berücksichtige insbesondere:

- Projektthema: Sideboard Manufacturer
- Geforderte Anwendungsfunktionen
- Verbindliche serviceorientierte Architektur
- Technologien und Prinzipien der Vorlesung
- Automatisierten Start über Docker Compose

Die REQUIREMENTS.md ist die maßgebliche
Anforderungsgrundlage.

## 2. Quellen

Verwende ausschließlich:

- `docs/REQUIREMENTS.md`
- `docs/PROJECT_CONTEXT.md`
- PDFs aus `Vorlesungsunterlagen/`

Keine externe Internetrecherche.

Erfinde keine Anforderungen oder Quellen.

Unterscheide zwischen:

1. Verbindlichen Anforderungen
2. Architekturprinzipien
3. Relevanten technischen Konzepten
4. Optionalen Empfehlungen

Die Erwähnung einer Technologie in der Vorlesung
macht ihren Einsatz nicht automatisch verpflichtend.

## 3. Vorbereitung

1. Ermittle alle PDFs unter `Vorlesungsunterlagen/`.
2. Sortiere sie nach Kapitelnummer.
3. Prüfe auf fehlende oder doppelte Kapitel.
4. Ermittle die Anzahl der benötigten Subagents.
5. Lege `docs/lecture-analysis/` als Ausgabeordner fest.

Verändere keine Original-PDFs oder Projektanforderungen.

## 4. Subagent-Delegation

Verwende `delegate_task`.

Regeln:

- Ein Subagent pro PDF-Kapitel.
- Maximal drei Subagents gleichzeitig.
- Jedes Kapitel wird vollständig analysiert.
- Jeder Subagent bearbeitet nur sein Kapitel.
- Keine verschachtelte Delegation.
- Keine Verwendung der Codex CLI.
- Nach jedem Batch die Ergebnisse überprüfen.

Übermittle jedem Subagenten:

- PDF-Pfad und Kapitelnummer
- Projektkontext und Anforderungen
- Erwarteten Ausgabepfad
- Analyseauftrag
- Ausgabevorlage
- Regeln für Quellenangaben

## 5. Kapitelanalyse

Jeder Subagent muss:

1. Sein PDF vollständig untersuchen.
2. Auch Diagramme, Tabellen und Codebeispiele berücksichtigen.
3. Inhalte mit den Projektanforderungen vergleichen.
4. Projektrelevante Erkenntnisse extrahieren.
5. Anforderungen und Empfehlungen klar unterscheiden.
6. Konkrete Auswirkungen auf das Sideboard-Projekt erläutern.
7. Jede wesentliche Aussage mit einer PDF-Seitenangabe belegen.
8. Unsichere Aussagen ausdrücklich kennzeichnen.

Quellenformat:

`Chapter X, PDF-Seite Y`

Verwende die tatsächliche Seitenposition innerhalb
der PDF-Datei.

## 6. Kapitelergebnisse

Erstelle pro Kapitel:

`docs/lecture-analysis/chapter-XX.md`

Lies vor der Erstellung die Vorlage:

`references/OUTPUT_TEMPLATE.md`

Die Vorlage definiert die verbindliche
Struktur der Kapitelanalysen.

## 7. Validierung

Nach Abschluss aller Subagents:

1. Prüfe, ob alle Kapitel analysiert wurden.
2. Kontrolliere die Vollständigkeit der Ergebnisdateien.
3. Überprüfe kritische Aussagen anhand der Original-PDFs.
4. Identifiziere Widersprüche und Doppelungen.
5. Kontrolliere die Trennung von Vorgaben und Empfehlungen.
6. Delegiere bei Bedarf gezielte Nachbesserungen.

Übernimm keine unbelegten Behauptungen.

## 8. Konsolidierung

Erstelle:

`docs/LECTURE_GUIDELINES.md`

Führe die validierten Erkenntnisse zusammen.

Strukturiere die Wissensbasis nach:

- Verbindlichen Anforderungen
- Architekturprinzipien
- Frontend
- Backend und Webservices
- Datenhaltung
- Docker und Deployment
- Testing und Qualitätssicherung
- Konsequenzen für die Sideboard-Architektur
- Offenen Fragen und Widersprüchen

Vermeide unnötige Wiederholungen.

Erhalte Quellenangaben und Verweise
auf die jeweiligen Kapitelanalysen.

## 9. Abschluss

Erstelle einen Abschlussbericht mit:

- Analysierten Kapiteln
- Erstellten Dateien
- Wichtigsten Erkenntnissen
- Identifizierten Widersprüchen
- Fehlenden oder unsicheren Informationen

Keine Änderungen an bestehenden Anforderungen,
keine Git-Commits und keine Pushes ohne Freigabe.
