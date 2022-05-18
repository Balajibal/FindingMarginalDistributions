# EXP. NO: 03

# DATE :

# <p align = "center"> Marginal distributions and correation coefficient </p>


# Aim : 

To find marginal distributions and correation coefficient of joint probability mass funcition of two dimensional random variables

![image](https://user-images.githubusercontent.com/104613195/168222062-bb7dec1f-f115-4669-8b4c-58283af8ccf3.png)

# Software required :  

Python

# Theory:

A marginal distribution is a distribution of values for one variable that ignores a more extensive set of related variables in a dataset.
The marginal mass function for X is found by summing over the appropriate column and the marginal mass function
for Y can be found be summing over the appropriate row.

Correlation coefficients are indicators of the strength of the linear relationship between two different variables. The coefficient of correlation is measure of degree of realtionship betwen two variavbles. A linear correlation coefficient that is greater than zero indicates a positive relationship. A value that is less than zero signifies a negative relationship. Finally, a value of zero indicates no relationship between the two variables x and y.  



# Procedure :
![image](https://user-images.githubusercontent.com/104613195/168220332-09383cb4-a7ac-4526-b547-fc522ca53227.png)



# Program

```python
#Developed By : BALAJI N
#Register No: 212220230006

import numpy as np
import math
p=[[0,0.01,0.03,0.05,0.07,0.09],
  [0.01,0.02,0.04,0.05,0.06,0.08],
  [0.01,0.03,0.05,0.05,0.05,0.06],
  [0.01,0.02,0.04,0.06,0.06,0.05]]
px=np.sum(p,axis=0)
px
py=np.sum(p,axis=1)
py
x=[0,1,2,3,4,5]
ex=np.inner(x,px)
ex
y=[0,1,2,3]
ey=np.inner(y,py)
ey
ex2=np.inner(np.square(x),px)
ex2
ey2=np.inner(np.square(y),py)
ey2
vx=ex2-ex**2
sx=math.sqrt(vx)
vx
vy=ey2-ey**2
sy=math.sqrt(vy)
vy
exy=0
for i in range(6):
    for j in range(4):
        exy=exy+x[i]*y[j]*p[j][i]
exy
cov=exy-ex*ey
r=cov/(sx*sy)

```


<br># Output :</br> 

![Screenshot (143)](https://user-images.githubusercontent.com/75234946/168963280-37e67d86-8eac-4123-b290-6d1c1cfa3b95.png)
![Screenshot (144)](https://user-images.githubusercontent.com/75234946/168963331-1eb4da02-9330-481b-910a-4bb07c1bc091.png)
![Screenshot (145)](https://user-images.githubusercontent.com/75234946/168963379-530344b2-d705-4ad7-a6d0-9049a4ca5261.png)



# Result :
Thus the marginal distributions and correation coefficient of joint probability mass function for the problem is found.
