# **PHASE 3 CLASSIFICATION PROJECT by Benbellah Owino**

## **1. Business Understanding**<hr>

### *Business problem*<br>
Our client, Mouz Bank, want's a model to easen the loan approval process. We will be using the model below to build a model that fulfil's the clients wishes.<br><br>

### ***Objectives***
We want a model that satisfies the following thresholds
1. Minimum  f1 score of 90%
2. Recall  f1 score of 90%
3. Minimum  precision score of 90%

We have very high thresholds because the model will operate in a high risk high reward environment so we want to minimize the former while maximize the latter. Anything less than that is as good as useless

## **2. Data understanding**
The loan approval dataset is a collection of financial records and associated information used to determine the eligibility of individuals or organizations for obtaining loans from a lending institution. It includes various factors such as cibil score, income, employment status, loan term, loan amount, assets value, and loan status. This dataset is commonly used in machine learning and data analysis to develop models and algorithms that predict the likelihood of loan approval based on the given features.

*Source*<br>
https://www.kaggle.com/datasets/architsharma01/loan-approval-prediction-dataset


## **3. Data preparation**n 
Our data set is already cleaned so there is no need for much cleaning and preparation although I got to do the following:
* We drop the 'loan_id' column since it has no use for modeling and in my opinion is "noise" in this context.
* Convert the "loan_status" to boolean where approved == True and rejected == false
* During modelling we encode categorical data using a technique called OneHotEncoding.
* In the Base Model(Logistic Regression) I standadized the numerical columns using the sklearn Standard Scaler.
  

## **4. Modeling**
We essentially did modelling 3 times in this section
i). The Base model is a Logistic Regression model
ii). The second model is a Decision Tree Classifier.
iii). The third time we did a cross evaluation using grid search to find the best possible model from multiple hyperparameters.


## **5. Evaluation**
We created funcitions that print our evaluation reports with multiple metrics like R2 Score, Accuracy, MAE, RMSE and the most important ones for our tasks like precision, recall and f1-score.
We also used confusion matrices to look at the output of our model.

## **6. Conclusion**
* We will deploy the third model since in my opinion it perfoms the best according to the metrics and meets all our objectives. 
* The model will do well to maximize revenue and customer satisfication due to the reason above.