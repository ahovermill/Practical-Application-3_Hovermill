README File:

Project Objective:  

This Practical Application is to compare and evaluate the performance of four classifiers using various methods that would give insight on the right model to use for predicting the most effective marketing strategy yeilding in robust Return on Investments (ROI) for the Portuguese Bank.

Classifiers under evaluation and comparision:
1) K-Nearest Neighbors, 
2) Logistic Regression
3) Decision Trees,
4) Support Vector Machine (SVMs) 

Project Background: 
The Portuguese Bank used their own contact center to reach out directly via telephone to various clients. Even though there were two options to use (Nominal Values and Amount Invested) the bank chose to use the Nominal attribute with values enumerated for three groups; however, the bank felt it needed to use it's internal database to gain more insight on their client's characteristics.

The marketing campaign used was simply reaching out to the clients via human interaction through phones calls.  A total of 17 campaings took place between 2008 - 2010 offering deposit incentives resulting in a 8% success rate.

Project Goal:
The goal is to evaluate each model and it's performance for which the bank will use for predictions on whether a client will agree to a deposit or not agree based on the marketing strategy based on a classification prediction and model into two categories (Yes or No) 

Jupyter Notebook:
The Jupyter Notebook references each CRISP-DM Phase and illustrates various codes supporting each phase. The Jupyter Notebook clearly states the Business Problem upfront to help the reader understand the objective for this exercise. 
	Business Problem: ** It is important to understand and choose the right model as the bank wants to ensure it's Return on Investoment (ROI) for allocating the right amount of resources for the predicted marketing strategy rcommended throught thee Model Evaluation Phase.

Dataset Information:
The dataset is from the https://archive.ics.uci.edu/ml/datasets/bank+marketing ; however, the CSV file was included with the Practical Application Zip File. I have used the CSV file to load the dataset. 
The dataset includes 41188 entries and a total of 21 columns. Listed below are the column desciptions.  Note: Column 21 is the target variable. Explaination is listed below.  

Bank Client Data
1 - age (numeric)
2 - job : type of job (categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown')
3 - marital : marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)
4 - education (categorical: 'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown')
5 - default: has credit in default? (categorical: 'no','yes','unknown')
6 - housing: has housing loan? (categorical: 'no','yes','unknown')
7 - loan: has personal loan? (categorical: 'no','yes','unknown')
related with the last contact of the current campaign:
8 - contact: contact communication type (categorical: 'cellular','telephone')
9 - month: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec')
10 - day_of_week: last contact day of the week (categorical: 'mon','tue','wed','thu','fri')
11 - duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.
other attributes:
12 - campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
13 - pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
14 - previous: number of contacts performed before this campaign and for this client (numeric)
15 - poutcome: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')
social and economic context attributes
16 - emp.var.rate: employment variation rate - quarterly indicator (numeric)
17 - cons.price.idx: consumer price index - monthly indicator (numeric)
18 - cons.conf.idx: consumer confidence index - monthly indicator (numeric)
19 - euribor3m: euribor 3 month rate - daily indicator (numeric)
20 - nr.employed: number of employees - quarterly indicator (numeric)

Output variable (desired target):
The target variable is Column 21 [y]. Has the client agreed to / subcribed to a term deposit? (binary: yes or no)

Business Goal: 
### The Business Objective is to choose the right model that can be used to show valuable marketing techniques that result in successful client contact based on characteristics that will lead to a client deposit. In return this will help management allocate resource types based on the marketing campaign prediction.

Summary of Findings:
Per the exercise task, I evaluated data in the first 7 columns, encoded categorical with numerical, and ensured the target variable was transformed for classification binary.

Modeling included building a baseline accuarcy and comparing it with each model. The baseline accuracy score established resulted in: Baseline Accuracy: 0.8872394297804447.  This score provided a baseline to work from when evalating each model. As a result the Logistic Regression model performed the best with an accuarcy score of: Model     0.887346. 

Below is the accuracy score comparision of all four models:
                                                               Train Accuracy                       Test Accuracy
Model                                             
Logistic Regression                                 0.887239                               0.887594
KNN                                                          0.889182                               0.877721
Decision Tree                                           0.917970                               0.861212
SVM                                                          0.887343                               0.887513

Best Model: Logistic Regression

Grid search included finding the best hyperparameters for each model. 

Best hyperparameters for Logistic Regression:
LogisticRegression(C=0.001)

Best hyperparameters for KNN:
KNeighborsClassifier(n_neighbors=9)

Best hyperparameters for Decision Tree:
DecisionTreeClassifier(max_depth=5)

Best hyperparameters for SVM:
SVC(C=0.001, gamma=0.001)

Once the Grid Search was completed, I ran the hyperparameter of the Logistic Regression. To overfitting, I evaluated each performance metric to gain additional insight. Evaluation of performance metrics was conducted. The results are below for the Logistic Regression.

Train Accuracy: 	0.8872394297804447
Test Accuracy: 	0.8875940762320952
The model is not overfitted.

Conclusion:
The conclusion resulted in recommending the bank to use another marketing strategy based on the Logistic Regression prediction.
