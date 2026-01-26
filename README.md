# Projekt Auwaldinitiative
Eine Projektbeschreibung "Auen-Renaturierung im Europaschutzgebiet Steirische Grenzmur - Auwaldinitiative" ist hier zu finden:
https://www.bfw.gv.at/waldwissen-forschung/bfw-projektdatenbank/ 
Die Webkarten sind im html Format gehalten und sind Teil des Arbeitspakets 5 (AP5) des Projektes, welches ein "okologisches Frühwarnsystem" für den Auwald an der Grenzmur entwickeln soll.

## Zielarten im Auwald:
Grauspecht - Picus canus   
Mittelspecht - Leiopicus medius   
Hirschkäfer - Lucanus cervus 	  
Scharlach-käfer - Cucujus cinnaberinus 	  
Alpenkammmolch - Triturus carnifex   
Gelbbauch-unke - Bombina variegata  

## ökologisches Frühwarnsystem: AP5
Die Entwicklung eines Frühwarnsystems zur frühzeitigen Erkennung potenzieller Gefährdungen für die Biodiversität des Auwalds wurde eingeleitet. Ein Startpunkt lag auf der Recherche und systematischen Analyse der Habitatansprüche ausgewählter Zeigerarten. Diese Analyse bildet die Grundlage für eine vorausschauende Planung von Schutzmaßnahmen sowie für das Monitoring der biologischen Vielfalt in der Projektregion. Für jede dieser Arten wurden die ökologischen Anforderungskategorien wie Lebensraum, Nahrungsangebot, Waldstruktur und artspezifische Merkmale analysiert. Besondere Beachtung fanden auch Wanderhindernisse, die für Amphibien wie den Kammmolch und die Gelbbauchunke von hoher Relevanz sein können.

--> Erstellung von Risikokarten und Verbreitungskarten anhand von Habitat-Modellierungen basierend auf Feld-Kartierungen (AP5, Projekt Auwaldinitiative)
Die Erstellung der Risikokarten und Arten-Verbreitungskarten im Projektgebiet erfolgte mit den Datengrundlagen der Feldaufnahmen vom Ökoteam (AP5 Datenerhebung) in den Jahren 2024, 2025. Dort fand ein Monitoring der 6 Zielarten, als auch der Umweltparameter statt. Diese dienten als Input-Grundlage für die Modellierungen (Abbildung 1). Die Outputs bzw. Ergebnisse der Modellierungen werden in Form von Karten (Risikokarten und Verbreitungskarten) im Frühwarnsystem später genutzt.

Modellierungen wurde durchgeführt, um folgende Fragen zu beantworten:
•	Wo sind potentielle Habitate für die Zeigerarten? (Verbreitungskarten)
•	Wie wird deren Vorkommen von Umweltfaktoren beeinflusst? (Modellergebnisse)
•	Wo sind diese Risiken erhöht und Eingriffe notwendig? (Risikokarten)
Es wurden verschiedene Random-Forest Modellierungen durchgeführt basierend auf entweder den im Feld aufgenommenen kategoriellen Umweltparametern (im Folgenden “ABC-Modell” benannt) und mit zusätzlich gesammelten kontinuierliche GIS-Daten (im Folgenden “erweitertes Modell” genannt). Kategorielle Daten (siehe Tabelle 2) bestanden aus insgesamt neun Parametern zu Habitatstruktur (A-stukturreich, B- mäßig sturkturreich, C-strukturarm), Artenzusammensetzung (A - typisch, B - bedingt typisch und C- untypisch) und Störungen (keine/gering, B – mittel, C – stark). Zusätzlich dazu wurde zum ABC-Model noch der Parameter “Habitat-change” hinzugefügt. Dieser stellt die Veränderung der Habitatqualität seit der letzten Lebensraumkartierungen 2001 im Vergleich zu den aktuellen Kartierungen  dar. Für das erweiterte Modell wurden kontinuierliche räumliche Daten gesammelt, um die Parameter 1-9 zu ergänzen und mit beispielsweise Fragmentierungsparametern, Karten von durch Satellitendaten detektierte Kronenschäden und räumliche Landschaftsparameter wie Distanz zu Flüssen und Seen und Baumartenvielfalt zu werweitern.

### Frühwarnsystem: technische Umsetzung und Integration des Frühwarnsystems in bestehende Überwachungsstrukturen. 
Das Frühwarnsystem wurde anhand von interaktiven Webkarten in einer neu eingerichteten temporären Website erstellt und öffentlich zugänglich gemacht (Abbildung 8). Dafür wurden die erstellten und mit der Modellierung errechneten Kartenlayer über einen webmap-service (wms) in einen öffentlichen Geoserver geladen und gestylt. Auf der Webseite wurden die Kartenansichten und -funktionalitäten (e.g. Auswahl-Panele und Legenden) über die JavaScript Bibliothek OpenLayers integriert. Die Dokumentation des Codes und der verwendeten Daten sind bei GitHub frei einsehbar  (https://github.com/hoffjohanna/auwald_grenzmur_modelle) und die Implementierung kann anhand dem index.html-Code auch jederzeit auf eine beliebige andere Webseite umziehen. In diesem Html befinden sich der gesamte Website-Style, die interaktive Kartendarstellung mit Auswahl-Panelen, Legendendarstellungen und Website-Reiter. Die Seite wurde in ihrer Funktionalität im Webinar am 16. Oktober 2025 präsentiert und mit Teilnehmenden des Webinars aktiv getestet und für die Abschlussveranstaltung angepasst.

### 1) Verbreitungskarten
Es wurden verschiedene Random-Forest Modellierungen durchgeführt basierend auf entweder den im Feld aufgenommenen kategoriellen Umweltparametern (im Folgenden “ABC-Modell” benannt) und mit zusätzlich gesammelten kontinuierliche GIS-Daten (im Folgenden “erweitertes Modell” genannt). Kategorielle Daten bestanden aus insgesamt neun Parametern zu Habitatstruktur (A-stukturreich, B- mäßig sturkturreich, C-strukturarm), Artenzusammensetzung (A - typisch, B - bedingt typisch und C- untypisch) und Störungen (keine/gering, B – mittel, C – stark). Zusätzlich dazu wurde zum ABC-Model noch der Parameter “Habitat-change” hinzugefügt. Dieser stellt die Veränderung der Habitatqualität seit der letzten Lebensraumkartierungen 2001 im Vergleich zu den aktuellen Kartierungen  dar. Für das erweiterte Modell wurden kontinuierliche räumliche Daten gesammelt, um die Parameter 1-9 zu ergänzen und mit beispielsweise Fragmentierungsparametern, Karten von durch Satellitendaten detektierte Kronenschäden und räumliche Landschaftsparameter wie Distanz zu Flüssen und Seen und Baumartenvielfalt zu werweitern. 

Die Methodik ist angelehnt an Paź-Dyderska et al. (2020). Für alle Analysen nutzten wir R (Version 3.5.3). Um die Vorkommenswahrscheinlichkeit ("Verbreitungskarten") der 6 Zielarten im Projektgebiet zu modellieren, verwendeten wir einen Random-Forest-Algorithmus. Dieses Verfahren eignet sich besser, weil manche positiven Nachweise der seltenen Arten (hier vor allem Grauspecht und Gelbbauchunke) im Gebiet sehr gering waren und klassische Modelle (z. B. logistische Regression) dadurch stärker verzerrt würden. Random Forest kann außerdem komplexe Zusammenhänge zwischen Variablen gut abbilden. Das Ergebnis dieser Modellierung sind Verbreitungskarten der Zielarten sowohl für das ABC-Modell, als auch das erweiterte Modell mit den kontinuierlichen Parametern. 

##### Parameter zur Habitatstruktur
P1-Vertikalstruktur   
P2-Stammdurchmesser  
P3-Totholz  
##### Parameter zur Artenzusammensetzung
P4-Baumartenmischung  
P5-Neophyten  
P6-Bodenvegetation  
##### Parameter zu Störungen
P7-Wildeinfluss  
P8-Kronenschaden  
P9-Hydrologie  


### 2) Risikokarten 
Die Erstellung der Risikokarten und Arten-Verbreitungskarten im Projektgebiet erfolgte mit den Datengrundlagen der Feldaufnahmen vom Ökoteam (AP5 Datenerhebung). Dort fand ein Monitoring der 6 Zielarten, als auch der Umweltparameter (siehe oben; Hanitatstruktur, Artenzusammensetzung, Störungen) statt. Diese dienten als Input-Grundlage für die Modellierungen der Verbreitungskarten, ebenso die Grundlage für die Risikokarten

# Verwendung der Verbeitungskarten
Zur Interpretation der Modelle erstellten wir Partielle Abhängigkeitsdiagramme (pdp - Partial-Dependence-Plots), die zeigen, wie einzelne Umweltvariablen die vorhergesagte Wahrscheinlichkeit beeinflussen (Abbidung 3). Die Variablenbedeutung (varimp – variable importance) bestimmten wir über den Anstieg des Modellfehlers (RMSE), wenn einzelne Variablen zufällig durchmischt werden (Abbldung 4). Anhand dieser Plots können Sets aus Einflussfaktoren für jede Zielart herausgearbeitet werden (Abbildung 5). Folgende Aussagen kann man aus diesen Sets angelehnt an die Modellergebnisse herausarbeiten:
•	Das Verbreitungsmodell für den Scharlachkäfer ist besonders sensibel gegenüber (ggü) Totholzmangel und Habitatveränderungen
•	Das Verbreitungsmodell für den Hirschkäfer ist sensibel ggü Totholzmangel und Habitatveränderungen, aber ebenso ggü. Wildeinfluss  und fast alle anderen Faktoren (ausgenommen Fragmentierung)
•	Das Verbreitungsmodell für den Kammmolch ist stark beeinflusst von hydrologsichem Regime, sensibel ggü. Habitatqualitätsänderungen, aber auch Neophyten und Mangel an Totholz haben Einfluss 
•	Die Verbreitungsmodelle für den Grauspecht und Mittelspecht sind Totholz-abhängig, wobei Grauspecht-Modell eine Sensitivität ggü Habitatveränderungen und Wildverbiss aufweist, das Modell des Mittelspechts etwas weniger
•	Das Verbreitungsmodell für die Gelbbauchunke wird vor allem negativ beeinflusst von Habitatfragmentierung und -veränderungen, sowie Anomalien des hydrologischen Regimes
Diese Ergebnisse sind jedoch mit Vorsicht zu genießen und stellen lediglich Korrelationen, keine Kausalzusammenhänge dar. Auch können Sekundäreffekte nicht ausgeschlossen werden. 
Modellstatistiken der zwei Modelle geben Aufschluss über die Modellgüte (Abbildung 6 und 7). Dabei zeigt sich das ABC in allen Bereichen eindeutig am robustesten und aussagekräftigsten. Deshalb werden für das Frühwarnsystem vor allem Umweltdaten und die Verbreitungskarten des ABC-Modells dargestellt. Außerdem wurden die Umweltparameter als Risikoparameter hinzugefügt, die am meisten einen negativen Einfluss auf die Verbreitungsmodelle hatten (Abbildung 8).



# Veroffentlichungen  der Karten
Nach Projektabschluss wurden die Webkarten auf der Website des NUKV Steiermark veröffentlicht:
https://www.nukv.at/riskmaps/

