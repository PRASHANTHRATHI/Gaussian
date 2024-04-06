# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. First,we want to import numpy,then import sys,assume a variable.
2. For gaussian elimination method, we want to make 2nd and 3rd column zero.
3. For that we want to make a range accorting to our program output.
4. Then print the program with correct form then the output will display.

## Program:
```
Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Prashanth.K
RegisterNumber:212223230152 

import numpy as np
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=int(input())
        
for i in range(n):
    for j in range(i+1,n):
        ratio = a[j][i]/a[i][i]
        
        for k in range(n+1):
            a[j][k] = a[j][k] - ratio * a[i][k]
        
x[n-1]=a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
        
    x[i]=x[i]/a[i][i]
    
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]), end = ' ')
```

## Output:
![Screenshot 2024-04-06 144203](https://github.com/PRASHANTHRATHI/Gaussian/assets/145743120/aa10f641-3c0e-4af6-9217-22d712d4a331)
![Screenshot 2024-04-06 144216](https://github.com/PRASHANTHRATHI/Gaussian/assets/145743120/031984cc-feef-4369-a5f7-8405fa8155f0)
![Screenshot 2024-04-06 144309](https://github.com/PRASHANTHRATHI/Gaussian/assets/145743120/e03b3449-b998-46af-9965-9051e129e92b)




## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

