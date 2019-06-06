## Python program to multiply two matrices
Given two matrices. 
The task is that we will have to create a program to multiply two matrices in python.

#### Task description:

Implement a function in Python3 that accepts two parameters, matrix X and matrix Y and returns the
result of their multiplication. 

1. [Intro to matrix multiplication](https://www.khanacademy.org/math/precalculus/precalc-matrices/multiplying-matrices-by-matrices/v/matrix-multiplication-intro)

*. [Multiplying matrices](https://www.khanacademy.org/math/precalculus/precalc-matrices/multiplying-matrices-by-matrices/v/multiplying-a-matrix-by-a-matrix)

*. [Multiplying matrices](https://www.khanacademy.org/math/precalculus/precalc-matrices/multiplying-matrices-by-matrices/a/multiplying-matrices)


You can use Python itself ONLY, no numpy or other math libs. You can use: 
1. regular loops, for, while, 
*. lists, and other standard data structures in Python



Implement a function with following prototype:
```python
def matrix_dot_matrix(X, Y):
    # Here you should implement an algorithm of multiplication itself using
    # loops and lists.
    # Don't forget if matricies can be mutiplied or not (check shape of each matrix)
    return output_matrix
```

put this function into file ```matrix_mult_from_scratch.py```

Upload the solution


Examples:
```python
X = [[1, 7, 3],
     [3, 5, 6],
     [6, 8, 9]]

Y = [[1, 1, 1, 2],
     [6, 7, 3, 0],
     [4, 5, 9, 1]]

print(matrix_dot_matrix(X, Y))


>>> [[55, 65, 49, 5],
     [57, 68, 72, 12],
     [90, 107, 111, 21]]
```


