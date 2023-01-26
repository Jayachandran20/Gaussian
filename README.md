# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.import the numpy module to use the built-in functions for calculation
2.Prepare the lists from each linear equations and assign in np.array()
3.Using the np.zeros(), we can find the solutions.
4.End the program
Program:

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: M.Jayachandran
RegisterNumber: 22008847
*/
```
```
import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        arr[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=arr[j][i]/arr[i][i]
        for k in range(n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
x[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=arr[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-arr[i][j]*x[j]
    x[i]=x[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")   #X0 = 53.35 X1 = -8.88 X2 = -4.40
```

## Output:

![gaussian](https://user-images.githubusercontent.com/118447015/212352434-6e7e4e1d-6e97-408b-9db3-8c81c245121e.png)




## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

