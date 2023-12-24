# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.first use the import statment 
2.second use the numpy operator 
3.third use the matrix function 
4.fourth I use print statment  

## Program:
```
/*
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: l.yagnesh kumar reddy
RegisterNumber: 23004742
'''
import numpy as np
import sys
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range (n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range (n):
    if matrix[i][j]==0.0:
        sys.exit("divide by zero error")
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
        print("X%d = %0.2f"%(i,x[i]),end=" ") 
*/
```

## Output:
![Screenshot 2023-12-24 201953](https://github.com/23004742/Gaussian/assets/150319318/016efe83-63c1-47ee-aa17-1e074e255928)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

