# FruitClassifier (1st ever ML project)

**Aim**: Design classifiers to categorize the fruit types apple, banana, grape and finally select the most suitable classifier. 

## Usage 
To use the program, you must first run ``FruitClassifier/Data Cleaning/Data Preparation and Cleaning.ipynb``. The result is the creation of a ``clean_data.csv`` (for further processing) and a ``clean_data.xlsx`` (for viewing, if desired). In the second step, ``Models, Training etc/Models.ipynb`` must be executed. The result is the evaluation of the model predictions within the notebook. 

Note on ``Models.ipynb``: Please note that if the cells are executed individually, the grid search for parameter determination should be completed before the models are created and trained. Otherwise the models with their own parameterization will not be created correctly. 

## General conditions 

A ``fruit_data.xlsx`` with 200 data sets provides data. Various requirements are given by the task:

- Data processing steps are traceable
- Data errors, missing values and outliers are taken into account
- The logistic regression and decision tree models are used
- The choice of hyperparameters is transparent
- The models are evaluated using suitable metrics
- The documentation shows the research question, methodology and results


## Methodology

The requirements were broken down into feasible subtasks on a GitHub project board and assigned to specific issues. Due to a lack of prior knowledge, the specific subtasks to be completed could only be determined during the research for the next steps. As a result, the project could not be fully planned at the beginning. An issue was always created, various subtasks were defined and then worked on. Problems that arose are listed in the issues.

## Results

In the notebook ``Models.ipynb`` four models are trained on the prepared data:

- **Model 1 (“``model1``”)** uses logistic regression and follows a standard parameterization
- Model 1 (“``model1_tuned``”)** uses logistic regression and was created deviating from the standard parameterization
- Model 2 (“``model2``”)** uses decision tree and follows a standard parameterization
- Model 2 (“``model2_tuned``”)** uses Decision Tree and was created in deviation from the standard parameterization

All four models were evaluated with the following metrics

- Precision / Accuracy
- F1 Score
- Confusion Matrix


The results of the models, measured against the three metrics mentioned, can be seen at the end of the notebook ``Models.ipynb``.

The analysis of the results allows the selection of the best model. The results of several trainings are taken into account: Model 2 (“``model2_tuned``”), i.e. Decision Tree with its own parameters, provides the best results in most cases. 


## Observations:

- The choice of hyperparameters using Grid Search alone tended to have a negative influence on the evaluation of the models. “Tendency” means that for most training test runs (= a total run of the notebook ``Models.ipynb``) the models parameterized by the user performed worse. Only sometimes were the models parameterized by Grid Search better in their predictions. Only by manually trying out possible parameter values was it possible, for example, to increase the accuracy of the Decision Tree model using hyperparameters. 
- The classification of grapes works best for all 4 models (see confusion matrices in ``Models.ipynb``). The classification of apples and bananas is not very reliable for all 4 models.    
