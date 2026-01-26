### Projekt Auwaldinitiative
Eine Projektbeschreibung "Auen-Renaturierung im Europaschutzgebiet Steirische Grenzmur - Auwaldinitiative" ist hier zu finden:
https://www.bfw.gv.at/waldwissen-forschung/bfw-projektdatenbank/ 
Die Webkarten sind im html Format gehalten und sind Teil des Arbeitspakets 5 (AP5) des Projektes, welches ein "okologisches Frühwarnsystem" für den Auwald an der Grenzmur entwickeln soll.

# ökologisches Frühwarnsystem: AP5
--> Erstellung von Risikokarten und Verbreitungskarten anhand von Habitat-Modellierungen basierend auf Feld-Kartierungen (AP5, Projekt Auwaldinitiative)
Die Erstellung der Risikokarten und Arten-Verbreitungskarten im Projektgebiet erfolgte mit den Datengrundlagen der Feldaufnahmen vom Ökoteam (AP5 Datenerhebung) in den Jahren 2024, 2025. Dort fand ein Monitoring der 6 Zielarten, als auch der Umweltparameter statt. Diese dienten als Input-Grundlage für die Modellierungen (Abbildung 1). Die Outputs bzw. Ergebnisse der Modellierungen werden in Form von Karten (Risikokarten und Verbreitungskarten) im Frühwarnsystem später genutzt.

Modellierungen wurde durchgeführt, um folgende Fragen zu beantworten:
•	Wo sind potentielle Habitate für die Zeigerarten? (Verbreitungskarten)
•	Wie wird deren Vorkommen von Umweltfaktoren beeinflusst? (Modellergebnisse)
•	Wo sind diese Risiken erhöht und Eingriffe notwendig? (Risikokarten)
Es wurden verschiedene Random-Forest Modellierungen durchgeführt basierend auf entweder den im Feld aufgenommenen kategoriellen Umweltparametern (im Folgenden “ABC-Modell” benannt) und mit zusätzlich gesammelten kontinuierliche GIS-Daten (im Folgenden “erweitertes Modell” genannt). Kategorielle Daten (siehe Tabelle 2) bestanden aus insgesamt neun Parametern zu Habitatstruktur (A-stukturreich, B- mäßig sturkturreich, C-strukturarm), Artenzusammensetzung (A - typisch, B - bedingt typisch und C- untypisch) und Störungen (keine/gering, B – mittel, C – stark). Zusätzlich dazu wurde zum ABC-Model noch der Parameter “Habitat-change” hinzugefügt. Dieser stellt die Veränderung der Habitatqualität seit der letzten Lebensraumkartierungen 2001 im Vergleich zu den aktuellen Kartierungen  dar. Für das erweiterte Modell wurden kontinuierliche räumliche Daten gesammelt, um die Parameter 1-9 zu ergänzen und mit beispielsweise Fragmentierungsparametern, Karten von durch Satellitendaten detektierte Kronenschäden und räumliche Landschaftsparameter wie Distanz zu Flüssen und Seen und Baumartenvielfalt zu werweitern.

# Frühwarnsystem: technische Umsetzung und Integration des Frühwarnsystems in bestehende Überwachungsstrukturen. 
Das Frühwarnsystem wurde anhand von interaktiven Webkarten in einer neu eingerichteten temporären Website erstellt und öffentlich zugänglich gemacht (Abbildung 8). Dafür wurden die erstellten und mit der Modellierung errechneten Kartenlayer über einen webmap-service (wms) in einen öffentlichen Geoserver geladen und gestylt. Auf der Webseite wurden die Kartenansichten und -funktionalitäten (e.g. Auswahl-Panele und Legenden) über die JavaScript Bibliothek OpenLayers integriert. Die Dokumentation des Codes und der verwendeten Daten sind bei GitHub frei einsehbar  (https://github.com/hoffjohanna/auwald_grenzmur_modelle) und die Implementierung kann anhand dem index.html-Code auch jederzeit auf eine beliebige andere Webseite umziehen. In diesem Html befinden sich der gesamte Website-Style, die interaktive Kartendarstellung mit Auswahl-Panelen, Legendendarstellungen und Website-Reiter. Die Seite wurde in ihrer Funktionalität im Webinar am 16. Oktober 2025 präsentiert und mit Teilnehmenden des Webinars aktiv getestet und für die Abschlussveranstaltung angepasst.




# 1) Verbreitungskarten
Die Methodik ist angelehnt an Paź-Dyderska et al. (2020) . Für alle Analysen nutzten wir R (Version 3.5.3). Um die Vorkommenswahrscheinlichkeit ("Verbreitungskarten") der 6 Zielarten im Projektgebiet zu modellieren, verwendeten wir einen Random-Forest-Algorithmus. Dieses Verfahren eignet sich besser, weil manche positiven Nachweise der seltenen Arten (hier vor allem Grauspecht und Gelbbauchunke) im Gebiet sehr gering waren und klassische Modelle (z. B. logistische Regression) dadurch stärker verzerrt würden. Random Forest kann außerdem komplexe Zusammenhänge zwischen Variablen gut abbilden. Das Ergebnis dieser Modellierung sind Verbreitungskarten der Zielarten sowohl für das ABC-Modell (Abbildung 2A), als auch das erweiterte Modell mit den kontinuierlichen Parametern (Abbildung 2B). 

Artenvorkommen:
Lucanus
Triturus
Cucujus
Leiopicus
...

# 2) Risikokarten 
P1-Vertikalstruktur
P2-Stammdurchmesser
P3-Totholz
P4-Baumartenmischung
P5-Neophyten
P6-Bodenvegetation
P7-Wildeinfluss
P8-Kronenschaden
P9-Hydrologie
Fragmentierung


# Veroffentlichungen  der Karten
Nach Projektabschluss wurden die Webkarten auf der Website des NUKV Steiermark veröffentlicht:
https://www.nukv.at/riskmaps/

