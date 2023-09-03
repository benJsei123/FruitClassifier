# FruitClassifier

**Ziel**: Klassifizierer zur Einordnung der Fruchtarten Apfel, Banane, Traube entwerfen und schließlich den best geeignetsten Klassifizierer auswählen. 

## Benutzung 
Zur Benutzung muss zuerst ``FruitClassifier/Data Cleaning/Datenaufbereitung und -bereinigung.ipynb`` ausgeführt werden. Resultat ist die Erstellung einer ``clean_data.csv`` (zur weiteren Verarbeitung) und einer ``clean_data.xlsx`` (zur Ansicht, falls gewünscht). Im zweiten Schritt muss ``Models, Training etc/Models.ipynb`` ausgeführt werden. Resultat ist die Bewertung der Modellvorhersagen innerhalb des Notebooks. 

Hinweis zu ``Models.ipynb``: Es ist zu beachten, dass bei einzelner Ausführung der Zellen die Grid Search für die Parameterfindung erst abgeschlossen sein sollte, bevor die Modelle erstellt und trainiert werden. Andernfalls werden die Modelle mit eigener Parametrisieung nicht richtig erzeugt. 

## Rahmenbedingungen 

Eine ``fruit_data.xlsx`` mit 200 Datensätzen stellt Daten bereit. Verschiedene Anforderungen sind durch die Aufgabenstellung gegeben:

- Datenverarbeitungsschritte sind nachvollziehbar
- Datenfehlern, fehlende Werte und Ausreißer werden berücksichtigt
- Die Modelle logistische Regression und Decision Tree werden benutzt
- Die Wahl der Hyperparameter ist transparent
- Die Modelle werden anhand geeigneter Metriken bewertet
- Die Dokumentation zeigt Fragestellung, Methodik und Ergebnisse auf


## Methodik

Die Anforderungen wurden auf einem GitHub Project Board zu umsetzbaren Teilaufgaben zerlegt und bestimmten Issues zugeordnet. Welche konkreten Teilaufgaben zu erledigen sind, konnte aufgrund geringer Vorkenntnisse erst während der Recherche für die nächsten Schritte bestimmt werden. Daher konnte das Projekt nicht anfangs einmal vollumfänglich geplant werden. Es wurde immer ein Issue erstellt, verschiedene Teilaufgaben festgelegt und anschließend bearbeitet. Aufgetretene Probleme sind in den Issues aufgeführt.

## Ergebnisse

In dem Notebook ``Models.ipynb`` werden unter anderem vier Modelle auf den aufbereiteten Daten trainiert:

- **Modell 1 ("``model1``")** nutzt logistische Regression und folgt einer Standard Parametrisierung
- **Modell 1 ("``model1_tuned``")** nutzt logistische Regression und wurde abweichend der Standard Parametrisierung erstellt
- **Modell 2 ("``model2``")** nutzt Decision Tree und folgt einer Standard Parametrisierung
- **Modell 2 ("``model2_tuned``")** nutzt Decision Tree und wurde abweichend der Standard Parametrisierung erstellt

Alle vier Modelle wurden mit folgenden Metriken bewertet:

- Genauigkeit / Accuracy
- F1 Score
- Verwechslungsmatrix / Confusion Matrix


Die Ergebnisse der Modelle, gemessen an den drei genannten Metriken, lassen sich am Ende des Notebooks ``Models.ipynb`` darstellen.

Die Untersuchung der Ergebnisse, lässt eine Auswahl eines besten Modells zu. Dabei werden die Ergebnisse von mehreren Trainings berücksichtigt: Das Modell 2 ("``model2_tuned``"), also Decision Tree mit eigenen Parametern, liefert in den meisten Fällen die besten Ergebnisse. 


## Beobachtungen:

- Die Wahl der Hyperparameter allein mittels Grid Search hatte tendenziell einen negativen Einfluss auf die Bewertung der Modelle. "Tendenziell" heißt, dass für die meisten Training-Testing-Durchläufe (= ein Gesamtdurchlauf des Notebooks ``Models.ipynb``) die eigens parametrisierten Modelle schlechter abschnitten. Nur manchmal waren die per Grid Search parametrisierten Modelle besser in ihren Vorhersagen. Erst durch manuelles Ausprobieren von möglichen Parameterwerten konnte bspw. für das Decision Tree Modell eine Steigerung der Genauigkeit durch Hyperparameter erreicht werden. 
- Die Klassifizierung von Trauben funktioniert für alle 4 Modell am besten (siehe Verwechslungsmatrizen in ``Models.ipynb``). Die Klassifizierung von Äpfeln und Bananen ist für alle 4 Modelle nicht besonders zuverlässig.    
