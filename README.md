# Masterarbeit-Code
Entwicklung einer Methode für die Berechnung der aktuellen Erreichbarkeit von Ärzten sowie die Simulation verschiedener Szenarien in der Zukunft. 

# Datengrundlage 
Die verwendeten Daten stammen allesamt aus OSM. Für die Vorbereitung der Daten, insbesondere das Zuschneiden auf das entsprechend zu untersuchende Bundesland, erfolgt im Skript [Datenvorbereitung.ipynb](https://github.com/SophieHartstock/Masterarbeit-Code/blob/master/Datenvorbereitung.ipynb)

# Methode
Für die Erreichbarkeitsanalyse werden Isochronen mittels Alpha-Shapes verwendet. Für die Eingabe ist ein Netzwerk-Graph notwendig, z. B. aus OpenStreetMap (Achtung: die Beispieldaten sind in Git LFS abgelegt!). Zudem wird ein Punkt-Datensatz benötigt, in dem die Ausgangspunkte definiert sind. 

Die unterschiedlichen Szenarien für die Simulation sind wie folgt:

1. Zufälliger Wegfall von Standorten der Ärzte
2. Gewichteter Wegfall von Standorten von Ärzten (auf Grundlage des Bevölkerungsanteil Ü64 pro Gemeinde)

Beide Szenarien werden im Skript [Isochronen.ipynb](https://github.com/SophieHartstock/Masterarbeit-Code/blob/master/Isochronen.ipynb) aufgegriffen und reduzieren den Datensatz der Ärzte um 30 %.

Die Auswertung erfolgt über das Verschneiden der erstellten Isochronen mit den Daten zu den Einwohnerzahlen.

## Ausblick
Eine weitere dankbare Methode für die Erreichbarkeitsanalyse ist die Erstellung von Rastern, die die durchschnittliche Fahrzeit zum nächstgelegenen Arzt beinhalten. Die Erstellung des Rasters werden beispielhaft im Skript [Rastererstellung.ipynb](https://github.com/SophieHartstock/Masterarbeit-Code/blob/master/Rastererstellung.ipynb) festgehalten.