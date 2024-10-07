# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

step 1 .Start the program.

step 2 - Get the independent variable X and dependent variable Y.

step 3 - Calculate the mean of the X -values and the mean of the Y -values.

step 4 - Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">



step 5  - Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">



step 6 - Use the slope m and the y -intercept to form the equation of the line.

step 7 - Obtain the straight line equation Y=mX+b and plot the scatterplot.

step 8 - Stop.

## Program:
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: ANUVIND KRISHNA 
RegisterNumber:  212223080004
*/
import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
Xmean=np.mean(X)
Ymean=np.mean(Y)
num,den=0,0 # num = numerator, den = denomenator
for i in range(len(X)):
  num+=(X[i]-Xmean)*(Y[i]-Ymean)
  den+=(X[i]-Xmean)**2
m=num/den
c=Ymean-m*Xmean
print(m,c)
Y_pred=m*X+c
print(Y_pred)
plt.scatter(X,Y)
plt.plot(X,Y_pred,color="red")
plt.show()

## Output:
SLOPE Y INTERCEPT :

![image](https://github.com/user-attachments/assets/c0864ea1-f5bb-4b60-96d1-68866b7be8b8)

Y PREDICT :

![image](https://github.com/user-attachments/assets/30c84765-b027-4e00-8966-db4838c20387)

GRAPH:

![image](https://github.com/user-attachments/assets/a087d5bb-20ad-4f1c-90df-a26830a74e97)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
