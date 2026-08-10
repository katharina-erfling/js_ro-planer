# 📝 RO Planer -- Changelog

Alle wichtigen Änderungen und Entwicklungsschritte von **RO Planer**.

> RO Planer wird iterativ anhand der praktischen Nutzung
> weiterentwickelt.  
> Der Changelog dokumentiert Funktionen, Verbesserungen und
> Fehlerbehebungen, ohne unnötige interne Implementierungsdetails offenzulegen.

------------------------------------------------------------------------
### v0.2.12

#### ✨ Neu

- Geräte-Sets bleiben nach dem Einfügen zunächst als zusammengehörige Gruppe erhalten.
- Beim Verschieben eines Geräts aus einer aktiven Gruppe wird das komplette Set gemeinsam verschoben.
- Die relativen Abstände und die ursprüngliche Anordnung der Geräte bleiben beim gemeinsamen Verschieben erhalten.
- Im Detailbereich steht für gruppierte Geräte die Aktion **„Aus Gruppe lösen“** zur Verfügung.
- Mit **„Gruppe auflösen“** kann die Gruppierung eines kompletten Sets aufgehoben werden.

#### 🔄 Verbessert

- Nach dem Lösen eines einzelnen Geräts bleibt der restliche Set-Aufbau weiterhin gruppiert.
- Besteht eine Gruppe nach Änderungen nur noch aus einem Gerät, wird die Gruppierung automatisch entfernt.
- Gelöste bzw. aufgelöste Geräte können anschließend wieder vollständig unabhängig voneinander verschoben werden.
- Gruppierte Geräte werden auf der Parcoursfläche dezent als zusammengehörig hervorgehoben, sobald ein Mitglied der Gruppe ausgewählt ist.

#### 🧠 Parcourslogik

- `groupId` wird nun aktiv für gemeinsames Verschieben und Auflösen von Geräte-Sets verwendet.
- Die Gruppierung beeinflusst weiterhin weder Stationsnummerierung noch Laufweg.
- Die Einzelobjekte eines Sets bleiben vollständig erhalten; Gruppierung ist lediglich eine zusätzliche Bearbeitungsebene.

### v0.2.11

#### ✨ Neu

- Ausgewählte Übungsstationen können jetzt mit **Entf/Delete** direkt von der Parcoursfläche gelöscht werden.
- Auch frei platzierte Geräte lassen sich mit **Entf/Delete** entfernen.
- Neuer Bereich **Geräte-Sets** für häufig benötigte PO-Aufbauten.
- Folgende Schnellaufbauten stehen zur Verfügung:
  - 2 Pylonen in einer Reihe mit 1,50 m Abstand
  - 3 Pylonen in einer Reihe mit je 1,50 m Abstand
  - 4 Pylonen in einer Reihe mit je 1,50 m Abstand
  - 4 leere Schalen als Raute
  - 4 Schalen mit Ablenkung als Raute
- Die Schalen-Raute wird mit 3 m Längsabstand und ca. 1,50 m Querabstand angelegt.

#### 🧠 Parcourslogik

- Geräte-Sets dienen als Schnellaufbau und erzeugen anschließend normale einzelne Geräteobjekte.
- Die automatisch gesetzten Geräte können nach dem Einfügen weiterhin einzeln verschoben und angepasst werden.
- Die Grundmaße der Pylonenreihen und Schalen-Rauten orientieren sich an den entsprechenden Aufbauangaben des VDH-Regelwerks 2027.
- Die Set-Struktur ist darauf vorbereitet, später weitere regelwerksbezogene Geräteanordnungen für bestimmte Übungen aufzunehmen.

#### ⌨️ Bedienung

- Die Delete-Taste reagiert nur auf eine aktuell ausgewählte Station bzw. ein ausgewähltes Gerät.
- Während der Eingabe in Text-, Zahlen- oder Auswahlfeldern wird die Delete-Taste nicht zum Löschen von Parcoursobjekten verwendet.

### v0.2.10

#### ✨ Neu

- **Schale mit Ablenkung** als frei platzierbares Parcoursobjekt ergänzt.
- **Schale ohne Ablenkung** als eigenes frei platzierbares Parcoursobjekt ergänzt.
- Beide Schalentypen können beliebig oft auf dem Parcours platziert und frei verschoben werden.
- Die beiden Varianten sind sowohl in der Gerätebibliothek als auch auf der Parcoursfläche optisch voneinander unterscheidbar.

#### 🎨 Design

- Ablenkungsschalen erhalten eine eigene kleine Illustration im Stil der bestehenden Pylonen- und Hürdenkarten.
- Die Schale mit Ablenkung zeigt dezent angedeuteten Inhalt.
- Die Schale ohne Ablenkung bleibt optisch leer.

#### 🧠 Parcourslogik

- Schalen werden wie Pylonen und Hürden als freie Parcoursobjekte behandelt.
- Sie erhalten keine Stationsnummer und verändern den automatischen Laufweg nicht.
- Die getrennten Gerätetypen **mit Ablenkung** und **ohne Ablenkung** können später von der regelbasierten Übungs- und Generatorlogik gezielt unterschieden werden.

### v0.2.9

#### ✨ Neu

- Neuer Bereich **Geräte** in der linken Bibliothek.
- Pylonen können beliebig oft frei auf der Parcoursfläche platziert und verschoben werden.
- Hürden können frei platziert, verschoben und gedreht werden.
- Geräte können im rechten Detailbereich ausgewählt und wieder entfernt werden.
- Frei platzierte Geräte werden gemeinsam mit dem Parcours gespeichert und wieder geladen.

#### 🎨 Design

- Pylonen und Hürden werden als kleine eigene Karten dargestellt, optisch angelehnt an die bestehende Schilderbibliothek.
- Auch auf der Parcoursfläche bleiben die Geräte bewusst schlicht und weich gestaltet, damit sie zu den pastelligen Bedienelementen passen.

#### 🧠 Parcourslogik

- Geräte sind vollständig von den Übungsstationen getrennt.
- Pylonen und Hürden erhalten keine Stationsnummer.
- Frei platzierte Geräte werden bei der Laufwegberechnung nicht als eigene Station berücksichtigt.
- Die Geräteebene ist für spätere Übungen vorbereitet, deren Aufbau bestimmte Pylonen-, Hürden- oder andere Geräteanordnungen voraussetzt.

#### ♻️ Kompatibilität

- Bereits gespeicherte Parcours aus älteren Versionen ohne Geräte-Daten können weiterhin geladen werden.

### v0.2.8

#### ✨ Neu

- Im rechten Detailbereich kann jetzt zwischen **Kurz erklärt** und **Regelwerk** gewechselt werden.
- **Kurz erklärt** zeigt die Übungsbeschreibung kompakt als Bullet Points.
- **Regelwerk** zeigt weiterhin die vollständige hinterlegte Regelwerkbeschreibung.
- Die zuletzt gewählte Textansicht wird lokal gespeichert und beim nächsten Schild beibehalten.

#### 🎨 Texte & Darstellung

- Der Footer wurde auf **„RO Planer · Rally Obedience Parcoursplanung“** geändert.
- Der RO Planer wird in Oberfläche und Projektdokumentation als eigenständiges Softwareprojekt dargestellt.

#### 🧩 Daten

- Für die Schilderdaten wurde ein eigener Bereich für kompakte Kurzfassungen ergänzt.
- Die Kurzfassungen bleiben getrennt von den offiziellen Regelwerktexten und den technischen Generator-Metadaten.

### v0.2.7

#### ✨ Neu

- Stationsnummern werden nun als kleine separate Mini-Schilder neben den eigentlichen Übungsschildern dargestellt.
- Der optionale Laufweg enthält dezente kleine Pfoten als zusätzliche Orientierung.
- Bei **automatischer Nummerierung** erhält ein neu platziertes Schild automatisch die Ausrichtung, die sich aus der Laufrichtung der vorherigen Station ergibt.

#### 🎨 Design

- Die runden Nummern-Badges wurden durch kleine rechteckige Nummernschilder mit angedeutetem Schildhalter ersetzt.
- Laufwege werden nun als gerade Verbindungen zwischen den Stationen dargestellt.
- Linien und Pfoten besitzen bewusst eine sehr geringe Deckkraft und bleiben optisch deutlich hinter den Übungsschildern.

#### 🧠 Parcourslogik

- Für die automatische Ausrichtung wird die Rotation der vorherigen Station mit der hinterlegten resultierenden Richtungsänderung der Übung kombiniert.
- Bei Übungen ohne hinterlegte Richtungsänderung bleibt die bisherige Laufrichtung erhalten.
- Die Rotation kann anschließend weiterhin manuell verändert werden; eine manuelle Änderung überschreibt die automatische Ausrichtung dieser Station.
- Offensichtlich fehlerhafte Richtungsmetadaten mehrteiliger Wendungen wurden anhand der Übungsbeschreibung korrigiert, wenn die Übung wieder in der ursprünglichen Laufrichtung endet.

### v0.2.6

#### 🐛 Behoben

- Kritischen Fehler behoben, durch den Schilder nach dem Drag & Drop nicht mehr auf der Parcoursfläche erschienen.
- Bei der Überarbeitung der Laufwegdarstellung waren Hilfsfunktionen für Schildvorschau und Zusatzschild-Logik versehentlich aus `app.js` entfernt worden.
- Die fehlenden Funktionen wurden wieder eingebunden, sodass normale Schilder und Übungen mit verpflichtendem Zusatzschild wieder korrekt platziert und angezeigt werden.

### v0.2.5

#### ✨ Neu

- Für Stationsnummern stehen jetzt zwei Modi zur Verfügung: **Automatisch** und **Manuell**.
- Im automatischen Modus erhalten neu abgelegte Stationen fortlaufend die nächste freie Nummer.
- Automatisch vergebene Stationsnummern können anschließend jederzeit manuell geändert werden.
- Im manuellen Modus werden neue Stationen zunächst ohne Nummer angelegt und können später individuell nummeriert werden.
- Die Stationsnummer kann direkt im rechten Detailbereich bearbeitet werden.

#### 🔄 Verbessert

- Stationsnummern sind vollständig von der Reihenfolge entkoppelt, in der Schilder auf den Parcours gezogen wurden.
- Der optionale Laufweg wird nun anhand der vergebenen Stationsnummern berechnet und folgt somit Station 1 → 2 → 3 usw.
- Nicht nummerierte Stationen werden im manuellen Modus nicht in die Laufwegberechnung einbezogen.
- Bei eingeblendeten Nummern werden noch nicht nummerierte Stationen mit `?` gekennzeichnet.
- Wird eine bereits vergebene Stationsnummer auf eine andere nummerierte Station gesetzt, werden die beiden Nummern automatisch getauscht.

#### ♻️ Kompatibilität

- Ältere gespeicherte Parcours ohne eigenes Feld für Stationsnummern werden beim Laden automatisch anhand ihrer bisherigen Reihenfolge nummeriert.

### v0.2.4

#### ✨ Neu

- Stationsnummern können optional auf dem Parcours eingeblendet werden.
- Ein optionaler Laufweg verbindet die platzierten Stationen automatisch in ihrer Reihenfolge.
- Der Laufweg wird beim Verschieben von Stationen live neu berechnet.
- Die Wegführung wird als dezente, leicht geschwungene Linie mit Richtungspfeilen dargestellt.

#### 🎨 Design

- Hauptschild und Zusatzschild werden auf dem Parcours nun optisch als zwei eigenständige Schilder dargestellt.
- Zwischen Haupt- und Zusatzschild bleibt ein sichtbarer Abstand; beide besitzen eigenen Rahmen, Hintergrund und Schatten.
- Laufweg und Pfeile verwenden bewusst eine zurückhaltende pastellige Farbe mit geringer Deckkraft, damit die Schilder visuell im Vordergrund bleiben.
- Laufweg und Stationsnummern sind unabhängig voneinander ein- und ausblendbar.

#### 🧩 Vorbereitung

- Die aktuelle Laufwegberechnung verwendet die Reihenfolge der platzierten Stationen.
- Die Laufwegebene ist so vorbereitet, dass später der regelbasierte Parcoursgenerator bzw. eine intelligentere Wegplanung dieselbe Darstellung verwenden kann.

### v0.2.3

#### ✨ Neu

- Klick auf ein Schild in der linken Bibliothek öffnet jetzt direkt die Vorschau mit Regelwerkbeschreibung im rechten Detailbereich.
- Übungen, die laut VDH-Regelwerk zwingend ein Zusatzschild benötigen, verlangen beim Platzieren automatisch die Auswahl eines passenden Zusatzschildes.
- Haupt- und Zusatzschild werden anschließend gemeinsam als eine Station auf dem Parcours dargestellt.
- Das gewählte Zusatzschild kann bei einer bereits platzierten Station im Detailbereich nachträglich geändert werden.

#### ✅ Regelprüfung

- Zusatzschilder Z-a bis Z-e können nicht mehr als eigenständige Station auf den Parcours gezogen werden.
- Zusatzschilder werden als Abschluss einer Hauptübung behandelt und bleiben technisch mit dieser Hauptübung verknüpft.
- Für Senior stehen bei erforderlichen Zusatzschildern ausschließlich Z-a, Z-c und Z-e zur Auswahl.
- Die Pflicht zum Zusatzschild wird aus den entsprechenden Übungsbeschreibungen des VDH-Regelwerks abgeleitet und nicht pauschal nur anhand des Wortes „Vorsitz“ vergeben.

#### 🔄 Verbessert

- Schilder mit erforderlichem Zusatzschild werden bereits in der Bibliothek entsprechend gekennzeichnet.
- Zusatzschilder werden in der Bibliothek als nicht eigenständig platzierbare Schilder gekennzeichnet.

### v0.2.2

#### ✅ Geprüft & korrigiert

- VDH-Klassenzuordnung der Schilder systematisch gegen das Regelwerk 2027 geprüft und als eigene Regelwerkslogik hinterlegt.
- Beginner enthält die Übungen der Gruppe B.
- Klasse 1 enthält die Übungen aus Beginner und Klasse 1.
- Klasse 2 enthält die Übungen aus Beginner, Klasse 1 und Klasse 2.
- Klasse 3 enthält die Übungen aus Beginner, Klasse 1, Klasse 2 und Klasse 3.
- Senior bleibt eine eigenständige Auswahl nach Anhang 3 und wird nicht aus der normalen Klassenhierarchie abgeleitet.
- Für Senior werden bei den Zusatzschildern ausschließlich Z-a, Z-c und Z-e berücksichtigt.
- Die zulässigen Übungszahlen pro Klasse wurden als geprüfte Regelwerksdaten hinterlegt.
- In der Schilderbibliothek wird nun direkt angezeigt, aus welchen Schildergruppen sich die gewählte Klasse zusammensetzt.

#### 🧩 Vorbereitung

- Die geprüften Klassendaten stehen künftig auch der Regelprüfung und dem Parcoursgenerator zur Verfügung.
- Ein separater QA-Datensatz dokumentiert die aktuelle Klassenzuordnung der Bibliothek.

### v0.2.1

#### 🔄 Verbessert

- Parcoursfläche deutlich vergrößert, damit vollständige Parcours mehr Platz zum sinnvollen Aufbau haben.
- Platzierte Schilder auf der Parcoursfläche verkleinert und die Größenverhältnisse zum verfügbaren Parcoursraum angepasst.
- Klassenfilter überarbeitet: Die gewählte Leistungsklasse bestimmt jetzt eindeutig, welche Schilder in der Bibliothek angezeigt werden.
- Höhere VDH-Klassen enthalten weiterhin automatisch alle dort zulässigen Schilder der jeweils niedrigeren Klassen.
- Senior wird nicht mehr als zusätzlicher Filter bzw. Badge innerhalb von Beginner und den regulären Klassen angezeigt, sondern ausschließlich als eigene Leistungsklasse behandelt.
- Typ-A-/Typ-B-Filter bleiben für die VDH-Klassen erhalten und werden bei FCI ausgeblendet.

## 🌸 v0.2 – Schilderbibliothek & Design

### v0.2.0

#### ✨ Neu

- Neues freundliches Pastelldesign.
- Regelwerk-Auswahl für **VDH 2027** und **FCI International**.
- Klassenfilter abhängig vom gewählten Regelwerk.
- Vollständige VDH-Schilderbibliothek mit Originalgrafiken.
- Filter nach Typ A, Typ B und Senior.
- Offizielle Übungsbeschreibung im Detailbereich.
- Zoomfunktion für die Parcoursfläche.
- Stationen werden intern bereits als Container gespeichert.
- Parcoursdaten speichern `rulesetId` und `classId`.

#### 🔄 Verbessert

- Schilderbibliothek deutlich übersichtlicher gestaltet.
- Parcoursfläche vergrößert und optisch ruhiger gestaltet.
- Detailbereich informativer aufgebaut.
- Suche berücksichtigt Nummer, Bezeichnung und Beschreibung.
- Responsive Grundstruktur überarbeitet.

#### 🚧 Vorbereitung

- FCI-Übungsdaten sind bereits im gemeinsamen Datenmodell enthalten.
- FCI-Originalgrafiken werden erst nach verifizierter Zuordnung eingebunden.
- Datenmodell für spätere Mehrschildübungen, Regelprüfung und Generatorlogik vorbereitet.


## 🌱 v0.1 -- Grundversion

### v0.1.0

#### ✨ Grundlage

- Erste nutzbare Version des RO Planers.
- Browserbasierter Parcourseditor.
- Parcoursfläche zum freien Platzieren von Schildern.
- Erste Demo-Schilderbibliothek.
- Schilder können per Drag & Drop auf den Parcours gezogen werden.
- Platzierte Schilder können frei verschoben werden.
- Rotation einzelner Schilder möglich.
- Eigene Notizen können pro platziertem Schild hinterlegt werden.
- Filterung der Schilderbibliothek nach Klasse.
- Suche nach Schildnummer bzw. Bezeichnung.
- Optionales Raster für die Parcoursfläche.
- Parcours kann lokal im Browser gespeichert und wieder geladen werden.
- Responsive Grundstruktur für unterschiedliche Bildschirmgrößen.

#### 🧩 Vorbereitung

- Grundstruktur für eine spätere vollständige Schilderdatenbank geschaffen.
- Vorbereitung auf regelbasierte Parcoursgenerierung.
- Vorbereitung auf Trainings-Tags und technische Übungsmetadaten.

