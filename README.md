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
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: VIJAYASHREE B
RegisterNumber:  212223040238
*/
~~~
import numpy as np
import matplotlib.pyplot as plt

#processing input data

X = np.array(eval(input()))
Y = np.array(eval(input()))

#mean

X_mean = np.mean(X)
Y_mean = np.mean(Y)
num =0
denom=0

#to find sum of(xi - x') & (yi -y') && (xi - x')^2

for i in range(len(X)):
    num+=(X[i] -X_mean)* (Y[i] -Y_mean)
    denom+= (X[i] - X_mean)**2
    
#to calculate slop
m= num/denom

#to calculate intercept

b=Y_mean-m*X_mean

print(m,b)

#line equation

Y_predicted= m*X+b
print(Y_predicted)

#to plot graph

plt.scatter(X,Y)
plt.plot(X,Y_predicted,color='red')
plt.show()

~~~

Output:

[Screenshot 2025-02-26 165025](https://github.com/user-attachments/assets/09163e06-2ade-4fc0-9bf2-13b1c888fd5c)

[Screenshot 2025-02-26 165312](https://github.com/user-attachments/assets/77ee3707-b407-4a79-a31b-cf7142d4c69b)

[Screenshot 2025-02-26 165137](https://github.com/user-attachments/assets/60b8224a-c5fd-441b-a59b-74deaea1d9cc)

[Screenshot 2025-02-26 165204](https://github.com/user-attachments/assets/e73fe6f5-1567-4638-9c50-6087b78e0e32)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
