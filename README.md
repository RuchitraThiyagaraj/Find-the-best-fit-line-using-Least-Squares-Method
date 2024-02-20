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
Developed by: RUCHITRA THIYAGARAJ
RegisterNumber:  212223110043
*/
```
import numpy as np
import matplotlib.pyplot as plt
x=np.array([0,1,2,3,4,7,6,7,9,10])
y=np.array([1,3,2,5,7,8,8,10,11,13])
xm=np.mean(x)
ym=np.mean(y)
num,den=0,0
for i in range(len(x)):
  num+=(x[i]-xm)*(y[i]-ym)
  den+=(y[i]-ym)**2
m=num/den
c=ym-m*xm
y_pred=m*x+c
print(y_pred)
plt.scatter(x,y)
plt.plot(x,y_pred,color="red")
plt.show()

## Output:
![image](https://github.com/RuchitraThiyagaraj/Find-the-best-fit-line-using-Least-Squares-Method/assets/154776996/e976a534-288e-438e-b2ca-5f8439b59894)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
