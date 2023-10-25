# Loan prediction using decision tree classifier 

This report entails loan prediction using decision tree classifier. The dataset used includes the following columns and their data types: 

|Column | Data type|
|-------|----------|
|Loan_ID | object| 
|Gender | object|
|Married | object|
|Dependents|object| 
|Education |object|
|Self_Employed |object| 
|ApplicantIncome |int64| 
|CoapplicantIncome |float64| 
|LoanAmount |float64| 
|Loan_Amount_Term |float64|
|Credit_History |float64| 
|Property_Area |object| 
|Loan_Status |object| 

 

 
&nbsp;
#### Introduction: 

The goal of the project is to investigate the use of a decision tree classifier for loan prediction. This report describes the practical activities completed, with an emphasis on the proper use of dataframe functions, feature selection, LabelEncoder, and the building of a decision tree classifier. The findings, including the evaluation metrics used to assess the performance of the decision tree models, are also discussed in the report. 

  
&nbsp;
#### Data and Preprocessing: 

The dataset used contains information about loan applicants, including various attributes such as applicant income, gender, credit score, loan term, loan amount, etc. The first step involved loading the dataset into a pandas dataframe, which facilitated data manipulation and analysis. Basic dataframe functions like head(), info(), shape() and describe() were used to gain an understanding of the dataset structure and content. 

 
&nbsp;
#### Feature Selection: 

Feature selection played a crucial role in the model development. Two different sets of features were selected using different methods. In the first set, features were chosen based on their correlation with the target variable and relevance to loan prediction. The following features were used: 

- Gender, Married, Dependents, Education, Self_Employed, ApplicantIncome, CoapplicantIncome, LoanAmount, Loan_Amount_Term, Credit_History, Property_Area 

 

The second set was selected using the feature importance method available in sklearn focusing on attributes with high importance scores. This approach aimed to ensure that the models would be trained on relevant and significant features. The following features were used: 

- Married, ApplicantIncome, LoanAmount, Credit_History


&nbsp;
#### Label Encoding: 

Since decision tree classifiers work with numerical data, categorical features needed to be converted into numerical format. The LabelEncoder from the scikit-learn library was used to transform categorical variables into integer values. This process allowed the decision tree model to handle the categorical attributes effectively. 

  
&nbsp;
#### Developing Decision Tree Classifier: 

A decision tree classifier was developed using the scikit-learn library. The dataset was split into training and testing sets, with the training set used to train the model and the testing set used to evaluate its performance. The decision tree classifier was configured with default parameters, and the training data was fit to the model using the fit() function. 

  
&nbsp;
#### Feature Selection Comparison: 

Two models were trained using the two different sets of features described earlier. The models were assessed based on their recall, precision, accuracy, and F1-score. The accuracy metric measured the overall correctness of the predictions, while precision focused on the ratio of true positive predictions to the total predicted positives. Recall assessed the proportion of actual positives that were correctly predicted, and the F1-score provided a balance between precision and recall. 

  
&nbsp;
#### Results and Discussion: 

The results of the predictions show that both models performed well. The model using correlation-based and relevant features achieved an accuracy of 0.74, precision of 0.75, recall of 0.74, and F1-score of 0.74. Meanwhile, the model utilising expert-selected features achieved an accuracy of 0.80, precision of 0.84, recall of 0.80, and F1-score of 0.81. Comparing the models based on feature selection, the latter boasted higher precision, accuracy, recall and F1-score. 
