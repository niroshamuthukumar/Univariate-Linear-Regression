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
##Developed by: Nirosha M
##register Num: 23014438

import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input()))
y=np.array(eval(input()))
xmean=np.mean(X)
ymean=np.mean(y)
num,den=0,0
for i in range(len(X)):
    num+=(X[i]-xmean)*(y[i]-ymean)
    den+=(X[i]-xmean)**2
m=num/den
c=ymean-m*xmean
print(m,c)
y_pred=m*X+c
print(y_pred)
plt.scatter(X,y)
plt.plot(X,y_pred,color="red")
plt.show()
```
## Output
![WhatsApp Image 2023-12-27 at 20 39 37_f399f535](https://github.com/niroshamuthukumar/Univariate-Linear-Regression/assets/151830921/6012f218-7e69-4b3c-a512-f1b1b053797a)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
