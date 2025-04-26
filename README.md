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
data=pd.read_csv("Placement_Data.csv") data.head()
data1=data.copy() data1=data1.drop(["sl_no","salary"],axis=1)#Browses the specified row or column data1.head()

data1.isnull().sum()

data1.duplicated().sum()

from sklearn.preprocessing import LabelEncoder le=LabelEncoder() data1["gender"]=le.fit_transform(data1["gender"]) data1["ssc_b"]=le.fit_transform(data1["ssc_b"]) data1["hsc_b"]=le.fit_transform(data1["hsc_b"]) data1["hsc_s"]=le.fit_transform(data1["hsc_s"]) data1["degree_t"]=le.fit_transform(data1["degree_t"]) data1["workex"]=le.fit_transform(data1["workex"]) data1["specialisation"]=le.fit_transform(data1["specialisation"] )
data1["status"]=le.fit_transform(data1["status"])
data1

x=data1.iloc[:,:-1] x y=data1["status"] y

from sklearn.model_selection import train_test_split x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.linear_model import LogisticRegression lr=LogisticRegression(solver="liblinear") lr.fit(x_train,y_train) y_pred=lr.predict(x_test) y_pred

from sklearn.metrics import accuracy_score accuracy=accuracy_score(y_test,y_pred) accuracy

from sklearn.metrics import confusion_matrix confusion=confusion_matrix(y_test,y_pred) confusion

from sklearn.metrics import classification_report classification_report1 = classification_report(y_test,y_pred)

print(classification_report1) lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])

```

## Output:

## DATA HEAD

![427432763-f1f948cd-7a83-46ac-bc24-eb4d1ca10bbb](https://github.com/user-attachments/assets/a329b96b-3ce3-44aa-b68e-b345bc2b77ae)

![427432686-1aa2c32b-f6f2-4fa9-8286-24e18d190fdc](https://github.com/user-attachments/assets/03d1e411-7a47-42bf-8b57-d8e6aa89cf12)


## ISNULL().SUM()

![427432891-9499215e-6483-4041-9bb6-ab8f96cdccba](https://github.com/user-attachments/assets/e8e850d3-1c06-4b92-bfec-ea76a5e365a9)

## DATA DUPLICATE

![427432997-c7387294-2a85-40e8-aaf6-7cbecdba7232](https://github.com/user-attachments/assets/c5cc73d3-5e3d-4303-8388-f77ed487c197)

## PRINT DATA

![427433144-97a37dfb-5e22-47ac-a358-a3c0674842ff](https://github.com/user-attachments/assets/f96efe64-ae63-4560-98e7-9ab20ec755f3)

## STATUS

![427433249-0972b01c-40fc-4f97-9e06-b189f0e8a8e1](https://github.com/user-attachments/assets/20992b29-8968-47c9-b770-d0d38a5e0931)

## Y_PRED

![427433338-716c6219-7077-4115-99ff-6371608feb53](https://github.com/user-attachments/assets/c65e081f-4625-4da7-a88d-a7ab5acc2a2a)

## ACCURACY

![427433432-c03dbc91-7981-42bd-b68c-cb618d8aaae9](https://github.com/user-attachments/assets/542e600c-dc27-4dbf-83dd-7f5211db6ae3)

## CONFUSION MATRIX

![427433515-6068d2d9-ee59-4cf5-bf58-7ba07b351fad](https://github.com/user-attachments/assets/6ca8c2e8-12e8-4f79-87a1-753d47379f43)

## CLASSIFICATION

![427433603-8d0529ac-9d5f-4fa6-9ce5-6f23bced3436](https://github.com/user-attachments/assets/36e9be46-56ae-42f0-808b-5da5f8accf44)


## LR PREDICT

![427433917-e73d7d65-82f3-4c48-886d-235a17a90913](https://github.com/user-attachments/assets/935a70f0-0832-4a9f-898f-b7eb7ef680b5)




## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
