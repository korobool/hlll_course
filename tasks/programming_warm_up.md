## Python program to multiply two matrices
Given two matrices. 
The task is that we will have to create a program to multiply two matrices in python.

#### Task description:

Implement a function in Python3 that accepts two parameters, matrix X and matrix Y and returns the
result of their multiplication. 

1. [Intro to matrix multiplication](https://www.khanacademy.org/math/precalculus/precalc-matrices/multiplying-matrices-by-matrices/v/matrix-multiplication-intro)- Video
2. [Multiplying matrices](https://www.khanacademy.org/math/precalculus/precalc-matrices/multiplying-matrices-by-matrices/v/multiplying-a-matrix-by-a-matrix) - Video
3. [Multiplying matrices](https://www.khanacademy.org/math/precalculus/precalc-matrices/multiplying-matrices-by-matrices/a/multiplying-matrices) - Article
4. [Materials in other languages](https://ru.wikipedia.org/wiki/%D0%A3%D0%BC%D0%BD%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5_%D0%BC%D0%B0%D1%82%D1%80%D0%B8%D1%86)
5. [Khan Academy - matrices](https://www.khanacademy.org/math/precalculus/x9e81a4f98389efdf:matrices/x9e81a4f98389efdf:multiplying-matrices-by-matrices/v/matrix-multiplication-intro)

### Python stdlib
You can use Python itself ONLY, no numpy or other math libs. You can use: 
1. regular loops, for, while, 
2. lists, and other standard data structures in Python



Implement a function with following prototype:
```python
def matrix_dot_matrix(X, Y):
    # Here you should implement an algorithm of multiplication itself using
    # loops and lists.
    # Don't forget to check if matricies can be mutiplied or not (check shape of each matrix)
    return output_matrix
```

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

### TODO: Next Step - *Task
Python and Numpy Based Solutions Comparson:

* Do the same thing with NumPy
* Compare speed using big matrix (find big enough one to make computation run for several secconds).

