---
name: 05 Suchen und Sortieren
toc: show
---
Im Rahmen dieser Einheiten beschäftigen wir uns mit dem Suchen und Sortieren von Objekten. Der Einfachheit halber werden wir uns am Anfang auf das Sortieren von Zahlen beschränken, wobei jedes Objekt sortiert bzw. ge
# Suchen 
In der Informatik versteht man unter **Suchen** ein Verfahren zur Untersuchung eines Arrays auf einen **bestimmten** Inhalt.

## lineare Suche

### Erklärung:
Die **lineare Suche** ist der einfachste Suchalgorithmus überhaupt. Es wird ein Element in einer Liste oder einem Array mit **n** Elementen gesucht. Dabei ist irrelevant, ob der Array bereits sortiert ist oder nicht.

Der Suchaufwand wächst linear mit der Anzahl der Elemente. Wenn die Daten zufallsverteilt sind, dann werden im Schnitt **n/2** Vergleichsoperationen benötigt. Im besten Fall ist gleich das erste Element der Liste dasjenige, das man sucht, im schlechtesten ist es das letzte.

Wenn die Anzahl der Elemente in einer Liste klein ist, dann ist es oft auch das effizienteste Verfahren.
### Beispiel Anwendung:
| [0] | [1] | [2] | [3] | [4] | [5] | [6] | [7] | [8] | [9] | Gesuchte Zahl |
| - | - | - | - | - | - | - | - | - | - | :-: |
| **16** | 78 | 11 | 9 | 0 | 777 | 45 | 109 | 8 | 90 | **11** |

Als Beispiel wird die Zahl **9** gesucht. angefangen wird zunächst an der Stelle 0 im Array. An dieser Stelle befindet sich die Zahl **16**, da diese nicht die gesuchte Zahl ist gehen wir ein Fach im Array weiter.

| [0] | [1] | [2] | [3] | [4] | [5] | [6] | [7] | [8] | [9] | Gesuchte Zahl |
| - | - | - | - | - | - | - | - | - | - | :-: |
| **16** | 78 | 11 | 9 | 0 | 777 | 45 | 109 | 8 | 90 | **11** |
| ~~16~~ | **78** | 11 | 9 | 0 | 777 | 45 | 109 | 8 | 90 | **11** |

Nach der **16** kommt die **78** die ist ebenfalls noch nicht die gesuchte Zahl somit wird sich weiter bewegt.

| [0] | [1] | [2] | [3] | [4] | [5] | [6] | [7] | [8] | [9] | Gesuchte Zahl |
| - | - | - | - | - | - | - | - | - | - | :-: |
| **16** | 78 | 11 | 9 | 0 | 777 | 45 | 109 | 8 | 90 | **11** |
| ~~16~~ | **78** | 11 | 9 | 0 | 777 | 45 | 109 | 8 | 90 | **11** |
| ~~16~~ | ~~78~~ | **11** | 9 | 0 | 777 | 45 | 109 | 8 | 90 | **11** |

Nach der **78** kommt die gesuchte Zahl **11** und die Suche ist mit der Wiedergabe der gefundenen Informationen beendet.
## binäre Suche

# Einfache Sortieralgorithmen

## Bubblesort
## optimierter Bubblesort
## Insertionsort
## Selectionsort

# Rekursive Sortieralgorithmen

## Mergesort
## Quicksort

# Aufwandsabschätzung
