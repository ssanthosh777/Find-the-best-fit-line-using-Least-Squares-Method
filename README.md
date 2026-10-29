# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: SANTHOSH S
RegisterNumber: 212224100052
```
```python
import numpy as np
import matplotlib.pyplot as plt

x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 5, 4, 5])

x_mean = np.mean(x)
y_mean = np.mean(y)

num = 0
denom = 0
for i in range(len(x)):
    num += (x[i] - x_mean) * (y[i] - y_mean)
    denom += (x[i] - x_mean)**2

m = num / denom
b = y_mean - m * x_mean

y_predicted = m * x + b
print(y_predicted)

print(m, b)

plt.scatter(x, y)                # Plot the actual data points
plt.plot(x, y_predicted, color='red')  # Plot the regression line
plt.show()
```

## Output:
<img width="352" height="167" alt="image" src="https://github.com/user-attachments/assets/9b3a00ec-bc49-4525-8cb4-97aedaf1013a" />
<img width="265" height="133" alt="image" src="https://github.com/user-attachments/assets/b7578597-78b9-441a-b49e-99da530e61ed" />
<img width="905" height="805" alt="image" src="https://github.com/user-attachments/assets/27cd6212-91e6-4236-9018-d139d5fa9635" />




## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
