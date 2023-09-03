# FruitClassifier

**Ziel**: Einen Klassifizierer entwerfen, der anhand der Merkmale Farbe, Größe und Gewicht die Fruchtarten Apfel, Banane, Traube einordnen kann.



## Rahmenbedingungen : 

Eine fruit_data.xlsx mit 200 Datensätzen stellt Daten bereit. Verschiedene Anforderungen sind durch die Aufgabenstellung gegeben:

- Datenverarbeitungsschritte sind nachvollziehbar
- Datenfehlern, fehlende Werte und Ausreißer werden berücksichtigt
- Die Modelle logistische Regression und Decision Tree werden benutzt
- Die Wahl der Hyperparameter ist transparent
- Die Modelle werden anhand geeigneter Metriken bewertet
- Die Dokumentation zeigt Fragestellung, Methodik und Ergebnisse auf


## Methodik

Die Anforderungen wurden auf einem GitHub Project Board zu umsetzbaren Teilaufgaben zerlegt und bestimmten Issues zugeordnet. Welche Teilaufgaben zu erledigen sind, konnte aufgrund geringer Vorkenntnisse erst während der Recherche für die nächsten Schritte bestimmt werden. Daher konnte das Projekt nicht anfangs einmal vollumfänglich geplant werden. Es wurde immer ein Issue erstellt, verschiedene Teilaufgaben festgelegt und anschließend bearbeitet. Aufgetretene Probleme sind in den Issues aufgeführt.

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
