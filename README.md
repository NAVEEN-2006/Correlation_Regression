# Correlation and regression for data analysis
### Developed by : NAVEEN KUMAR S
### Register number : 212223040129
# Aim : 

To analyse given data using coeffificient of correlation and regression line
![image](https://github.com/NAVEEN-2006/Correlation_Regression/assets/152067648/bca53956-57e5-4050-a7c1-f40296f11dad)



# Software required :  

##### Python

# Theory:

Correlation describes the strength of an association between two variables, and is completely symmetrical, the correlation between A and B is the same as the correlation between B and A. However, if the two variables are related it means that when one changes by a certain amount the other changes on an average by a certain amount.  

If y represents the dependent variable and x the independent variable, this relationship is described as the regression of y on x. The relationship can be represented by a simple equation called the regression equation. The regression equation representing how much y changes with any given change of x can be used to construct a regression line on a scatter diagram, and in the simplest case this is assumed to be a straight line.

# Procedure :

![image](https://github.com/NAVEEN-2006/Correlation_Regression/assets/152067648/ef8a1314-67ba-43e2-8a71-152e1ea05f22)


# Program :
```
import numpy as np
import math
import matplotlib.pyplot as plt
x=[ int(i) for i in input().split()]
y=[ int(i) for i in input().split()]
N=len(x)
Sx=0
Sy=0
Sxy=0
Sx2=0
Sy2=0
for i in range(0,N):
    Sx=Sx+x[i]
    Sy=Sy+y[i]
    Sxy=Sxy+x[i]*y[i]
    Sx2=Sx2+x[i]**2
    Sy2=Sy2+y[i]**2
r=(N*Sxy-Sx*Sy)/(math.sqrt(N*Sx2-Sx**2)*math.sqrt(N*Sy2-Sy**2))
print("The Correlation coefficient is %0.3f"%r)
byx=(N*Sxy-Sx*Sy)/(N*Sx2-Sx**2)
xmean=Sx/N
ymean=Sy/N
print("The Regression line Y on X is ::: y = %0.3f + %0.3f (x-%0.3f)"%(ymean,byx,xmean))
plt.scatter(x,y)
def Reg(x):
  return ymean + byx*(x-xmean)
x=np.linspace(20,80,51)
y1=Reg(x)
plt.plot(x,y1,'r')
plt.xlabel('x-data')
plt.ylabel('y-data')
plt.legend(['Regression Line','Data points'])
```

# Output:
![image](https://github.com/NAVEEN-2006/Correlation_Regression/assets/152067648/93636d04-f7a2-4552-9bc7-3839aaebef0a)

![image](https://github.com/NAVEEN-2006/Correlation_Regression/assets/152067648/0a0e1ee4-d56c-42ed-8625-5dc34cc1328e)



# Result:

The Correlation and regression for data analysis of objects from feeder using probability distribution are calculated.
