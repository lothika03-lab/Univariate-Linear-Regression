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
x=np.array([0,1,2,3,4,5,6,7,8,9])
y=np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()


x_mean=np.mean(x)
y_mean=np.mean(y)
num=0
den=0
for i in range(len(x)):
num+=(x[i]-x_mean)*(y[i]-y_mean)
den+=(x[i]-x_mean)**2
m=num/den
c=y_mean-m*x_mean
print(m,c) 



y_pred=m*x+c
print(y_pred)
plt.scatter(x,y)
plt.plot([min(x),max(x)],[min(y_pred),max(y_pred)],color='red')
plt.show() 

```
## Output
```
<img width="935" height="553" alt="527911009-41472154-5200-4752-af1d-3d8d503abde3" src="https://github.com/user-attachments/assets/7c871930-3415-4377-97be-ba052686890f" />
<img width="928" height="581" alt="527910990-fdb93594-0194-4965-89a2-cd26c15387d8" src="https://github.com/user-attachments/assets/47db54a9-f6a1-4924-809a-69934680bbc9" />
```
## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
