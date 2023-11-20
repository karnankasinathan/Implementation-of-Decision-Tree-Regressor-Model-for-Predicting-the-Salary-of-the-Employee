# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the libraries and read the data frame using pandas.
2. Calculate the null values present in the dataset and apply label encoder.
3. Determine test and training data set and apply decison tree regression in dataset.
4. calculate Mean square error,data prediction and r2.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: karnan k
RegisterNumber:  212222230062
*/
import pandas as pd
data=pd.read_csv("Salary.csv")
...
data.head()
...
data.info()
...
data.isnull().sum()
...
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
....
data.head()
..
x=data[["Position","Level"]]
x.head()
y=data[["Salary"]]
...
.
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])

## Output:
### data.head()
![image](https://github.com/karnankasinathan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118787064/dfed050f-4131-4eb4-aede-6f5c66e98966)

### data.info()
![image](https://github.com/karnankasinathan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118787064/51d08e5c-7125-4c46-bef4-fa9d457ad1fb)

### isnull() and sum()
![image](https://github.com/karnankasinathan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118787064/f0f9030c-f7c2-4bfd-ba32-9b9b6b43a6f0)

### data.head() for salary
![image](https://github.com/karnankasinathan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118787064/2f037c8e-5c34-428e-a60d-92fa7d5e7693)

### MSE value
![image](https://github.com/karnankasinathan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118787064/a0d7a13b-85b8-433f-a681-8f7501014942)

### R2 value
![image](https://github.com/karnankasinathan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118787064/bfa06429-77a5-4e8d-b195-b69bedea8dac)

### prediction value
![image](https://github.com/karnankasinathan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118787064/1fffc1d3-af8b-4b11-aefc-3bb4a52fd5c7)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
