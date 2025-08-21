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
Developed by: BARATHRAJ K
RegisterNumber:  212224230033
*/
import numpy as np 
import matplotlib.pyplot as plt
x = np.array([3.6,4.8,7.2,6.9,10.7,6.1,7.9,9.5,5.4])
y = np.array([9.3,10.2,11.5,12,18.6,13.2,10.8,22.7,12.7])
ypred = 1.53*x+2.88
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print("m = ",m,",b = ",b)
ypred = m*x+b
print("ypred = ",ypred)

plt.scatter(x,y,color='Black')
plt.plot(x,ypred,color='Red')
plt.show()

```

## Output:
<img width="1130" height="949" alt="image" src="https://github.com/user-attachments/assets/f9e96ac8-e35d-49ab-87b1-53bc31ee4e21" />


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
