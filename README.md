# Credit Card Approval prediction using ML Techniques

This project was done as a final project from my class BUAN 6341- APPLIED MACHINE LEARNING 
![image](https://user-images.githubusercontent.com/106167638/215358082-10dbec0f-618c-4ae2-a39f-7eb19778ce12.png) 
(Img source: nycdatascience.com)


Commercial banks receive a lot of applications for credit cards. Many of them get rejected for many reasons, like high loan balances, low income levels, or too many inquiries on an individual's credit report, for example. Manually analyzing these applications is mundane, error-prone, and time-consuming (and time is money!). Luckily, this task can be automated with the power of machine learning and pretty much every commercial bank does so nowadays. In this project, I will build an automatic credit card approval predictor using machine learning techniques, just like the real banks do.

TASK

Build a machine learning model to predict if an applicant is 'good' or 'bad' client, different from other tasks, the definition of 'good' or 'bad' is not given. You should use some techique, such as vintage analysis to construct you label. Also, unbalance data problem is a big problem in this task. Similarly, In our data, we had skewed target variable, so we used SMOTE to synthetically oversample the data to remove the biasness.

SMOTE stands for Synthetic Minority Oversampling Technique. SMOTE is an improved method of dealing with imbalanced data in classification problems.

CLEANING AND PREPROCESSING

Our dataset contains both numeric and non-numeric data (specifically data that are of float64, int64 and object types). The dataset also contains values from several ranges. Some features have a value range of 0 - 28, some have a range of 2 - 67, and some have a range of 1017 - 100000. Finally, the dataset has missing values, which are labeled with '?', which can be seen in the last cell.

For numeric columns, we impute the missing values with a strategy called mean imputation. For non-numeric columns the mean imputation strategy would not work. This needs a different treatment. We are going to impute these missing values with the most frequent values as present in the respective columns. This is good practice when it comes to imputing missing values for categorical data in general.

Finally, we need to convert categorical and non-categorical features because many machine learning models (like XGBoost) (and especially the ones developed using scikit-learn) require the data to be in a strictly numeric format. We will do this by using a technique called label encoding.

TRAINING AND MODEL PREDICTION

Which model should we pick? A question to ask is: are the features that affect the credit card approval decision process correlated with each other? We use a correlation technique to see if the parameters and find out a high degree of correlation. Because of this correlation, we'll take advantage of the fact that generalized linear models perform well in these cases like a Logistic Regression model.

We have tried five different classification models for our credit card approval prediction task. The train and test accuracy of the models is summarized in the Figure below. We have obtained the best test data accuracy (88%) from the Logistic Regression classifier. The small difference in train and test accuracy scores indicates the absence of overfitting and underfitting.

![image](https://user-images.githubusercontent.com/106167638/215357889-d6732472-1249-482f-ba82-1a935edfe0c6.png)







