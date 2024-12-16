# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. import numpy as np
2. give inputs
3. Forward Elimination
4. Back Substitution
5. Output Results

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
![Screenshot 2024-12-06 130114](https://github.com/user-attachments/assets/bde7a04c-b34c-41d1-a820-bb21c4fbbca2)

![Screenshot 2024-12-06 130203](https://github.com/user-attachments/assets/42a24c34-363b-4fee-86fb-9d08e0f03f21)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

