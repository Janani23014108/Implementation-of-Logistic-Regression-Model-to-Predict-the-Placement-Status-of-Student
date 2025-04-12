# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import necessary libraries (pandas, LabelEncoder, train_test_split, etc.).
2. Load the dataset using pd.read_csv().
3. Create a copy of the dataset and drop unnecessary columns (sl_no, salary).
4. Check for missing and duplicate values using isnull().sum() and duplicated().sum().
5. Encode categorical variables using LabelEncoder() to convert them into numerical values.

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: J.JANANI
RegisterNumber: 212223230085

import pandas as pd
pf=pd.read_csv("Placement_Data.csv")
pf.head()
pf1=pf.copy()
pf1=pf1.drop(['sl_no','salary'],axis=1)
pf1.head()
pf1.isnull().sum()
pf1.duplicated().sum()
x=pf1.iloc[:,:-1]
x
y=pf1["status"]
y
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.metrics import accuracy_score,confusion_matrix,classification_report
accuracy=accuracy_score(y_test,y_pred)
accuracy
confusion=confusion_matrix(y_test,y_pred)
confusion
classification=classification_report(y_test,y_pred)
print(classification)
lr.predict([[1,80,1,9,1,1,90,1,0,85,1,85]])
 
*/
```

## Output:
![the Logistic Regression Model to Predict the Placement Status of Student](sam.png)







## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
