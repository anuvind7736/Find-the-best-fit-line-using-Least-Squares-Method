# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
step 1.start

step 2. Get the independent variable X and dependent variable Y.

step 3.Calculate the mean of the X -values and the mean of the Y -values.

step 4. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">

step 5.Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">

step 6. Use the slope m and the y -intercept to form the equation of the line.

step 7.Obtain the straight line equation Y=mX+b and plot the scatterplot.

step 8.end

## Program:
```

import numpy as np
import matplotlib.pyplot as plt

# preprocessing input data

X = np.array(eval(input()))
Y = np.array(eval(input()))

# Mean
X_mean =np.mean(X)
Y_mean =np.mean(Y)
num=0 #for slope
denom=0 #for slope

#to find sum of (xi-x') & (yi-y') & (xi-x')^2
for i in range(len(X)):
  num+=(X[i] -X_mean)*(Y[i]-Y_mean)
  denom+=(X[i]-X_mean)**2

#calculate slope
m=num/denom

#calculate intersept
b=Y_mean-m*X_mean

print(m,b)

#line equation
y_predicted=m*X+b
print(y_predicted)

#plot graph
plt.scatter(X,Y)
plt.plot(X,y_predicted,color='red')
plt.show()

Developed by: ANUVIND KRISHNA.K
RegisterNumber: 212223080004

```




## Output:
## SLOPE Y-INTERCEPT 
![image](https://github.com/user-attachments/assets/f79246e8-1af1-4c57-8d85-b72f8129c22c)

## Y PREDICTED
![image](https://github.com/user-attachments/assets/5af0f558-3520-4e0d-9f82-a751d5ef5ca4)

## GRAPH
![image](https://github.com/user-attachments/assets/ea81aaff-d87c-4b6d-b794-125d18503ee6)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
