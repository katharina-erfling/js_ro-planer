# 📝 RO Planer -- Changelog

Alle wichtigen Änderungen und Entwicklungsschritte von **RO Planer**.

> RO Planer wird iterativ anhand der praktischen Nutzung
> weiterentwickelt.  
> Der Changelog dokumentiert Funktionen, Verbesserungen und
> Fehlerbehebungen, ohne unnötige interne Implementierungsdetails offenzulegen.

------------------------------------------------------------------------
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

