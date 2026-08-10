# 🐾 RO Planer

Ein browserbasierter Rally-Obedience-Parcoursplaner für Training und Parcoursplanung.

---

## 🌿 Idee

Der RO Planer soll mehr sein als ein klassischer Parcourseditor.

Neben dem freien Erstellen eigener Rally-Obedience-Parcours soll die Anwendung später unter anderem dabei helfen,

- passende Trainingssequenzen zusammenzustellen,
- Parcours nach Leistungsklasse zu erzeugen,
- bestimmte Trainingsschwerpunkte gezielt einzubauen,
- Regeln und Besonderheiten der einzelnen Übungen zu berücksichtigen,
- Mehrschildübungen sinnvoll abzubilden,
- und langfristig regelbasierte Zufallsparcours zu generieren.

Die Entwicklung erfolgt bewusst iterativ: Erst wird eine einfache, funktionierende Basis geschaffen, anschließend werden Funktionen und Bedienung nach und nach ausgebaut.

---

## ✨ Aktueller Stand

### v0.1.0 – Grundversion

Die erste Version enthält:

- browserbasierte Anwendung ohne Installation
- Parcoursfläche
- Schilderbibliothek mit Demo-Schildern
- Filter nach Klasse
- Suche innerhalb der Schilderbibliothek
- Drag & Drop von Schildern auf die Parcoursfläche
- freie Positionierung platzierter Schilder
- Rotation von Schildern
- eigene Notizen pro platziertem Schild
- optionales Raster
- lokales Speichern und Laden des Parcours im Browser
- responsive Grundstruktur

---

## 🚧 In Arbeit

Als nächster größerer Entwicklungsschritt entsteht die echte Schilderbibliothek auf Grundlage des VDH-Regelwerks Rally Obedience 2027.

Geplant sind unter anderem:

- Originalgrafiken der Übungsschilder
- vollständige Schilddaten für die nationalen RO-Klassen
- offizielle Bezeichnungen und Übungsbeschreibungen
- Typ A / Typ B / Typ A oder B
- Zusatzschilder
- technische Metadaten für die spätere Generatorlogik
- Trainings-Tags und Übungskategorien
- Berücksichtigung von Mehrschildübungen
- modernere, freundlichere Benutzeroberfläche mit pastelligem Farbschema

---

## 🧠 Langfristiges Ziel

Der spätere Parcoursgenerator soll Schilder nicht lediglich zufällig auswählen.

Stattdessen soll er einen Parcours anhand hinterlegter Regeln und Übungseigenschaften zusammenstellen und dabei zum Beispiel berücksichtigen:

- gewählte Leistungsklasse
- zulässige Anzahl der Übungen
- Führseiten und Seitenwechsel
- Richtungsänderungen
- Start- und Endzustände von Übungen
- stationäre Übungen und Übungen in Bewegung
- benötigte Zusatzschilder
- Mehrschildübungen
- Platzbedarf und Geräte
- Abstände zwischen Stationen
- sinnvolle Laufwege
- individuelle Trainingsschwerpunkte

Dieses System wird erst schrittweise entwickelt und getestet.

---

## 🛠 Technik

Der RO Planer ist aktuell eine lokale Webanwendung aus:

- HTML
- CSS
- JavaScript

Es wird kein Server benötigt.

---

## ▶️ Start

Repository herunterladen oder klonen und anschließend:

```text
index.html
```

im Browser öffnen.

Die Parcoursdaten werden aktuell lokal im Browser gespeichert.

---

## 📁 Projektstruktur

```text
ro-planer/
├── index.html
├── style.css
├── app.js
├── README.md
└── CHANGELOG.md
```

Die Struktur wird mit dem Ausbau der Schilderbibliothek erweitert, beispielsweise um eigene Daten- und Asset-Ordner.

---

## 📚 Regelwerk & Übungsschilder

Die Entwicklung der Schilderbibliothek orientiert sich am **VDH-Regelwerk Rally Obedience, gültig ab 01.01.2027**.

Die verwendeten offiziellen Übungsschilder und Regelwerksinhalte stammen nicht vom RO Planer. Rechte an Regelwerk, Grafiken, Logos und sonstigen Verbandsinhalten verbleiben bei den jeweiligen Rechteinhabern.

Der RO Planer ist ein privates, unabhängiges Entwicklungsprojekt und keine offizielle Anwendung des VDH.

---

## 🗺️ Geplante Entwicklung

Geplant sind unter anderem:

- vollständige Schilderbibliothek
- schöneres Pastelldesign
- bessere Parcourswerkzeuge
- Parcours speichern und verwalten
- regelbasierte Validierung
- Trainingsparcours
- Zufallsparcours nach Klasse
- Parcours nach Trainingsziel
- Hundeprofile
- Trainingshistorie und Statistiken

Die Reihenfolge kann sich während der praktischen Entwicklung ändern.

---

> **Hinweis:** RO Planer befindet sich in aktiver Entwicklung. Funktionen, Datenmodell und Benutzeroberfläche können sich zwischen den Versionen deutlich verändern.
