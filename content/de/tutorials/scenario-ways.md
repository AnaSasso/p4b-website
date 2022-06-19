---
title: Szenarien - Wege
permalink: "/de/tutorials/scenario-ways/"
weight: 30
sections:
- training

---
#### Beschreibung des Features

GOAT ermöglicht die Entwicklung eigener Szenarien, wie z.B. der Modifikation des Netzwerks oder der Bau einer neuen Brücke. Das entwickelte Szenario kann zu dem aktuellen Netzwerk hinzugefügt und Änderungen der Erreichbarkeit durch Isochronen bewertet werden.

#### Mögliche Anwendungsfälle (Planungsfragen)

* Wie verändert sich die Erreichbarkeit durch den Bau einer neuen Fahrradbrücke über einen Fluss?
* Welche Variante eines neuen Radweges erschließt die höchste Anzahl an Anwohnern?

#### Schritt-für-Schritt-Anleitung für eine beispielhafte Planungsaufgabe

#### 1 Szenario zu neuer Fahrradbrücke

##### 1.1 Planungsfrage

Wie verändert sich die Erreichbarkeit durch den Bau einer neuen Fahrradbrücke über einen Fluss?

##### 1.2 Arbeitsschritte

1. Gehen Sie in das Fenster zur Szenarienentwicklung und erstellen Sie ein neues Szenario.

<img src="/images/tutorials/Scenario_POIs/create_scenario.webp"  alt="Create scenario" style="max-height:300px;"/>

2. Geben Sie dem Szenario einen Namen und klicken Sie auf "OK".

<img src="/images/tutorials/Scenario_building/name_scenario.webp"  alt="Name scenario" style="max-height:200px;"/>

3. Wählen Sie welchen Layer Sie bearbeiten möchten; in diesem Fall den „Wege“-Layer.

<img src="/images/tutorials/Scenario_building/scenario_ways.webp"  alt="Edit ways" style="max-height:350px;"/>

4. Sie befinden sich nun im Szenario-Modus. Um dies zu verdeutlichen, ändert sich die Menü-Farbe von grün zu dunkelblau.
   
5. Zoomen Sie zu der Stelle, an der Sie eine neue Fahrradbrücke bauen wollen und wählen Sie mittels des Kreis-Werkzeuges das umliegenden Straßennetz aus.

<img src="/images/tutorials/Scenario_building/circle_scenario.webp"  alt="Circle tool"/>

6. Zeichnen Sie an der gewünschten Stelle eine neue Wegeverbindung, wählen Sie als Wegetyp „Brücke“ aus und klicken Sie auf „Speichern“. Die gezeichneten Wege werden nun rechts in der Tabelle aufgeführt. 

<img src="/images/tutorials/Scenario_building/bridge_building.webp"  alt="Draw" style="max-height:300px;"/>

7. Indem Sie sich die Isochronen für den Ist-Zustand und für das Szenario berechnen lassen, können Sie die Auswirkung der neuen Wegeverbindung auf die Erreichbarkeit analysieren. Wählen Sie hierzu den Routingmodi „Fahrrad“ aus und setzen den Berechnungsmodus auf „Vergleich“. In den Optionen können Sie die Reisezeit, die Fahrgeschwindigkeit und die Anzahl der zu berechnenden Isochronen einstellen.

<img src="/images/tutorials/Scenario_building/comparison.webp"  alt="Comparison" style="max-height:400px;"/>

8. Platzieren Sie den Startpunkt für die Isochronenberechnung in der Nähe der neuen Brücke. Als Ergebnis wird Ihnen in Rot die Isochronen im Ist-Zustand und in Grün die Isochronen unter Berücksichtigung der neuen Wegeverbindung angezeigt. Der Ergebnistabelle können Sie die jeweilige Fläche und Einwohnerzahl innerhalb der Isochrone entnehmen.

<img src="/images/tutorials/Scenario_building/result_isochrone.webp"  alt="Result" />
