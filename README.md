# Implementation-of-Logistic-Regression-Using-Gradient-Descent

## AIM:
To write a program to implement the the Logistic Regression Using Gradient Descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
step 0:start 

step 1.Import the data file and import numpy, matplotlib and scipy.

step 2.Visulaize the data and define the sigmoid function, cost function and gradient descent.

step 3.Plot the decision boundary .

step 4.Calculate the y-prediction.

step 5.stop
## Program:
```
/*
Program to implement the the Logistic Regression Using Gradient Descent.
Developed by: M.ARJUN
RegisterNumber: 212222040012

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
dataset=pd.read_csv("Placement_Data.csv")
dataset

dataset=dataset.drop('sl_no',axis=1)
dataset=dataset.drop('salary',axis=1)

dataset["gender"]=dataset["gender"].astype('category')
dataset["ssc_b"]=dataset["ssc_b"].astype('category')
dataset["hsc_b"]=dataset["hsc_b"].astype('category')
dataset["degree_t"]=dataset["degree_t"].astype('category')
dataset["workex"]=dataset["workex"].astype('category')
dataset["specialisation"]=dataset["specialisation"].astype('category')
dataset["status"]=dataset["status"].astype('category')
dataset["hsc_s"]=dataset["hsc_s"].astype('category')
dataset.dtypes

dataset["gender"]=dataset["gender"].cat.codes
dataset["ssc_b"]=dataset["ssc_b"].cat.codes
dataset["hsc_b"]=dataset["hsc_b"].cat.codes
dataset["degree_t"]=dataset["degree_t"].cat.codes
dataset["workex"]=dataset["workex"].cat.codes
dataset["specialisation"]=dataset["specialisation"].cat.codes
dataset["status"]=dataset["status"].cat.codes
dataset["hsc_s"]=dataset["hsc_s"].cat.codes
dataset

x=dataset.iloc[:, :-1].values
y=dataset.iloc[: ,-1].values
y

theta=np.random.randn(x.shape[1])
Y=y
def sigmoid(z):
    return 1/(1+np.exp(-z))

def loss(theta,x,Y):
      h=sigmoid(x.dot(theta))
      return -np.sum(y*np.log(h)+(1-y)*np.log(1-h))
def gradient_descent(theta,x,Y,alpha,num_iterations):
    m=len(y)
    for i in range(num_iterations):
        h=sigmoid(x.dot(theta))
        gradient=x.T.dot(h-y)/m
        theta-=alpha * gradient
    return theta

theta=gradient_descent(theta,x,Y,alpha=0.01,num_iterations=1000)

def predict(theta,x):
    h=sigmoid(x.dot(theta))
    y_pred=np.where(h>=0.5,1,0)
    return y_pred
y_pred=predict(theta,x)

accuracy=np.mean(y_pred.flatten()==Y)
print("Accuracy:",accuracy)

print(y_pred)
print(y)

xnew=np.array([[0,87,0,95,0,2,78,2,0,0,1,0]])
y_prednew=predict(theta,xnew)
print(y_prednew)

xnew=np.array([[0,0,0,0,0,2,8,2,0,0,1,0]])
y_prednew=predict(theta,xnew)
print(y_prednew)

*/
```

## Output:
![image](https://github.com/ARJUN19122004/-Implementation-of-Logistic-Regression-Using-Gradient-Descent/assets/119429483/04081b8f-1bdf-45da-8309-b448ff876d16)
![image](https://github.com/ARJUN19122004/-Implementation-of-Logistic-Regression-Using-Gradient-Descent/assets/119429483/7c6baca2-7393-458e-a884-4978fb80e3ad)
![image](https://github.com/ARJUN19122004/-Implementation-of-Logistic-Regression-Using-Gradient-Descent/assets/119429483/5a384226-2ec4-4de4-b443-4ab582ca4f8b)
![image](https://github.com/ARJUN19122004/-Implementation-of-Logistic-Regression-Using-Gradient-Descent/assets/119429483/f8e30592-be3f-41b8-8939-08d2a35cff8f)
![image](https://github.com/ARJUN19122004/-Implementation-of-Logistic-Regression-Using-Gradient-Descent/assets/119429483/d11e4a1f-31cc-4c11-9a92-3476263b2974)




## Result:
Thus the program to implement the the Logistic Regression Using Gradient Descent is written and verified using python programming.

