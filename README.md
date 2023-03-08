# Credit_Risk_Analysis
## Overview
The objective of challenge 18 was to create a machine learning model to predict credict risk. Along the challenge, different techniques were use to train and evaluate models with unbalanceed classes (High Risk and Low Risk). Using a credict card dataset, the data was oversample using Random Oversampling and SMOTE algorithms, and undersample using Cluster Centroids algorithm. Then SMOTEENN algorithm, a combinatory approach of over- and undersampling was applied to the dataset.

After the resampling methods, two machine learning models to reduce vias were applied to the same dataset, the Balanced Random Forest Classifier and Easy Esemble Classifier, to predict the credit risk.

## Results
The analysis was divided in two parts, the resampling methods and the ensemble classifiers. In all the methods data was extracted from a csv file called "LoanStats_2019Q1.csv", filtered, splited into training and testing sets, results were predicted using a logistic regression model, and evaluated using the "balanced_accuracy_score". Furthermore, a confusion matrix and the imbalanced classification report  were created.

### Resampling Models:
Four resampling models were used along the this part: Random Oversampler, SMOTE, Cluster Centroids and SMOTEENN. 

#### Random Oversampler:
The balanced accuracy score for this resampling model was 0.6327441209976938, and the Classification Report for this model is shown in Figure 1.

![Captura de pantalla 2023-03-07 a la(s) 18 11 38](https://user-images.githubusercontent.com/93279134/223585283-f636a39a-25c1-4e42-a341-0fd724a96154.png)

Figure 1.  Random Oversampling Classification Report.

#### SMOTE Oversampler:

The balanced accuracy score for this resampling model was 0.6610201770878679, and the Classification Report for this model is shown in Figure 2.

![Captura de pantalla 2023-03-07 a la(s) 18 15 23](https://user-images.githubusercontent.com/93279134/223585797-c0e42445-1632-42ed-9536-8e1204649c93.png)

Figure 2. SMOTE Oversampling Classification Report.

#### Cluster Centroids Undersampler:

The balanced accuracy score for this resampling model was 0.5442369453268994, and the Classification Report for this model is shown in Figure 3.

![Captura de pantalla 2023-03-07 a la(s) 18 17 50](https://user-images.githubusercontent.com/93279134/223586117-d6ed6599-d2a8-492a-9a11-10a8f4146357.png)

Figure 3. Cluster Centroid Undersampling Classification Report.

#### SMOTEENN Combination Sampling:

The balanced accuracy score for this resampling model was 0.6205641202567403, and the Classification Report for this model is shown in Figure 4.

![Captura de pantalla 2023-03-07 a la(s) 18 20 44](https://user-images.githubusercontent.com/93279134/223586492-d5a39fc5-13cc-4ecb-84a3-24219eac664b.png)

Figure 4. SMOTEENN Sampling Classification Report.

### Ensemble Models:

#### Balanced Random Forest Classifier:

The balanced accuracy score for this resampling model was 0.678100890070298, and the Classification Report for this model is shown in Figure 5.

![Captura de pantalla 2023-03-07 a la(s) 18 28 56](https://user-images.githubusercontent.com/93279134/223587641-1a0e64f7-0ebd-4eff-8d13-af6f04bea9e3.png)

Figure 5. Random Forest Classifier Classification Report.

#### Easy Ensemble AdaBoost Classifier:

The balanced accuracy score for this resampling model was 0.9291943752373366, and the Classification Report for this model is shown in Figure 6.

![Captura de pantalla 2023-03-07 a la(s) 18 31 47](https://user-images.githubusercontent.com/93279134/223588008-ba26c975-cffd-434d-add6-443bdaceb0ef.png)

Figure 6. Easy Ensemble AdaBoost Classifier Classification Report.

### General Results:

After the complete analysis, in the list below the results of balanced accuracy, precision and recall, for all the methods are shown:

- Random Oversampler: Balanced_Accuracy_Score: 0.6327441209976938, Precision (High risk): 0.01, Recall (High Risk): 0.68.
- SMOTE Oversampler: Balanced_Accuracy_Score: 0.6610201770878679, Precision (High risk): 0.01, Recall (High Risk): 0.63.
- Cluster Centroids Undersampler: Balanced_Accuracy_Score: 0.5442369453268994, Precision (High risk): 0.01, Recall (High Risk): 0.69.
- SMOTEENN Combination Sampling: Balanced_Accuracy_Score: 0.6205641202567403, Precision (High risk): 0.01, Recall (High Risk): 0.69.
- Balanced Random Forest Classifier: Balanced_Accuracy_Score: 0.678100890070298, Precision (High risk): 0.90, Recall (High Risk): 0.36.
- Easy Ensemble AdaBoost Classifier: Balanced_Accuracy_Score: 0.9291943752373366, Precision (High risk): 0.09, Recall (High Risk): 0.91.

## Summary
In general terms, three scores were used to evaluate the models. Balanced Accuracy (defined as the average of recall obtained on each model), precision (defined as the likelihood that a result is actually true) and recall (define as the measure of how many of the true postives are actually classified as true). 

According to the previous definitios, recall would be the most imporant score because out of all the credit risk, it's the main objective to correctly classify those which are of high risk, so recall would give us the certanty 
