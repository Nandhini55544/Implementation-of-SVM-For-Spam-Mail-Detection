# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Start the Program.
2.Import the necessary packages.
3.Read the given csv file and display the few contents of the data.
4.Assign the features for x and y respectively.
5.Split the x and y sets into train and test sets.
6.Convert the Alphabetical data to numeric using CountVectorizer.
7.Predict the number of spam in the data using SVC (C-Support Vector Classification) method of SVM (Support vector machine) in sklearn library.
8.Find the accuracy of the model.
9.End the Program. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Nandhini M
RegisterNumber:  212224040211
import pandas as pd

data=pd.read_csv("spam.csv",encoding="Windows-1252")

data.head()

data.info()

data.isnull().sum()

x=data["v1"].values
y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
*/
```

## Output:
![image](https://github.com/user-attachments/assets/5d133955-05b0-4733-847f-6eb98d32bd6e)
![image](https://github.com/user-attachments/assets/195d320d-98f3-411c-b717-e3e8da460bbb)
![image](https://github.com/user-attachments/assets/f3fafa2c-d3ae-478a-9bd4-946e863214c3)
![image](https://github.com/user-attachments/assets/873dba3c-fedc-437c-bcb4-9fd9eccce185)
![image](https://github.com/user-attachments/assets/2a6ee4da-7932-47f0-a5cc-1c8ab5f1536c)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
