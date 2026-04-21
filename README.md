# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
Step 1: Import the required libraries: NumPy, Matplotlib, and LinearRegression from Scikit-Learn.

Step 2: Create the input dataset for study hours (X) and marks (Y), then train the linear regression model using model.fit(X, Y).

Step 3: Find the slope and intercept of the regression line, accept user input for study hours, and predict the marks using model.predict().

Step 4: Plot the original data points as a scatter plot and draw the regression line using Matplotlib, then display the graph.
## Program:
```
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
Y = np.array([35, 50, 65, 70, 85])

model = LinearRegression()

model.fit(X, Y)

m = model.coef_[0]
b = model.intercept_

print("Slope (m):", m)
print("Intercept (b):", b)

x_input = float(input("Enter hours studied: "))
predicted_marks = model.predict([[x_input]])
print("Predicted Marks:", predicted_marks[0])

Y_pred = model.predict(X)

plt.scatter(X, Y, label="Actual Data")
plt.plot(X, Y_pred, label="Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression (Using sklearn)")
plt.legend()
plt.show()
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Suvetha R
RegisterNumber:  212225220113
*/
```

## Output:
![simple linear regression model for predicting the marks scored](sam.png)
<img width="723" height="746" alt="Screenshot 2026-04-21 110158" src="https://github.com/user-attachments/assets/e3dddf6b-2f5c-4042-93a6-edd0e8340733" />


## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
