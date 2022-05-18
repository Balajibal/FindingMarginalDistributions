Marginal distributions and correation coefficient
Aim :
To find marginal distributions and correation coefficient of joint probability mass funcition of two dimensional random variables

image

Software required :
Python

Theory:
A marginal distribution is a distribution of values for one variable that ignores a more extensive set of related variables in a dataset. The marginal mass function for X is found by summing over the appropriate column and the marginal mass function for Y can be found be summing over the appropriate row.

Correlation coefficients are indicators of the strength of the linear relationship between two different variables. The coefficient of correlation is measure of degree of realtionship betwen two variavbles. A linear correlation coefficient that is greater than zero indicates a positive relationship. A value that is less than zero signifies a negative relationship. Finally, a value of zero indicates no relationship between the two variables x and y.

Procedure :
image

Program
#Developed By : Lokesh Krishnaa  M
#Register No: 212220230030

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
Output :
Screenshot (2) Screenshot (3)

Result :
Thus the marginal distributions and correation coefficient of joint probability mass function for the problem is found.
