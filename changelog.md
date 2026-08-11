# 📝 RO Planer -- Changelog

Alle wichtigen Änderungen und Entwicklungsschritte von **RO Planer**.

> RO Planer wird iterativ anhand der praktischen Nutzung
> weiterentwickelt.  
> Der Changelog dokumentiert Funktionen, Verbesserungen und
> Fehlerbehebungen, ohne unnötige interne Implementierungsdetails offenzulegen.

------------------------------------------------------------------------
### v0.3.4

#### 🌍 FCI-Equipmentregeln

- FCI-Schilder können jetzt strukturierte Angaben zum benötigten Equipment enthalten.
- Die bereits regelwerksgesicherten Rückruf- und Kegelübungen wurden mit ihren benötigten Pylonen verknüpft.
- Im rechten Detailbereich wird bei entsprechenden FCI-Schildern das benötigte Equipment samt Abstandshinweis angezeigt.

#### 🧭 FCI-Gerätemodi

- Neuer dreistufiger Modus für die FCI-Geräteunterstützung:
  - **Setzhilfe** – das benötigte Gerät wird nach dem Schild direkt zum manuellen Setzen aktiviert.
  - **Automatisch** – das benötigte Einzelgerät wird automatisch an der hinterlegten empfohlenen Position eingefügt.
  - **Aus** – keine automatische Geräteunterstützung.
- Der gewählte FCI-Gerätemodus wird lokal gespeichert.

#### 📏 Live-Abstandsmessung

- Während der manuellen FCI-Setzhilfe wird die Distanz zwischen Schild und aktuell zu platzierendem Gerät live in Metern angezeigt.
- Bei festen Zielabständen wird der Sollwert direkt eingeblendet.
- Bei zulässigen Bereichen wird der gültige Meterbereich angezeigt.
- Erreicht die aktuelle Distanz den hinterlegten Zielwert bzw. liegt sie im erlaubten Bereich, erscheint ein dezentes **✓**.
- Die Live-Messung nutzt denselben Metermaßstab wie die bestehende Distanzanzeige im Parcours.

#### 🧠 Vorbereitung

- Equipmentbedarf, Gerätemenge, Rollen und Platzierungsregeln sind als eigene FCI-Regeldaten strukturiert.
- Diese Daten können später direkt für automatische Komplettaufbauten, Regelprüfung und FCI-Generator verwendet werden.

### v0.3.3

#### 🎨 Darstellung

- Die ausgeschriebene Übungsbezeichnung unter platzierten Schildern wurde von der Parcoursfläche entfernt.
- Auf dem Parcours werden jetzt nur noch **Originalschildgrafik und Schildnummer** angezeigt.
- Die Änderung gilt sowohl für **VDH-** als auch für **FCI-Schilder**.
- Die vollständige Bezeichnung bleibt weiterhin in der Schilderbibliothek und im rechten Detailbereich verfügbar.

#### 🔄 Verbessert

- Platzierte Schilder sind dadurch deutlich kompakter und beanspruchen weniger Raum auf der Parcoursfläche.
- Die Höhe der Schildkarten wurde entsprechend reduziert.
- Der Fokus auf der Parcoursfläche liegt stärker auf Schildgrafik, Position, Nummerierung, Geräten und Laufweg.

### v0.3.2

#### 🇩🇪 Deutsche FCI-Regelwerktexte

- Die Detailbeschreibungen aller **89 FCI-Übungsschilder 101–422** wurden auf die deutsche Fassung des FCI-Regelwerks 2024 umgestellt.
- Die Ansicht **„Regelwerk“** zeigt bei FCI-Schildern nun die deutsche Übungsbeschreibung.
- Die offiziellen englischen Originalschilder und deren englische Bezeichnungen bleiben unverändert, da bei internationalen FCI-Wettbewerben die Originalschilder verwendet werden.
- Die bisher hinterlegten englischen Beschreibungen bleiben intern als Referenz erhalten.
- Die deutschen Beschreibungen werden als inoffizielle Übersetzung gekennzeichnet; im Zweifel gilt weiterhin die offizielle englische FCI-Fassung.

#### 📝 Kurz erklärt

- Für alle FCI-Schilder wurde die Ansicht **„Kurz erklärt“** aus den deutschen Regelwerkbeschreibungen neu aufgebaut.
- Die Kurzansicht zeigt die jeweilige Übung als deutsche Bullet Points.
- Die Stichpunkte werden ausschließlich aus dem deutschen Regelwerktext abgeleitet und ergänzen keine zusätzlichen Übungsregeln.
- Langfassung, Kurzfassung und technische Generator-Metadaten bleiben getrennte Datenbereiche.

#### 🐛 Behoben

- In der Gerätebibliothek wurden die Illustrationen für **Pylone** und **Hürde/Sprung** nicht mehr angezeigt.
- Ursache war eine falsche CSS-Klassenzuordnung in der Geräte-Vorschau.
- Pylone und Hürde werden sowohl in der linken Geräteauswahl als auch im rechten Vorschaufenster wieder korrekt dargestellt.
- Die Darstellung der Geräte auf der Parcoursfläche bleibt unverändert.

### v0.3.1

#### 🌍 FCI-Schilderbibliothek

- Die bisherige provisorische FCI-Schilderbibliothek wurde vollständig neu aus der offiziellen FCI-Quelle aufgebaut.
- Alle **89 nummerierten FCI-Übungsschilder von 101 bis 422** sind jetzt vorhanden.
- Das in der bisherigen Datenbasis fehlende Schild **322 · TURN AROUND, RECALL FRONT STOP, RIGHT TO LEFT, STOP (B)** wurde ergänzt.
- Zusätzlich wurden die offiziellen Grafiken für **START** und **FINISH** als FCI-Assets hinterlegt.

#### 🖼️ Originalschilder

- Jedes FCI-Schild verwendet jetzt die zugehörige Originalgrafik aus dem offiziellen FCI-Dokument **„Descriptions of the FCI Class Exercise Signs“**.
- Die Grafiken wurden in der offiziellen Dokumentreihenfolge eindeutig den Schildnummern zugeordnet.
- Die bisherigen Platzhalter bzw. nicht verifizierten Bildzuordnungen wurden ersetzt.
- Der Bildstatus der FCI-Schilder ist jetzt als **verifiziert** hinterlegt.

#### 📚 Offizielle Schilddaten

- Englische Originalbezeichnungen der FCI-Schilder wurden mit der offiziellen Quelle abgeglichen.
- Punktwerte werden korrekt aus den vier FCI-Schildgruppen 1 / 2 / 3 / 4 übernommen.
- Arbeitsbereiche A / B / C / D werden, soweit im Schildtitel angegeben, strukturiert gespeichert.
- Die ausführlichen offiziellen englischen Übungsbeschreibungen aus FCI Item 5 wurden den einzelnen Schildern zugeordnet.
- Die FCI-Daten sind als **„verified-from-official-fci-item-5“** gekennzeichnet.

#### 🧠 Grundlage für den FCI-Planer

- Die Geräte-, Abstands- und Setzhilfen können ab jetzt auf die tatsächlich richtigen FCI-Schildnummern und Originalschilder referenzieren.
- Weitere FCI-Regellogik wird auf dieser verifizierten Bibliothek aufgebaut und nicht mehr auf dem früheren provisorischen Datenstand.

## 🌍 v0.3 – FCI-Manueller Parcoursplaner

### v0.3.0

#### ✨ Neu

- Neuer Entwicklungsschwerpunkt **FCI International Class** für das manuelle Erstellen von Trainings- und Wettkampfparcours.
- Meterbasierter Parcoursmaßstab mit **55 px = 1 m**.
- Direkte Distanzanzeige zwischen aufeinanderfolgenden nummerierten Stationen.
- Zusätzliche Distanzanzeige zwischen verknüpften Schildern und Geräten/Pylonen.
- Distanzwerte werden in Metern mit einer Nachkommastelle dargestellt.
- Die Distanzanzeige kann separat ein- und ausgeschaltet werden.

#### 🧭 FCI-Setzhilfe

- Neue zuschaltbare **FCI-Setzhilfe**.
- Nach dem Platzieren bestimmter FCI-Schilder kann der Planer automatisch in den Modus **„Pylone setzen“** wechseln.
- Die benötigte Pylone befindet sich damit sinngemäß direkt „in der Hand“ und wird mit dem nächsten Klick auf die Parcoursfläche gesetzt.
- Die Setzhilfe kann jederzeit deaktiviert werden, wenn Geräte vollständig manuell oder über einen automatischen Komplettaufbau gesetzt werden sollen.
- Erste Setzhilfen wurden für Übungen mit Rückrufmarkierungen sowie für die 90°-Kegelübungen vorbereitet.

#### 📏 FCI-Distanzen

- Die allgemeinen FCI-Abstände von etwa **3–5 m zwischen Übungen** können nun direkt beim manuellen Parcoursbau kontrolliert werden.
- Regelwerksabhängige Geräteabstände können als technische Metadaten hinterlegt und im Planer sichtbar gemacht werden.
- Für Rückrufmarkierungen sind **5 m** als Regelwert vorbereitet.
- Für die Kegelübungen 417/418 ist der Bereich **1–2 m** vorbereitet.
- Die vorhandene Struktur ist außerdem für **2 m Schild → Sprung** und **1,5–2 m Schild → erster Kegel bei Figurenübungen** vorbereitet.

#### 🧠 Vorbereitung

- Distanzwerte und FCI-Geräteanforderungen liegen nicht nur als UI-Hinweise vor, sondern sind als technische Regeln vorbereitet.
- Damit können dieselben Daten später für Warnungen, automatische PO-Aufbauten und den eigentlichen FCI-Parcoursgenerator verwendet werden.


### v0.2.19

#### 🐛 Behoben

- Der automatische Aufbau für **1-111 · Slalom einfach mit Ablenkung** war räumlich falsch am Schild verankert.
- Die Gerätefolge wurde bisher über ihren Mittelpunkt positioniert; dadurch konnte die erste bzw. unterste Pylone hinter dem Übungsschild liegen oder optisch verschwinden.
- Die fehlerhafte Mittelpunkt-Verankerung wurde für diesen Aufbau entfernt.

#### 🐾 VDH 2027

- Der Slalom-Aufbau folgt jetzt der tatsächlichen PO-Struktur:
  - erste Pylone
  - erste Ablenkungsschale
  - zweite Ablenkungsschale
  - letzte Pylone
- Alle vier Positionen liegen auf einer gedachten Geraden mit jeweils **1,50 m Abstand**.
- Das Übungsschild wird entsprechend der PO **in der Nähe der ersten Pylone** platziert.
- Der Eingang in den Slalom bleibt damit zwischen erster Pylone und erster Ablenkung abbildbar.

#### 🧠 Parcourslogik

- Für Geräteaufbauten kann nun eine explizite Ankerstrategie hinterlegt werden.
- Der Slalom mit Ablenkung verwendet `first-item` als Anker: Nicht der Mittelpunkt der Gruppe, sondern das erste Gerät bestimmt die Lage relativ zum Schild.
- Zusätzlich können seitlicher Abstand und Vorwärtsversatz des ersten Geräts relativ zur Station definiert werden.
- Diese Ankerlogik kann später auch für weitere PO-Aufbauten verwendet werden, bei denen das Schild ausdrücklich in der Nähe eines bestimmten Geräts stehen muss.

### v0.2.18

#### 🐛 Behoben

- Automatisch eingefügte Geräteaufbauten konnten bisher teilweise in das zugehörige Übungsschild hineinragen.
- Ursache war eine feste Positionierung des Set-Mittelpunkts, ohne die tatsächliche Länge des Geräteaufbaus zu berücksichtigen.
- Beim Slalom konnte dadurch insbesondere die unterste Pylone im Bereich des Schildes stehen.

#### 🔄 Verbessert

- Der Abstand eines verknüpften Geräteaufbaus zum Schild wird nun anhand der tatsächlichen Ausdehnung des Sets berechnet.
- Der komplette Slalom-Aufbau liegt bei Standardausrichtung sauber oberhalb des Schildes.
- Zwischen Schild und nächstem Gerät bleibt ein kleiner visueller Sicherheitsabstand.
- Die Abstandsermittlung funktioniert auch nach einer Drehung der Station in 90°-Schritten.

#### 🧠 Parcourslogik

- Für verknüpfte Geräte-Sets wird neben der Stationstiefe auch die halbe Ausdehnung des jeweiligen Presets berücksichtigt.
- Reihen- und Sequenzaufbauten werden anhand von Geräteanzahl und hinterlegtem Abstand berechnet.
- Rautenförmige Aufbauten können dieselbe Logik über ihre hinterlegte Längsausdehnung verwenden.

### v0.2.17

#### 🐛 Behoben

- Beim Drehen gruppierter Geräte wurden bisher nicht nur deren Positionen, sondern auch die einzelnen Geräte selbst mitgedreht.
- Dadurch erschienen insbesondere Schalen nach einer Drehung des Aufbaus seitlich bzw. hochkant.
- Die Gruppenrotation wurde korrigiert: Sie verändert jetzt ausschließlich die räumliche Anordnung der Geräte.

#### 🔄 Verbessert

- Pylonen, Schalen und Hürden behalten beim Drehen eines Geräte-Sets ihre eigene optische Ausrichtung bei.
- Dasselbe Verhalten gilt für Geräteaufbauten, die direkt mit einem Übungsschild verknüpft sind.
- Beim Drehen eines Schildes rotiert der verknüpfte Aufbau weiterhin passend um die Station, die einzelnen Geräte bleiben dabei jedoch optisch aufrecht.
- Die Bezeichnung **„Gruppe drehen“** wurde in **„Anordnung drehen“** geändert.
- Bei verknüpften Aufbauten lautet die Aktion nun **„Schild + Anordnung drehen“**.

#### 🧠 Parcourslogik

- Gruppenrotation und Geräteausrichtung werden nun als zwei getrennte Konzepte behandelt.
- `groupRotation` beschreibt ausschließlich die Orientierung der Anordnung.
- `rotation` eines einzelnen Geräts wird durch das Drehen der Gruppe nicht mehr automatisch verändert.

### v0.2.16

#### ✨ Neu

- Regelwerksbezogene Geräteaufbauten werden beim Einfügen direkt mit dem zugehörigen Übungsschild verknüpft.
- Schild und verknüpfter Geräteaufbau können als gemeinsame Einheit verschoben werden.
- Wird ein verknüpftes Geräte-Set bewegt, bewegt sich das zugehörige Schild ebenfalls mit.
- Beim Drehen eines Schildes rotiert der komplette verknüpfte Aufbau passend mit.
- Wird ein verknüpftes Geräte-Set ausgewählt, steht die gemeinsame Aktion **„Schild + Aufbau drehen“** zur Verfügung.

#### 🐾 Slalom-Aufbau

- Der Slalom-Aufbau wird bei aufrechter Schildausrichtung standardmäßig **oberhalb des Schildes nach oben in Laufrichtung** angeordnet.
- Die Geräte bleiben dabei als Set gruppiert und zusätzlich mit der Übungsstation verknüpft.
- Bei einer Drehung der Station um 90°, 180° oder 270° wird die komplette Geräteanordnung entsprechend mitgedreht.

#### 🖱️ Mehrfachauswahl

- Auf freier Parcoursfläche kann jetzt durch Aufziehen eines Rechtecks eine Mehrfachauswahl erstellt werden.
- Das Auswahlrechteck kann gleichzeitig Übungsschilder und Geräte erfassen.
- Alle markierten Elemente können anschließend gemeinsam verschoben werden.
- Die komplette Mehrfachauswahl kann mit **Entf/Delete** gelöscht werden.
- Im rechten Detailbereich wird die Anzahl der ausgewählten Elemente angezeigt.
- Verknüpfte Geräte folgen auch dann ihrem Schild, wenn bei einer Mehrfachauswahl nur das Schild selbst erfasst wurde.

#### 🧠 Parcourslogik

- Schild und Geräte bleiben technisch eigenständige Objekte, werden bei automatisch erzeugten Aufbauten aber explizit miteinander verknüpft.
- Dadurch bleibt die bestehende Geräte-Gruppierung erhalten, während zusätzlich gemeinsames Verschieben und Drehen mit der Station möglich ist.
- Beim bewussten Auflösen einer Gerätegruppe kann die Verbindung zur Station wieder gelöst werden.
- Beim Löschen einer Station werden noch mit ihr verknüpfte Geräte ebenfalls entfernt.

### v0.2.15

#### ✨ Neu
- Übungsschilder können direkt mit einem passenden Geräteaufbau verknüpft werden.
- Bei verknüpften, platzierten Schildern erscheint **„Passenden Aufbau hinzufügen“**.
- Der Aufbau wird als gruppiertes Geräte-Set eingefügt und bleibt verschiebbar, drehbar und auflösbar.

#### 🐾 VDH 2027
- **1-111 · Slalom einfach mit Ablenkung** und **2-220 · Slalom hin und zurück – mit Ablenkung** wurden mit dem passenden Grundaufbau verknüpft.
- Der Aufbau besteht aus **2 Pylonen und 2 Ablenkungsschalen** auf einer gedachten Geraden mit jeweils **1,50 m Abstand**.
- Die beiden mittleren Positionen werden durch die Ablenkungsschalen gebildet.

#### 🧠 Parcourslogik
- Geräteaufbauten sind als technische Metadaten am Schild hinterlegt.
- Weitere Aufbauten werden nur ergänzt, wenn ihre Anordnung aus dem Regelwerk eindeutig hervorgeht.

### v0.2.14

#### 🐛 Behoben

- Fehler behoben, durch den die Drehsteuerung bei gruppierten Pylonen und Schalen nicht angezeigt wurde.
- Die Sichtbarkeit der Rotation wird bei Geräte-Sets jetzt ausdrücklich anhand der Gruppierung geprüft und nicht nur anhand der Drehbarkeit des einzelnen Geräts.

#### 🔄 Verbessert

- Wird ein Gerät aus einem gruppierten Set ausgewählt, erscheint im rechten Detailbereich jetzt **„Gruppe drehen“**.
- Die komplette Gruppe kann dort über die vier festen Ausrichtungen **0° / 90° / 180° / 270°** gedreht werden.
- Dies funktioniert auch bei Pylonen und Schalen, die als Einzelobjekte keine eigene Rotation benötigen.
- Nach dem Auflösen der Gruppe wird die Gruppen-Drehsteuerung wieder ausgeblendet; bei individuell drehbaren Geräten bleibt die normale Ausrichtung verfügbar.

### v0.2.13

#### 🔄 Verbessert

- Die stufenlose Rotation von Übungsschildern wurde entfernt.
- Schilder lassen sich nur noch in den vier sinnvollen Parcoursrichtungen **0° / 90° / 180° / 270°** ausrichten.
- Auch drehbare Einzelgeräte verwenden ausschließlich diese vier festen Richtungen.
- Der bisherige Schieberegler wurde durch vier eindeutige Ausrichtungsbuttons ersetzt.

#### ✨ Neu

- Gruppierte Geräte-Sets können nun als komplette Einheit gedreht werden.
- Die gesamte Set-Anordnung rotiert dabei in 90°-Schritten um ihren gemeinsamen Mittelpunkt.
- Abstände und Form des Sets bleiben beim Drehen erhalten.
- Eine Pylonenreihe kann damit beispielsweise direkt von waagerecht auf senkrecht gedreht werden, ohne die einzelnen Pylonen neu platzieren zu müssen.

#### 🧠 Parcourslogik

- Automatisch ausgerichtete Schilder werden ebenfalls auf die vier rechtwinkligen Richtungen begrenzt.
- Gruppen speichern ihre gemeinsame Ausrichtung separat von der individuellen Geräteausrichtung.
- Beim Lösen oder vollständigen Auflösen einer Gerätegruppe wird die Gruppenrotation sauber entfernt, die aktuelle Lage der Einzelgeräte bleibt jedoch erhalten.

#### ♻️ Kompatibilität

- Freie Rotationswerte aus älteren gespeicherten Parcours werden beim Laden automatisch auf die nächstgelegene Ausrichtung 0°, 90°, 180° oder 270° gesetzt.

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

