# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import required libraries (NumPy, Pandas, Matplotlib)
2. Load dataset using read_csv()
3. Extract independent variable (R&D Spend) into X
4. Extract dependent variable (Profit) into y
5. Calculate mean of X
6. Calculate standard deviation of X
7. Calculate predicted values
	​


## Program:
```
Program to implement the linear regression using gradient descent.
Developed by: K  MONISHWAR
RegisterNumber:  212225230188

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("Downloads\Startup.csv")
X=data["R&D Spend"].values
y=data["Profit"].values

X=(X-X.mean())/X.std()
m=0
b=0

learning_rate=0.01
epochs=1000
n=len(X)
for i in range(epochs):
    y_pred=m*X+b
    
    dm=(-2/n)*np.sum(X*(y-y_pred))
    db=(-2/n)*np.sum(y-y_pred)
    m=m-learning_rate*dm
    b=b-learning_rate*db
print("Slope(m):",m)
print("Intercept(b):",b)
y_pred=m*X+b

plt.scatter(X,y)
plt.plot(X,y_pred)
plt.xlabel("R&D Spend")
plt.ylabel("Profit")
plt.title("Gradient Descent on 50_Startups Dataset")
plt.show()
```

## Output:
<img width="918" height="674" alt="image" src="https://github.com/user-attachments/assets/12463207-660e-47f6-9699-f4104ec0878a" />
<img width="918" height="633" alt="image" src="https://github.com/user-attachments/assets/5442d90d-d3da-4b03-ae7f-0d117128ea7f" />


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
