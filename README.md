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
#Preprocessing Input data
X=np.array([0,1,2,3,4,5,6,7,8,9])
Y=np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(X,Y)
plt.show()
```

## Output
<img width="729" height="544" alt="image" src="https://github.com/user-attachments/assets/7826d03c-8720-4fa8-bd60-d246db9f644b" />
## Program
```
#Building the model
X_mean=np.mean(X)
Y_mean=np.mean(Y)
num=0
den=0
for i in range(len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    den+=(X[i]-X_mean)**2
m=num/den
c=Y_mean-m*X_mean
print(m,c)
```
## Output
1.1696969696969697 1.2363636363636363

## Program
```
#Making predictions
Y_pred=m*X + c
print(Y_pred)
plt.scatter(X,Y) #actual
#plt.scatter(X,Y_pred,color='red')
plt.plot([min(X),max(X)], [min(Y_pred),max(Y_pred)],color='red') #predicted
plt.show()

```
## Output
[ 1.23636364  2.40606061  3.57575758  4.74545455  5.91515152  7.08484848  8.25454545  9.42424242 10.59393939 11.76363636]
  <img width="773" height="528" alt="image" src="https://github.com/user-attachments/assets/545cd4b1-8fa5-491a-aa35-bb49f732eee6" />

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
