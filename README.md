# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
import numpy as np
import matplotlib.pyplot as plt

# Step 1: Input data
X = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
Y = np.array([1, 3, 2, 5, 7, 8, 8, 9, 10, 12])

# Step 2: Plot original data
plt.scatter(X, Y)
plt.title("Original Data")
plt.xlabel("X")
plt.ylabel("Y")
plt.show()

# Step 3: Calculate mean
X_mean = np.mean(X)
Y_mean = np.mean(Y)

# Step 4: Calculate slope (m) and intercept (c)
num = 0
den = 0

for i in range(len(X)):
    num += (X[i] - X_mean) * (Y[i] - Y_mean)
    den += (X[i] - X_mean) ** 2

m = num / den
c = Y_mean - m * X_mean

print("Slope (m) =", m)
print("Intercept (c) =", c)

# Step 5: Prediction
Y_pred = m * X + c

print("Predicted values:")
print(Y_pred)

# Step 6: Plot regression line
plt.scatter(X, Y, label="Actual")
plt.plot(X, Y_pred, color="red", label="Regression Line")
plt.title("Linear Regression")
plt.xlabel("X")
plt.ylabel("Y")
plt.legend()
plt.show()

```
## Output
<img width="1425" height="817" alt="image" src="https://github.com/user-attachments/assets/a23bc812-17ad-403d-bac9-a9c5b55cb4a1" />
<img width="1426" height="813" alt="image" src="https://github.com/user-attachments/assets/b5388b05-d847-446d-b072-8307e077146b" />
<img width="1427" height="815" alt="image" src="https://github.com/user-attachments/assets/07ccc7c9-9faf-42c6-bb07-4eee4222359b" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
