# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
```
1.Import the numpy module and sys module to use the built-in functions for calculation
2.Get the size of the matrix from user and create empty matrix and vector
3.using for loop get elements for matrix and vector
4.Using another for loop to take each element in the matrix
5.solve row echelon form
6.perform back substitution
7.print the value in two decimal points
8.End the program
```
## Program:
```

Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Vasanth P
RegisterNumber: 24900136
import numpy as np
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")
```

## Output:
![alt text](image.png)
![alt text](image-1.png)
## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

