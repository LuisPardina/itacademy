# Repte #4 - Models de classificació
## Model Predictiu - Càncer de mama 🎗️



## Dataset Explanation

+ Target: 
The target variable to predict is "diagnosis", where "0" is benign tumor and "1" is malignant tumor

+ Features: 
The datasets contain 30 features, which are different measurements  of the tumors (dimensions smothness, texture,...). The actual measurements are 10, but they are shown for the mean, the sequence and the worst case (10 x 3 = 30). Thus, the independent variables are numerical and continuous. It has 455 records (patients) in the train dataset and 114 records in the test dataset. The datasets are clean (no Null values).


## Feature Engineering / Scaling 

+ Some variables exhibit a strong relationship with each other. To avoid the potential issues created by multicollinearity and reduce the complexity I drop "area" and "surface" variables from the dataset, since they are closely related to the radius.

+ Most of the variables show skew and outliers, then I select to scalate them prior to fit the model. I select Robust Scaler as a convenient tool in this case.

+ I don't use a PCA since despite there are many variables the total amount of data is low.


## Model Selection and fit

+ In this case, the most relevant metrics are the overall accuracy and the recall. This last one is specially important because we want to avoid False Negatives, that is, patients with a malignant tumor that is predicted as benign.

+ I test several classification models with a cross_validation score (with the standard 5 folds), to make a first selection. I make a first selection of Logistic Regression and SVC (Support Vector Classification) based in the results of the key metrics.

+ I train the two models splitting the train set into two subsets, 80% to fit the models and 20% to test the results. I present the confusion matrix obtained with the two models run over the test subset.

+ I refine the hyperparameters of both models with the help of GridSearch and train the two models over the complete train set.

+ Finally, I make the final selections. The results of the accuracy, recall, and f1_score of the two different models have been validated using **Cross Validation** and taking into account the mean and standard deviation.  A recall close to 95,3% ad a f1 close to 95,8% have been achieved.



## Results, model predict

+ I have constructed the final model using the Logistic Regression Classifier with solver = 'liblinear' (for small datasets, ‘liblinear’ is a good choice).  A csv table with the predicted results has been created.
           

