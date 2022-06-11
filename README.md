# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Import pandas as pd and import the required dataset.<br>

2.Calculate the null values in the dataset.<br>

3.Import the LabelEncoder from sklearn.preprocessing.<br>

4.Convert the string values to numeric values.<br>

5.Import train_test_split from sklearn.model_selection.<br>

6.Assign the train and test dataset.<br>

7.Import DecisionTreeRegressor from sklearn.tree.<br>

8.Import metrics from sklearn.metrics.<br>

9.Calculate the MeanSquareError.<br>

10.Apply the metrics to the dataset.<br>

11.Predict the output for the required values.<br>

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: D.Amarnath Reddy.
RegisterNumber: 212221240012


import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x= data[["Position","Level"]]
y=data["Salary"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size = 0.2,random_state = 2)

from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred = dt.predict(x_test)

from sklearn import metrics
mse = metrics.mean_squared_error(y_test,y_pred)
mse

r2= metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])

*/
```

## Output:
<img width="331" alt="img 1" src="https://user-images.githubusercontent.com/94165103/173192595-1a571d5d-9267-43eb-afd9-72572c6888b2.png">

<img width="341" alt="img 2" src="https://user-images.githubusercontent.com/94165103/173192601-ac1b4156-077c-4493-bfa1-6f287d749a84.png">


<img width="365" alt="img 3" src="https://user-images.githubusercontent.com/94165103/173192609-f3035c08-52b0-4926-8dfe-0e744b65a92e.png">

<img width="343" alt="img 4" src="https://user-images.githubusercontent.com/94165103/173192615-d5c957b4-f16b-4852-9045-ccaf953a1555.png">

<img width="414" alt="img 5" src="https://user-images.githubusercontent.com/94165103/173192617-1ef44e88-a731-4098-b6fb-22abb29e9869.png">
<img width="371" alt="img 6" src="https://user-images.githubusercontent.com/94165103/173192622-5ec3e5fb-58f2-4903-a458-872a0f1ed67f.png">



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
