# Projekt Auwaldinitiative
Eine Projektbeschreibung <strong>"Auen-Renaturierung im Europaschutzgebiet Steirische Grenzmur - Auwaldinitiative"</strong> ist [hier](https://www.bfw.gv.at/waldwissen-forschung/bfw-projektdatenbank/) zu finden.

Die Webkarten sind in html Format eingebettet und sind Teil des Arbeitspakets 5 (AP5) des Projektes, welches ein "okologisches Frühwarnsystem" für den Auwald an der Grenzmur entwickeln soll.

## Zielarten im Auwald:
Grauspecht - Picus canus   
Mittelspecht - Leiopicus medius   
Hirschkäfer - Lucanus cervus 	  
Scharlachkäfer - Cucujus cinnaberinus 	  
Alpenkammmolch - Triturus carnifex   
Gelbbauchunke - Bombina variegata  

## ökologisches Frühwarnsystem: AP5
Die Entwicklung eines Frühwarnsystems zur frühzeitigen Erkennung potenzieller Gefährdungen für die Biodiversität des Auwalds wurde eingeleitet. Ein Startpunkt lag auf der Recherche und systematischen Analyse der Habitatansprüche ausgewählter Zeigerarten durch das Bundesforschungszentrum für Wald - [BFW](https://www.bfw.gv.at/). Diese Analyse bildet die Grundlage für eine vorausschauende Planung von Schutzmaßnahmen sowie für das Monitoring der biologischen Vielfalt in der Projektregion das Natura2000 Schutzgebiet "Auwald an der Grenzmur" in der Süd-Steiermark. Für jede dieser Arten wurden die ökologischen Anforderungskategorien wie Lebensraum, Nahrungsangebot, Waldstruktur und artspezifische Merkmale analysiert. 

Die Erstellung der Risikokarten und Arten-Verbreitungskarten im Projektgebiet erfolgte mit den Datengrundlagen der Feldaufnahmen vom [Ökoteam](https://www.oekoteam.at/de/) (AP5 Datenerhebung) in den Jahren 2024, 2025. Dort fand ein Monitoring der 6 Zielarten, als auch der Umweltparameter statt. Diese dienten als Input-Grundlage für die Modellierungen (Verbreitungskarten mit ABC Modell und Risikokarten) und wurden von Beobachtungsdaten von GBIF und weiteren Umweltdaten als Geographische Umweltdaten (GIS) erweitert (Verbreiungsdaten mit erweitertem Modell). Die Outputs bzw. Ergebnisse der Modellierungen werden in Form von Karten (Risikokarten und Verbreitungskarten) im Frühwarnsystem genutzt.

Modellierungen wurde durchgeführt, um folgende Fragen zu beantworten:
<ul>
  <li> Wo sind potentielle Habitate für die Zeigerarten? (Verbreitungskarten)</li>
    <li> Wie wird im Model deren Vorkommen von Umweltfaktoren beeinflusst? (Modellergebnisse)</li>
    <li> Wo sind diese Risiken erhöht und Eingriffe notwendig? (Risikokarten)</li>
</ul>
Es wurden verschiedene Random-Forest Modellierungen durchgeführt basierend auf entweder den im Feld aufgenommenen kategoriellen Umweltparametern (im Folgenden “ABC-Modell” benannt) und mit zusätzlich gesammelten kontinuierliche GIS-Daten (im Folgenden “erweitertes Modell” genannt). Kategorielle Daten (siehe Tabelle 2) bestanden aus insgesamt neun Parametern zu <strong>Habitatstruktur</strong> (A-stukturreich, B- mäßig sturkturreich, C-strukturarm), <strong> Artenzusammensetzung</strong> (A - typisch, B - bedingt typisch und C- untypisch) und <strong>Störungen</strong> (keine/gering, B – mittel, C – stark). Zusätzlich dazu wurde zum ABC-Model noch der Parameter “Habitat-change” hinzugefügt. Dieser stellt die Veränderung der Habitatqualität seit der letzten Lebensraumkartierungen 2003 im Vergleich zu den aktuellen Kartierungen  dar. Für das erweiterte Modell wurden kontinuierliche räumliche Daten gesammelt, um die Parameter 1-9 zu ergänzen und mit beispielsweise Fragmentierungsparametern, Karten von durch Satellitendaten detektierte Kronenschäden und räumliche Landschaftsparameter wie Distanz zu Flüssen und Seen und Baumartenvielfalt zu werweitern.

### Frühwarnsystem: technische Umsetzung und Integration des Frühwarnsystems in bestehende Überwachungsstrukturen. 
Das Frühwarnsystem wurde anhand von interaktiven Webkarten in einer neu eingerichteten temporären Website erstellt und öffentlich zugänglich gemacht (Abbildung 8). Dafür wurden die erstellten und mit der Modellierung errechneten Kartenlayer über einen webmap-service (wms) in einen öffentlichen Geoserver geladen und gestylt. Auf der Webseite wurden die Kartenansichten und -funktionalitäten (e.g. Auswahl-Panele und Legenden) über die JavaScript Bibliothek OpenLayers integriert. Die Dokumentation des Codes und der verwendeten Daten sind bei GitHub frei einsehbar  (https://github.com/hoffjohanna/auwald_grenzmur_modelle) und die Implementierung kann anhand dem index.html-Code auch jederzeit auf eine beliebige andere Webseite umziehen. In diesem Html befinden sich der gesamte Website-Style, die interaktive Kartendarstellung mit Auswahl-Panelen, Legendendarstellungen und Website-Reiter. Die Seite wurde in ihrer Funktionalität im Webinar am 16. Oktober 2025 präsentiert und mit Teilnehmenden des Webinars aktiv getestet und für die Abschlussveranstaltung angepasst.

### 1) Verbreitungskarten
Es wurden verschiedene Random-Forest Modellierungen durchgeführt basierend auf entweder den im Feld aufgenommenen kategoriellen Umweltparametern (im Folgenden “ABC-Modell” benannt) und mit zusätzlich gesammelten kontinuierliche GIS-Daten (im Folgenden “erweitertes Modell” genannt). Kategorielle Daten bestanden aus insgesamt neun Parametern zu Habitatstruktur (A-stukturreich, B- mäßig sturkturreich, C-strukturarm), Artenzusammensetzung (A - typisch, B - bedingt typisch und C- untypisch) und Störungen (keine/gering, B – mittel, C – stark). Zusätzlich dazu wurde zum ABC-Model noch der Parameter <strong> Habitatveränderung </strong> hinzugefügt. Dieser stellt die Veränderung der Habitatqualität seit der letzten Lebensraumkartierung und deren Zustand im Jahr 2001 im Vergleich zu den aktuellen Kartierungen dar. Für das "erweiterte Modell" wurden kontinuierliche räumliche Daten gesammelt, um die Parameter 1-9 (P1-P9) zu ergänzen und mit beispielsweise Fragmentierungsparametern, Karten von durch Satellitendaten detektierte Kronenschäden und räumliche Landschaftsparameter wie Distanz zu Flüssen und Seen und Baumartenvielfalt zu erweitern. Das erweiterte Modell zeichnet sich auch durch eine räumlich weitere Erfassung der gesamten Projektregion aus.

Die Methodik der Verbreitungskarten ist angelehnt an die Arbeiten von [Paź-Dyderska et al. (2020)](https://doi.org/10.1016/j.ufug.2020.126868). Für alle Analysen nutzten wir R (Version 3.5.3). Um die Verbreitungskarten der 6 Zielarten im Projektgebiet zu modellieren, verwendeten wir einen Random-Forest-Algorithmus. Hier werden Vorkommenswahrscheinlichkeiten jeder Art anhand der Zusammensetzung an (für die Art günstigen und ungünstigen) Umweltfaktoren berechnet. Dieses Verfahren eignet sich besser, weil manche positiven Nachweise der seltenen Arten (hier vor allem Grauspecht und Gelbbauchunke) im Gebiet sehr gering waren und klassische Modelle (z. B. logistische Regression) dadurch stärker verzerrt würden. Random Forest kann außerdem komplexe Zusammenhänge zwischen Variablen gut abbilden. Die Ergebnisse dieser Modellierung sind Verbreitungskarten der Zielarten sowohl für das ABC-Modell mit den kategoriellen Daten, als auch das erweiterte Modell mit den kontinuierlichen Parametern. Anhand von Statistiken wie (pdp plots - partial dependency) und Variablen Einfluss (varimp) konnten die wichtigsten Einflussparameter identifiziert und als "Risikokarten" sichtbar gemacht werden.

##### Parameter zur Habitatstruktur (ABC Modell)
P0-Zustandsveränderung der Habitatqualität (Vergleich zwischen 2003 und 2019)
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
Die Erstellung der Risikokarten und Arten-Verbreitungskarten im Projektgebiet erfolgte mit den Datengrundlagen der Feldaufnahmen vom Ökoteam (AP5 Datenerhebung). Dort fand ein Monitoring der 6 Zielarten, als auch der Umweltparameter (siehe oben; Habitatstruktur, Artenzusammensetzung, Störungen) statt. Diese dienten als Input-Grundlage für die Modellierungen der Verbreitungskarten, ebenso die Grundlage für die Risikokarten. Die Parameter, die im Modell und den Statistiken dazu den höchsten Einluss auf die Verbreitungswahrscheinlichkeit der Zielarten hatten, wurden als Risikoparameter dargestellt.

##### Risikoparameter
Zustandsveränderung (2003-2019)  
P1: Strukturarmut (=wenige Gehölzschichten)  
P2: Mangel an Altbäumen (>35cm Durchmesser)  
P3: Mangel an Totholz  
P4: Baumartenmischung (=geringe Baumartenvielfalt)  
P5: Standortfremde Gehölze (Bäume)  
P6: Neophyten in Krautschicht (Bodenvegetation)  
P7: Verbiss durch Wild  
P8: Kronenschäden  
P9: gestörte Hydrologie  
Fragmentierung (Edge density - Verhältnis von Umfang zu Fläche eines Waldstückes)  


# Verwendung der Verbeitungskarten
Zur Interpretation der Modelle erstellten wir Partielle Abhängigkeitsdiagramme (pdp - Partial-Dependence-Plots), die zeigen, wie einzelne Umweltvariablen die vorhergesagte Wahrscheinlichkeit beeinflussen (Abbidung 3). Die Variablenbedeutung (varimp – variable importance) bestimmten wir über den Anstieg des Modellfehlers (RMSE), wenn einzelne Variablen zufällig durchmischt werden (Abbldung 4). Anhand dieser Plots können Sets aus Einflussfaktoren für jede Zielart herausgearbeitet werden (Abbildung 5). Folgende Aussagen kann man aus diesen Sets angelehnt an die Modellergebnisse herausarbeiten:
<ul>
  <li> Das Verbreitungsmodell für den Scharlachkäfer ist besonders sensibel gegenüber (ggü) Totholzmangel und Habitatveränderungen </li>
  <li> Das Verbreitungsmodell für den Hirschkäfer ist sensibel ggü Totholzmangel und Habitatveränderungen, aber ebenso ggü. Wildeinfluss  und fast alle anderen Faktoren (ausgenommen Fragmentierung)</li>
  <li> Das Verbreitungsmodell für den Kammmolch ist stark beeinflusst von hydrologsichem Regime, sensibel ggü. Habitatqualitätsänderungen, aber auch Neophyten und Mangel an Totholz haben Einfluss </li>
  <li> Die Verbreitungsmodelle für den Grauspecht und Mittelspecht sind Totholz-abhängig, wobei Grauspecht-Modell eine Sensitivität ggü Habitatveränderungen und Wildverbiss aufweist, das Modell des Mittelspechts etwas weniger </li>
  <li> Das Verbreitungsmodell für die Gelbbauchunke wird vor allem negativ beeinflusst von Habitatfragmentierung und -veränderungen, sowie Anomalien des hydrologischen Regimes </li>
</ul>

Diese Ergebnisse sind jedoch mit Vorsicht zu genießen und stellen lediglich Korrelationen, keine Kausalzusammenhänge dar. Auch können Sekundäreffekte nicht ausgeschlossen werden. 
Modellstatistiken der zwei Modelle geben Aufschluss über die Modellgüte. Dabei zeigt sich das ABC in allen Bereichen eindeutig am robustesten und aussagekräftigsten. Deshalb werden für das Frühwarnsystem vor allem Umweltdaten und die Verbreitungskarten des ABC-Modells dargestellt.


# Veroffentlichungen  der Karten
Während der Projektlaufzeit wurden die Karten in lokalen Veranstaltungen und Workshops Teilnehmenden gezeigt, erklärt und miteinander diskutiert. Nach Projektabschluss wurden die Webkarten auf der Website des NUKV Steiermark veröffentlicht:
https://www.nukv.at/riskmaps/

# Datenschutzrichtlinien
Die Verwendung der Karten läuft über den INSPIRE Kartendienst des Land-, forst- und wasserwirtschaftlichen Rechenzentrums (LFRZ). Die Daten sind öffentlich zugänglich. Gemäß § 4 BDSG muss jeder Seitenbesucher über die Erhebung seiner personenbezogenen Daten informiert werden. Hierfür ist eine Datenschutzerklärung notwendig.
