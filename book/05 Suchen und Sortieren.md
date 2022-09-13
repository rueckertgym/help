---
name: 05 Suchen und Sortieren
toc: show
---
# Suchen und Sortieren auf der linearen Datenstruktur Array
Im Rahmen dieser Einheiten beschäftigen wir uns mit dem Suchen und Sortieren von Objekten. Der Einfachheit halber werden wir uns am Anfang auf das Sortieren von Zahlen beschränken, wobei jedes Objekt sortiert bzw. gesucht werden kann, wenn ein Suchkriterium vorliegt.
## UML Diagramm zum Projekt
Das unten stehende UML Diagramm dient als Vorlage.
```mermaid
classDiagram
    
    class Sortieren {
      -int [] zZahlenarray
      - Random zZufallsgenerator
      +Sortieren()
      +Sortieren(int pGroesse)
      +Sortieren(int pGroesse, int pMaxZahl)
      +bfms() void
      +bfmsZufall() void
      +bfmsZufallFlex(int pMaxZahl) void
      +bubblesort() void
      +insertionsort() void
      +selectionsort() void
      +lineareSuche(int pZahl) boolean
      +binaereSuche(int pGesuchteZahl)
      -binaereSuche_intern(int pZahl, int pBeginn, int pEnde) boolean
      +quicksort() void
      -quicksort_intern(int pL, int pRechts) void
      +mergeSort() void
      -mergesort(int pLo, int pHi) void
      -merge_intern(int links, int mitte, int rechts) void
    }
```
# Auschecken im edugit
Eine Arbeitskopie des Projekts könnt ihr unter https://edugit.org/abitur-2024/01-suchen-und-sortieren-abi-2024.git mit BlueJ auschecken. 
## Aufgabe(n)
1. Erstellt eine Arbeitskopie.
2. Kopiert die Vorlagenklasse unter eurem Namen z.B.: Sortieren_Ulf
3. commitet, pusht und aktualisiert eure Implementation. Die zu implementierenden Aufgaben findet ihr in den Kommentaren oberhalb der Methoden.
4. Fangt zum Begin einer Stunde mit einer frischen Arbeitskopie mit der Implementaion an.

# Suchen 
In der Informatik versteht man unter **Suchen** ein Verfahren zur Untersuchung einer DAtenstruktur (in unserem FAll momentan die Datenstruktur array) auf einen **bestimmten** Inhalt.

## lineare Suche

### Erklärung:
Die **lineare Suche** ist der einfachste Suchalgorithmus überhaupt. Es wird ein Element in einer Liste oder einem Array mit **n** Elementen gesucht. Dabei ist irrelevant, ob der Array bereits sortiert ist oder nicht.

Der Suchaufwand wächst linear mit der Anzahl der Elemente. Wenn die Daten zufallsverteilt sind, dann werden im Schnitt **n/2** Vergleichsoperationen benötigt. Im besten Fall ist gleich das erste Element der Liste dasjenige, das man sucht, im schlechtesten ist es das letzte.

Wenn die Anzahl der Elemente in einer Liste klein ist, dann ist es oft auch das effizienteste Verfahren.
### Beispiel Anwendung:
| [0] | [1] | [2] | [3] | [4] | [5] | [6] | [7] | [8] | [9] | ges. Zahl |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |:-:| :-: | :-: |
| **16** | 78 | 11 | 9 | 0 | 777 | 45 | 109 | 8 | 90 | **11** |

Als Beispiel wird die Zahl **9** gesucht. angefangen wird zunächst an der Stelle 0 im Array. An dieser Stelle befindet sich die Zahl **16**, da diese nicht die gesuchte Zahl ist gehen wir ein Fach im Array weiter.

| [0] | [1] | [2] | [3] | [4] | [5] | [6] | [7] | [8] | [9] | ges. Zahl |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |:-:| :-: | :-: |
| **16** | 78 | 11 | 9 | 0 | 777 | 45 | 109 | 8 | 90 | **11** |
| ~~16~~ | **78** | 11 | 9 | 0 | 777 | 45 | 109 | 8 | 90 | **11** |

Nach der **16** kommt die **78** die ist ebenfalls noch nicht die gesuchte Zahl somit wird sich weiter bewegt.

| [0] | [1] | [2] | [3] | [4] | [5] | [6] | [7] | [8] | [9] | ges. Zahl |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |:-:| :-: | :-: |
| **16** | 78 | 11 | 9 | 0 | 777 | 45 | 109 | 8 | 90 | **11** |
| ~~16~~ | **78** | 11 | 9 | 0 | 777 | 45 | 109 | 8 | 90 | **11** |
| ~~16~~ | ~~78~~ | **11** | 9 | 0 | 777 | 45 | 109 | 8 | 90 | **11** |

Nach der **78** kommt die gesuchte Zahl **11** und die Suche ist mit der Wiedergabe der gefundenen Informationen beendet.

### Struktorgramm
### Java Quellcode
## binäre Suche

### Erklärung:
Eine binäre Suche ist eine schnelle und effiziente Methode, um einen bestimmten Zielwert aus einer Reihe von bestellten Artikeln zu ermitteln. Indem Sie in der Mitte der sortierten Liste beginnen, können Sie den Suchraum effektiv halbieren, indem Sie anhand des Medianwerts im Vergleich zum Zielwert festlegen, ob die Liste auf- oder absteigend sein soll.

Bei der binären Suche musste das Ziel nur mit drei Werten verglichen werden. Im Vergleich zu einer linearen Suche hätte die Suche vom ersten Wert an begonnen und sich nach oben bewegt, wobei das Ziel mit acht Werten verglichen werden musste. Eine binäre Suche ist nur mit einem geordneten Datensatz möglich; Wenn die Daten zufällig angeordnet sind, liefert eine lineare Suche die ganze Zeit über Ergebnisse, während eine binäre Suche wahrscheinlich in einer Endlosschleife stecken bleibt.
### Beispiel Anwendung:

# Einfache Sortieralgorithmen
## Bubblesort
### Video
::youtube[Bubblesort]{#lyZQPjUT5B4}

### Struktogramm und Java Quellcode
::::tabs{id="Algorithmen"}
:::tab{title="Struktogramm" id="Struktogramm"}
![Bubblesort](./Bilder/01_SuchenUndSortieren/Bubblesort_Struktogramm.png "Bubblesort")

Du kannst dir das Struktorgramm auch als json Datei herunterladen. Dieses kann dann im Struktogramm Editor der  [Uni Dresden](https://dditools.inf.tu-dresden.de/ovk/Informatik/Programmierung/Grundlagen/Struktogramme.html) eingebunden und weiterverwendet werden
:download[Herunterladen]{src="./download/Bubblesort_Struktogramm.json"}
:::
:::tab{title="Java Quellcode" id="Java Quellcode"}
```java
   public void bubblesort()
    {   
        int hilfe = 0;
        for (int i = 0; i < zZahlenarray.length; i++)
        {
            for (int x = 0; x < zZahlenarray.length -1; x++)
            {
                if (zZahlenarray [x] > zZahlenarray [+1])
                {
                    hilfe= zZahlenarray[x+1];
                    zZahlenarray [x] = zZahlenarray[x+1];
                    zZahlenarray [x] = hilfe;
                }
            }
        }
    }
```
:::
::::

## optimierter Bubblesort

## Insertionsort
### Video
::youtube[Insertionsort]{#ROalU379l3U}
### Struktorgramm
### Java Quellcode

## Selectionsort
### Video
::youtube[Selectionsort]{#Ns4TPTC8whw}
### Struktorgramm
### Java Quellcode

# Rekursive Sortieralgorithmen

## Mergesort
### Video
::youtube[Mergesort]{#XaqR3G_NVoo}
### Struktorgramm
### Java Quellcode

## Quicksort
### Video
::youtube[Quicksort]{#ywWBy6J5gz8}
### Struktorgramm
### Java Quellcode

# Aufwandsabschätzung

https://cryptpad.fr/sheet/#/2/sheet/view/xH9bfbaoI0-4Vb9TtHEUxhpMWZ-P63gabh4H6ZmrGy0/
