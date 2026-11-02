# Einzelprojektarbeit: Cloud-based Web Application Development

## Grundlage und Geltungsbereich

Dieses Dokument fasst die Anforderungen an die Einzelprojektarbeit aus der Vorlesungsunterlage **„Chapter 0 - Organisation und Prüfungsleistung“** von **Prof. Dr. Uwe Breitenbücher** ausführlich zusammen. Es dient als Arbeitsgrundlage für die Themenwahl, die Konzeption, die Implementierung und die Vorbereitung der Abgabe.

Maßgeblich sind die Aussagen zur Einzelprojektarbeit auf den PDF-Seiten 14 bis 19 sowie die Projektarbeitsthemen auf den Seiten 20 bis 25. Die Einordnung der Prüfungsleistung stammt von Seite 7. Die Seitenangaben beziehen sich auf die Position der Seiten innerhalb der PDF-Datei.

**Die Abschnitte 1 bis 7 geben die Vorgaben der PDF in eigenen Worten wieder. Abschnitt 8 enthält ergänzende Umsetzungsempfehlungen und ist keine zusätzliche Prüfungsordnung.** Die Checkliste in Abschnitt 9 führt die Vorgaben zur praktischen Kontrolle zusammen.

> **Achtung: Die Abgabefrist ist klärungsbedürftig.** Auf PDF-Seite 19 wird für die Einzelprojektarbeit der **12.06.2025 EOB** genannt. Für die Gruppenprojektarbeit steht auf Seite 13 dagegen der **12.06.2026 EOB**. Diese unterschiedlichen Jahresangaben werden hier unverändert dokumentiert. Aus der PDF lässt sich keine verlässlich gültige Frist für die vorliegende Einzelprojektarbeit ableiten. Der tatsächliche Abgabetermin muss anhand aktueller Kursinformationen oder mit dem Dozenten geklärt werden.

## 1. Ziel und Rahmen der Einzelprojektarbeit

Im Rahmen der Einzelprojektarbeit entwickelt eine einzelne studierende Person eine **Cloud-Native-Web-Anwendung** zu einem der vorgegebenen Projektarbeitsthemen. Die Arbeit umfasst sowohl die Konzeption der Systemarchitektur als auch die Umsetzung eines funktionsfähigen Prototyps. Architektur und Implementierung sollen inhaltlich zusammenpassen und auf den in der Vorlesung behandelten Grundlagen aufbauen.

Die Prüfungsleistung des Moduls besteht aus einer Gruppenprojektarbeit und einer Einzelprojektarbeit. Beide Teile zählen jeweils **50 Prozent der Gesamtnote**. In der Einzelprojektarbeit sind **maximal 50 Punkte** erreichbar. Eine weitergehende Aufteilung dieser Punkte auf einzelne Funktionen oder Qualitätsmerkmale enthält die PDF nicht.

Die Einzelprojektarbeit wird **allein** bearbeitet. Gleichzeitig erlaubt die Aufgabenstellung ausdrücklich, Ergebnisse der Gruppenprojektarbeit wiederzuverwenden. Auch die direkte Übernahme durch Copy-and-paste ist laut PDF zulässig. Diese Erlaubnis ändert jedoch nichts daran, dass für die Einzelprojektarbeit ein anderes Projektarbeitsthema gewählt werden muss.

**Quellen:** PDF-Seiten 7 und 15.

## 2. Themenwahl und Umfang

Das Thema kann aus den fünf in der PDF vorgestellten Projektarbeitsthemen frei ausgewählt werden:

| Projektarbeitsthema | Fachlicher Schwerpunkt |
| --- | --- |
| Car Manufacturer | Fahrzeugkonfiguration und Bestellung bei einem fiktiven Automobilhersteller |
| Wellness Resort | Zusammenstellung und Buchung von Wellness-Angeboten |
| Fashion Design Studio | Individuelle Konfiguration und Bestellung von Modeartikeln |
| Sideboard Manufacturer | Individuelle Konfiguration und Bestellung von Sideboards |
| Fruit Drink Company | Zusammenstellung und Bestellung von Fruchtgetränken |

**Das Thema der Einzelprojektarbeit darf nicht mit dem Thema der eigenen Gruppenprojektarbeit übereinstimmen.** Entscheidend ist damit die Wahl eines anderen Projektarbeitsthemas aus der Liste; die Wiederverwendung technischer Ergebnisse bleibt ausdrücklich erlaubt.

Für die Einzelprojektarbeit darf das in den Themenbeschreibungen enthaltene **AI-Feature vollständig weggelassen werden**. Die Ausnahme bezieht sich auf dieses Feature. Für die weiteren beschriebenen Funktionen nennt die PDF keine entsprechende allgemeine Befreiung.

Wird das AI-Feature umgesetzt, beschreiben die Themenfolien dafür ein selbst ausgedachtes, kreatives Feature mit **Google Gemini**. Die ausdrückliche Erlaubnis zum Weglassen bei der Einzelprojektarbeit ist dabei zu berücksichtigen.

Da für dieses Dokument noch kein konkretes Thema festgelegt wurde, sind in Abschnitt 5 alle fünf Themen beschrieben. Für die eigentliche Umsetzung ist das ausgewählte Thema maßgeblich.

**Quellen:** PDF-Seite 15 sowie Seiten 21 bis 25.

## 3. Zu entwickelnde Ergebnisse

Für die Einzelprojektarbeit sind zwei zentrale Ergebnisse zu erstellen: eine **Architekturbeschreibung** und ein **Prototyp**.

### 3.1 Architekturbeschreibung

Die Architekturbeschreibung besteht aus einem Architekturdiagramm für das konzipierte System und einer Dokumentation der wichtigsten Architekturentscheidungen. Das Diagramm stellt die geplante Systemarchitektur dar; die schriftliche Dokumentation erläutert die wesentlichen Entscheidungen, auf denen diese Architektur beruht.

Für beide Bestandteile sind Vorlagen vorgegeben, die laut PDF in **Relax** verfügbar sind:

- `Architekturdokumentation_Template.docx`
- `Architekturmodellierung_Template.pptx`

Die Architekturbeschreibung soll auf den **Architekturstilen, Architekturmustern und Prinzipien der Vorlesung** aufbauen. Die konkrete Ausarbeitung muss sich daher an den behandelten Vorlesungsinhalten und den bereitgestellten Vorlagen orientieren. Die PDF nennt in diesem Kapitel keine zusätzliche feste Gliederung oder einen verbindlichen Seitenumfang.

Für die Abgabe ist die Architekturbeschreibung als **PDF** bereitzustellen. Das vorliegende Markdown-Dokument dient der Aufgabenklärung und ersetzt diese abzugebende Architekturbeschreibung nicht.

### 3.2 Funktionsfähiger Prototyp

Der Prototyp setzt die Web-Anwendung für das gewählte Thema um. Er soll auf den Technologien der Vorlesung basieren und die zum Thema beschriebenen Funktionen abbilden. Die besondere Ausnahme ist das bei der Einzelprojektarbeit optionale AI-Feature.

Die Implementierung muss so vorbereitet werden, dass das gesamte System lokal auf einer laufenden Docker Engine mit einem einzigen Compose-Aufruf funktionsfähig gestartet werden kann. Die dafür erforderliche Docker-Compose-Datei gehört zum Prototyp und muss Bestandteil der Abgabe sein.

**Quellen:** PDF-Seiten 16 bis 19.

## 4. Technologische Grundlage

Die PDF nennt folgende Technologien als Grundlage für die Umsetzung:

| Bereich | In der PDF genannte Technologien |
| --- | --- |
| Frontend | HTML, CSS und JavaScript |
| Backend und zugehörige Infrastruktur | NodeJS, MySQL, MinIO, Redis, Docker und Docker Compose |

Damit soll die Anwendung auf der technologischen Basis der Vorlesung entstehen. Die Aufgabenfolie führt die genannten Technologien auf, legt in diesem Kapitel aber keine detaillierte Aufgabenverteilung zwischen den einzelnen Diensten fest. Diese Zuordnung ist im eigenen Architekturentwurf vorzunehmen und zu begründen.

Der Einsatz weiterer Technologien ist ausdrücklich zulässig. Voraussetzung ist, dass die abgegebene Anwendung weiterhin vollständig über folgenden Befehl gestartet werden kann:

```bash
docker compose up
```

Die Erweiterung des Technologieumfangs hebt diese Startanforderung nicht auf. Auch zusätzliche Komponenten müssen in den automatisierten Start des Gesamtsystems eingebunden werden, soweit sie für dessen Funktionsfähigkeit erforderlich sind.

**Quellen:** PDF-Seiten 16 und 18.

## 5. Projektarbeitsthemen und funktionale Anforderungen

### 5.1 Car Manufacturer

Bei diesem Thema wird eine Cloud-Native-Web-Anwendung für einen **fiktiven Automobilhersteller** entwickelt.

**Fahrzeugkonfigurator mit Bestellfunktion:** Fahrzeuge sollen grafisch konfiguriert und anschließend bestellt werden können. Der Konfigurator soll optische Änderungen an Bauteilen sichtbar machen, beispielsweise bei der Auswahl anderer Reifen. Für die Bestellung genügt eine rudimentäre Seite, auf der Adressdaten eingegeben werden und der Kauf über eine Schaltfläche „Kaufen“ ausgelöst wird.

**Merchandise-Shop:** Zusätzlich soll ein Webshop vorhanden sein, über den Merchandise-Artikel mithilfe eines Warenkorbs gekauft werden können.

**Impressionen:** Die Anwendung soll Bilder einiger Fahrzeuge anzeigen. Außerdem sollen Videos einiger Fahrzeuge eingebunden werden, beispielsweise über YouTube.

**Road to the Super Car Presentation:** Als weitere Funktion soll ein Supercar auf einer Karte dargestellt werden, das zu einem Präsentationsort fährt. Die PDF fordert hierfür eine einfache Darstellung und nennt keine weitergehenden Anforderungen an Navigation oder reale Standortdaten.

**Optionales AI-Feature:** Für die Einzelprojektarbeit darf dieses Feature entfallen. Bei einer Umsetzung sieht die Themenbeschreibung ein selbst entwickeltes, kreatives Feature mit Google Gemini vor.

**Quelle:** PDF-Seite 21; Ausnahme zum AI-Feature auf Seite 15.

### 5.2 Wellness Resort

Bei diesem Thema wird eine Cloud-Native-Web-Anwendung für ein **fiktives Wellness-Resort** entwickelt.

**Wellness-Urlaub-Konfigurator mit Buchungsfunktion:** Wellness-Aufenthalte sollen grafisch zusammengestellt und gebucht werden können. Der Konfigurator soll verschiedene Wellness-Angebote darstellen und ihre Kombination ermöglichen. Der Abschluss darf rudimentär über eine Seite mit Adressdateneingabe und einer Schaltfläche „Kaufen“ erfolgen.

**Wellness-Artikel-Shop:** Ein zusätzlicher Webshop soll den Kauf von Wellness-Artikeln über einen Warenkorb ermöglichen.

**Impressionen:** Bilder einiger Wellness-Angebote sollen angezeigt und Videos zu solchen Angeboten eingebunden werden. YouTube wird als mögliches Beispiel für die Videoeinbindung genannt.

**Anzeige des aktuellen Wetters:** Die Anwendung soll Wetterinformationen anzeigen. Die Daten dürfen erfunden sein, sollen sich dann aber von Zeit zu Zeit ändern. Alternativ können echte Wetterdaten verwendet werden. Eine bestimmte Wetter-API oder ein konkretes Aktualisierungsintervall schreibt die Themenfolie nicht vor.

**Optionales AI-Feature:** Für die Einzelprojektarbeit darf dieses Feature entfallen. Bei einer Umsetzung sieht die Themenbeschreibung ein selbst entwickeltes, kreatives Feature mit Google Gemini vor.

**Quelle:** PDF-Seite 22; Ausnahme zum AI-Feature auf Seite 15.

### 5.3 Fashion Design Studio

Bei diesem Thema wird eine Cloud-Native-Web-Anwendung für ein **fiktives Fashion Design Studio** entwickelt.

**Modekonfigurator mit Bestellfunktion:** Ein Modeartikel, beispielsweise ein Pullover, soll grafisch individuell konfiguriert und bestellt werden können. Unterschiedliche Varianten sollen dargestellt und miteinander kombiniert werden können. Für den Bestellabschluss genügt die beschriebene einfache Seite mit Adressdaten und einer Schaltfläche „Kaufen“.

**Pflegemittel-Shop:** Über einen Webshop mit Warenkorb sollen Pflegemittel für Kleidungsstücke gekauft werden können.

**Impressionen:** Die Anwendung soll Bilder einiger von Kunden erstellter Modeartikel anzeigen. Außerdem sollen Videos von Herstellungsprozessen eingebunden werden, beispielsweise über YouTube.

**Community-Feature:** Modeentwürfe anderer Nutzer sollen angezeigt werden. Weitere Community-Funktionen wie Kommentare, Bewertungen oder Nachrichten werden auf der Themenfolie nicht gefordert.

**Optionales AI-Feature:** Für die Einzelprojektarbeit darf dieses Feature entfallen. Bei einer Umsetzung sieht die Themenbeschreibung ein selbst entwickeltes, kreatives Feature mit Google Gemini vor.

**Quelle:** PDF-Seite 23; Ausnahme zum AI-Feature auf Seite 15.

### 5.4 Sideboard Manufacturer

Bei diesem Thema wird eine Cloud-Native-Web-Anwendung für einen **fiktiven Sideboard-Hersteller** entwickelt.

**Sideboard-Konfigurator mit Bestellfunktion:** Sideboards sollen grafisch individuell konfiguriert und anschließend bestellt werden können. Dabei sollen unterschiedliche Größen, Farben und weitere Varianten dargestellt und kombiniert werden können. Die Bestellung darf rudimentär über die Eingabe von Adressdaten und eine Schaltfläche „Kaufen“ abgeschlossen werden.

**Zubehör-Shop:** Ein Webshop mit Warenkorb soll den Kauf von Zubehörartikeln ermöglichen. Als Beispiel nennt die PDF Schrauben.

**Impressionen:** Bilder einiger von Kunden erstellter Sideboards sollen angezeigt werden. Videos von Herstellungsprozessen sollen ebenfalls eingebunden werden, beispielsweise über YouTube.

**Community-Feature:** Die Anwendung soll Sideboard-Entwürfe anderer Nutzer anzeigen. Die Themenfolie spezifiziert darüber hinaus keine weiteren Interaktionsmöglichkeiten.

**Optionales AI-Feature:** Für die Einzelprojektarbeit darf dieses Feature entfallen. Bei einer Umsetzung sieht die Themenbeschreibung ein selbst entwickeltes, kreatives Feature mit Google Gemini vor.

**Quelle:** PDF-Seite 24; Ausnahme zum AI-Feature auf Seite 15.

### 5.5 Fruit Drink Company

Bei diesem Thema wird eine Cloud-Native-Web-Anwendung für eine **fiktive Fruit Drink Company** entwickelt.

**Fruit-Drink-Konfigurator mit Bestellfunktion:** Fruchtgetränke sollen grafisch aus mehreren Früchten zusammengestellt und bestellt werden können. Der Konfigurator soll verschiedene Früchte darstellen und ihre Kombination ermöglichen. Für die Bestellung genügt ein einfacher Ablauf mit Adressdateneingabe und einer Schaltfläche „Kaufen“.

**Küchenartikel-Shop:** Ein Webshop mit Warenkorb soll den Kauf von Küchenartikeln ermöglichen. Als Beispiel werden Gläser genannt.

**Impressionen:** Die Anwendung soll Bilder einiger von Kunden erstellter Fruchtgetränke anzeigen. Zusätzlich sollen Videos von Herstellungsprozessen eingebunden werden, beispielsweise über YouTube.

**Community-Feature:** Konfigurationen von Fruchtgetränken anderer Nutzer sollen angezeigt werden. Zusätzliche soziale Funktionen werden auf der Themenfolie nicht beschrieben.

**Optionales AI-Feature:** Für die Einzelprojektarbeit darf dieses Feature entfallen. Bei einer Umsetzung sieht die Themenbeschreibung ein selbst entwickeltes, kreatives Feature mit Google Gemini vor.

**Quelle:** PDF-Seite 25; Ausnahme zum AI-Feature auf Seite 15.

## 6. Automatisierter Start mit Docker Compose

Eine zentrale technische Anforderung ist der **vollautomatisierte Start des gesamten Systems**. Auf einer bereits laufenden lokalen Docker Engine muss der folgende Befehl ausreichen, um den Prototyp funktionsfähig hochzufahren:

```bash
docker compose up
```

Die Abgabe muss die dafür benötigte Docker-Compose-Datei sowie alle erforderlichen Dateien des Prototyps enthalten. Maßgeblich ist die Funktionsfähigkeit des Gesamtsystems. Das bloße Starten einzelner Container erfüllt die beschriebene Anforderung noch nicht, wenn die Anwendung anschließend nicht funktioniert.

Die PDF weist ausdrücklich darauf hin, dass ein Prototyp, der nicht in dieser Form gestartet werden kann, zu einem **signifikanten Punktabzug** führt. Der automatisierte Start sollte deshalb bei der Umsetzung und vor der Abgabe besonders sorgfältig überprüft werden.

Die lokale Startvorgabe ist ausdrücklich formuliert. Eine zusätzliche Verpflichtung zur Bereitstellung bei einem öffentlichen Cloud-Anbieter wird im Abschnitt zur Einzelprojektarbeit nicht genannt.

**Quellen:** PDF-Seiten 18 und 19.

## 7. Abgabe und Präsentation

### 7.1 Abzugebende Bestandteile

Die Ergebnisse werden in einer **einzelnen ZIP-Datei** abgegeben. Diese muss folgende Bestandteile enthalten:

1. Die **Architekturbeschreibung als PDF**, einschließlich des Architekturdiagramms und der Dokumentation der wichtigsten Entscheidungen.
2. **Alle Dateien des Prototyps**, einschließlich der Docker-Compose-Datei für den vollständigen automatisierten Systemstart.

Die ZIP-Datei soll **keine `node_modules`-Verzeichnisse von NodeJS/NPM** enthalten, damit die Dateigröße klein bleibt. Die für den Systemstart notwendigen Abhängigkeiten müssen entsprechend im vorgesehenen Build- und Startablauf berücksichtigt werden.

Ein zusätzliches Statement-of-Work-Dokument wird auf der Abgabefolie der Einzelprojektarbeit nicht als Bestandteil genannt. Die entsprechende Anforderung auf Seite 13 bezieht sich auf die Gruppenprojektarbeit.

### 7.2 Abgabeweg

Die Abgabe erfolgt **per E-Mail an Prof. Breitenbücher**. Die PDF erlaubt ausdrücklich, die einzelne ZIP-Datei über einen **Download-Link** bereitzustellen. Eine konkrete E-Mail-Adresse wird auf der betreffenden Folie nicht angegeben.

### 7.3 Abgabefrist

Auf der Folie zur Einzelprojektarbeit steht **12.06.2025 EOB**. Die Abkürzung EOB steht üblicherweise für „End of Business“; eine konkrete Uhrzeit legt die Folie nicht fest.

Wegen der abweichenden Jahreszahl **2026** auf der Folie zur Gruppenprojektarbeit ist diese Datumsangabe klärungsbedürftig. Weder die Jahreszahl noch eine genaue Uhrzeit sollten ohne weitere Bestätigung als verbindliche Frist übernommen werden.

### 7.4 Präsentation

Für die Einzelprojektarbeit ist laut PDF **keine Präsentation der Ergebnisse vorgesehen**. Die Präsentations- und Interviewangaben aus dem Abschnitt zur Gruppenprojektarbeit gehören daher nicht zu den beschriebenen Anforderungen an die Einzelprojektarbeit.

**Quelle:** PDF-Seite 19; Vergleich mit den Gruppenanforderungen auf Seite 13.

## 8. Ergänzende Empfehlungen für die Umsetzung

**Die folgenden Hinweise sind praktische Empfehlungen. Sie sind keine zusätzlichen, in Chapter 0 festgelegten Prüfungsanforderungen.**

### 8.1 Thema und Funktionsumfang festhalten

Zu Beginn empfiehlt es sich, das Thema der Gruppenarbeit und das davon abweichende Thema der Einzelarbeit schriftlich festzuhalten. Anschließend kann aus Abschnitt 5 eine konkrete Funktionsliste für das ausgewählte Thema abgeleitet werden. Dabei sollte auch dokumentiert werden, ob das optionale AI-Feature umgesetzt oder weggelassen wird.

### 8.2 Architektur und Implementierung aufeinander abstimmen

Das Architekturdiagramm sollte die tatsächlich implementierten Komponenten und ihre Beziehungen nachvollziehbar darstellen. Für die Dokumentation bietet es sich an, die Verantwortlichkeiten der Komponenten, die Kommunikationswege und den Einsatz der gewählten Technologien zu erläutern. Die vorgegebenen Relax-Vorlagen bleiben dabei die maßgebliche Orientierung für den Aufbau.

Beispielsweise können MySQL für relationale Anwendungsdaten, MinIO für Objektdateien und Redis für geeignete temporäre Daten oder Caching vorgesehen werden. Diese Zuordnung ist ein möglicher Architekturansatz und keine in Chapter 0 festgelegte Aufteilung.

### 8.3 Den ersten Start reproduzierbar gestalten

Der Start sollte aus einem frisch entpackten Abgabeverzeichnis überprüft werden. Dabei ist besonders hilfreich zu kontrollieren, ob Container-Images gebaut oder geladen werden, Abhängigkeiten installiert werden und benötigte Datenstrukturen sowie gegebenenfalls Beispieldaten automatisch verfügbar werden. Auch die Bereitschaft abhängiger Dienste sollte im Startablauf berücksichtigt werden.

Für die Überprüfung empfiehlt sich ein Zustand ohne bereits manuell vorbereitete Projektdaten. So lässt sich erkennen, ob der Prototyp unbemerkt von lokalen Dateien, bereits vorhandenen Datenbankeinträgen oder früheren Einrichtungsschritten abhängt.

### 8.4 Eine kurze Startanleitung beilegen

Eine ergänzende `README.md` kann beschreiben, in welchem Verzeichnis `docker compose up` ausgeführt wird, unter welcher lokalen Adresse die Anwendung erreichbar ist und ob externe Dienste verwendet werden. Eine solche Anleitung erleichtert die Prüfung, ersetzt aber nicht den geforderten automatisierten Start.

### 8.5 Die zentralen Benutzerabläufe prüfen

Vor der Abgabe empfiehlt es sich, den Konfigurator, den Bestell- beziehungsweise Buchungsabschluss, den Shop mit Warenkorb, die Bild- und Videoansichten sowie das themenspezifische Zusatzfeature vollständig durchzugehen. Beim Wellness-Thema betrifft das beispielsweise die wechselnden Wetterdaten, bei den Community-Themen die Anzeige fremder Entwürfe und beim Automobilthema die Kartendarstellung.

Die Funktionsprüfung sollte nach Möglichkeit mit dem Stand erfolgen, der tatsächlich in die ZIP-Datei aufgenommen wird. Außerdem lohnt sich ein Abgleich zwischen Architekturbeschreibung und Implementierung, damit beide denselben Systemstand beschreiben.

## 9. Checkliste der Vorgaben aus der PDF

### Rahmen und Themenwahl

- [ ] Die Einzelprojektarbeit wird von einer Person bearbeitet.
- [ ] Eines der fünf vorgegebenen Projektarbeitsthemen wurde ausgewählt.
- [ ] Das gewählte Thema unterscheidet sich vom Thema der eigenen Gruppenprojektarbeit.
- [ ] Der Funktionsumfang des ausgewählten Themas ist berücksichtigt; das AI-Feature darf entfallen.
- [ ] Falls das beschriebene AI-Feature umgesetzt wird, wird Google Gemini verwendet.

### Architektur und Prototyp

- [ ] Ein Architekturdiagramm wurde erstellt.
- [ ] Die wichtigsten Architekturentscheidungen wurden dokumentiert.
- [ ] Die vorgegebenen Vorlagen aus Relax wurden berücksichtigt.
- [ ] Die Architekturbeschreibung baut auf den Architekturstilen, Architekturmustern und Prinzipien der Vorlesung auf.
- [ ] Der Prototyp basiert auf der in der PDF genannten Technologiebasis.
- [ ] Die zum gewählten Thema beschriebenen Funktionen sind umgesetzt; die Ausnahme für das AI-Feature ist berücksichtigt.
- [ ] Eine Docker-Compose-Datei ist vorhanden.
- [ ] Das gesamte System startet lokal auf einer laufenden Docker Engine mit `docker compose up` vollautomatisiert und funktionsfähig.

### Abgabepaket und Organisation

- [ ] Die Architekturbeschreibung liegt als PDF vor.
- [ ] Alle erforderlichen Dateien des Prototyps sind enthalten.
- [ ] Die Abgabe ist als einzelne ZIP-Datei zusammengestellt.
- [ ] Die ZIP-Datei enthält keine `node_modules`-Verzeichnisse.
- [ ] Die Abgabe erfolgt per E-Mail an Prof. Breitenbücher, gegebenenfalls mit einem Download-Link zur ZIP-Datei.
- [ ] Die tatsächlich gültige Abgabefrist wurde wegen der widersprüchlichen Jahresangaben geklärt.

## 10. Noch zu konkretisierende Projektangaben

Für die weitere Projektplanung sind insbesondere folgende Angaben offen:

| Angabe | Aktueller Stand |
| --- | --- |
| Thema der eigenen Gruppenprojektarbeit | Noch einzutragen |
| Gewähltes Thema der Einzelprojektarbeit | Noch auszuwählen; muss vom Gruppenthema abweichen |
| Umsetzung des optionalen AI-Features | Noch festzulegen |
| Verbindlicher Abgabetermin und gegebenenfalls genaue Uhrzeit | Wegen der widersprüchlichen Angaben zu klären |
| Zugriff auf die Relax-Vorlagen | Für die Erstellung der Architekturbeschreibung sicherzustellen |

## Quelle

- **Prof. Dr. Uwe Breitenbücher: [„Cloud-based Web Application Development - Chapter 0 - Organisation und Prüfungsleistung“](../Vorlesungsunterlagen/Chapter%200%20-%20Organisation%20und%20Pru%CC%88fungsleistung.pdf)**.
- **PDF-Seite 7:** Zusammensetzung und Gewichtung der Prüfungsleistung.
- **PDF-Seiten 14 bis 19:** Rahmen, Ergebnisse, Technologien und Abgabe der Einzelprojektarbeit.
- **PDF-Seiten 20 bis 25:** Vorgestellte Projektarbeitsthemen und ihre Funktionen.
- **PDF-Seite 13:** Vergleichsstelle für die abweichende Jahresangabe und die ausschließlich dort beschriebenen Gruppenabgabeanforderungen.
