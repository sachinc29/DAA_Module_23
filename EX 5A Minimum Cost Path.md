
# EX 5A Minimum Cost Path

## AIM:

To write a Python program using A Naive recursive implementation of Minimum Cost Path Problem.

## Algorithm

1. Read input values R and C.

2. Define a 3x3 cost matrix.

3. Define a recursive function minCost(cost, m, n):

4. If m < 0 or n < 0: return a large number.

5. If m == 0 and n == 0: return cost[0][0].

6. Else: return cost[m][n] + min(minCost from left, top, and diagonal).

7. Call minCost(cost, R-1, C-1) and print the result.

## Program:
```
A program to implement to find the Minimum Cost Path Problem using a  Naive recursive Approach.

Developed by: Sachin C
Register Number: 212222230125
```
```python
R = int(input())
C = int(input())
import sys
def minCost(cost, m, n):
    if (n < 0 or m < 0):
        return sys.maxsize
    elif (m == 0 and n == 0):
        return cost[m][n]
    else:
        return cost[m][n] + min( minCost(cost, m-1, n-1),
                                minCost(cost, m-1, n),
                                minCost(cost, m, n-1) )
def min(x, y, z):
    if (x < y):
        return x if (x < z) else z
    else:
        return y if (y < z) else z
cost= [ [1, 2, 3],
        [4, 8, 2],
        [1, 5, 3] ]
print(minCost(cost, R-1, C-1))
```

## Output:

![image](https://github.com/user-attachments/assets/f214044e-59d6-43be-a5de-c82aba17c39a)


## Result:
Thus the above program was executed successfully for finding the minimum cost.
