Addition and Scalar Multiplication
Addition and subtraction are element-wise, so you simply add or subtract each corresponding element:

[acbd]
+
[wyxz]
=
[a+wc+yb+xd+z]
[ 
a
​	
  
bc
​	
  
d
​	
 ]+[ 
w
​	
  
xy
​	
  
z
​	
 ]=[ 
a+w
​	
  
b+xc+y
​	
  
d+z
​	
 ]
Subtracting Matrices:

[acbd]
-
[wyxz]
=
[a−wc−yb−xd−z]
[ 
a
​	
  
bc
​	
  
d
​	
 ]−[ 
w
​	
  
xy
​	
  
z
​	
 ]=[ 
a−w
​	
  
b−xc−y
​	
  
d−z
​	
 ]
To add or subtract two matrices, their dimensions must be the same.

In scalar multiplication, we simply multiply every element by the scalar value:

[acbd]
* x =
[a∗xc∗xb∗xd∗x]
[ 
a
​	
  
bc
​	
  
d
​	
 ]∗x=[ 
a∗x
​	
  
b∗xc∗x
​	
  
d∗x
​	
 ]
In scalar division, we simply divide every element by the scalar value:

[acbd]
/ x =
[a/xc/xb/xd/x]
[ 
a
​	
  
bc
​	
  
d
​	
 ]/x=[ 
a/x
​	
  
b/xc/x
​	
  
d/x
​	
 ]
Experiment below with the Octave/Matlab commands for matrix addition and scalar multiplication. Feel free to try out different commands. Try to write out your answers for each command before running the cell below.


```MATLAB
% Initialize matrix A and B 
A = [1, 2, 4; 5, 3, 2]
B = [1, 3, 4; 1, 1, 1]

% Initialize constant s 
s = 2

% See how element-wise addition works
add_AB = A + B 

% See how element-wise subtraction works
sub_AB = A - B

% See how scalar multiplication works
mult_As = A * s

% Divide A by s
div_As = A / s

% What happens if we have a Matrix + scalar?
add_As = A + s

```

Matrix-Vector Multiplication
We map the column of the vector onto each row of the matrix, multiplying each element and summing the result.

⎡⎣acebdf⎤⎦
*
[xy]
=
⎡⎣⎢a∗x+b∗yc∗x+d∗ye∗x+f∗y⎤⎦⎥
[ 
a
​	
  
bc
​	
  
de
​	
  
f
​	
 ]∗[ 
xy
​	
 ]=[ 
a∗x+b∗yc∗x+d∗ye∗x+f∗y
​	
 ]
The result is a vector. The number of columns of the matrix must equal the number of rows of the vector.

An m x n matrix multiplied by an n x 1 vector results in an m x 1 vector.

Below is an example of a matrix-vector multiplication. Make sure you understand how the multiplication works. Feel free to try different matrix-vector multiplications.




```MATLAB
% Initialize matrix A 
A = [1, 2, 3; 4, 5, 6;7, 8, 9] 

% Initialize vector v 
v = [1; 1; 1] 

% Multiply A * v
Av = A * v
```
We multiply two matrices by breaking it into several vector multiplications and concatenating the result.

⎡⎣acebdf⎤⎦
*
[wyxz]
=
⎡⎣⎢a∗w+b∗yc∗w+d∗ye∗w+f∗ya∗x+b∗zc∗x+d∗ze∗x+f∗z⎤⎦⎥
[ 
a
​	
  
bc
​	
  
de
​	
  
f
​	
 ]∗[ 
w
​	
  
xy
​	
  
z
​	
 ]=[ 
a∗w+b∗y
​	
  
a∗x+b∗zc∗w+d∗y
​	
  
c∗x+d∗ze∗w+f∗y
​	
  
e∗x+f∗z
​	
 ]
An m x n matrix multiplied by an n x o matrix results in an m x o matrix. In the above example, a 3 x 2 matrix times a 2 x 2 matrix resulted in a 3 x 2 matrix.

To multiply two matrices, the number of columns of the first matrix must equal the number of rows of the second matrix.

For example:


```MATLAB
% Initialize a 3 by 2 matrix 
A = [1, 2; 3, 4;5, 6]

% Initialize a 2 by 1 matrix 
B = [1; 2] 

% We expect a resulting matrix of (3 by 2)*(2 by 1) = (3 by 1) 
mult_AB = A*B

% Make sure you understand why we got that result
```
Matrix Multiplication Properties
Matrices are not commutative: A∗B \neq B∗AA∗B 

​	
 =B∗A
Matrices are associative: (A∗B)∗C = A∗(B∗C)(A∗B)∗C=A∗(B∗C)
The identity matrix, when multiplied by any matrix of the same dimensions, results in the original matrix. It's just like multiplying numbers by 1. The identity matrix simply has 1's on the diagonal (upper left to lower right diagonal) and 0's elsewhere.

⎡⎣100010001⎤⎦
[ 
1
​	
  
0
​	
  
00
​	
  
1
​	
  
00
​	
  
0
​	
  
1
​	
 ]
When multiplying the identity matrix after some matrix (A∗I), the square identity matrix's dimension should match the other matrix's columns. When multiplying the identity matrix before some other matrix (I∗A), the square identity matrix's dimension should match the other matrix's rows.


```MATLAB
% Initialize random matrices A and B 
A = [1,2;4,5]
B = [1,1;0,2]

% Initialize a 2 by 2 identity matrix
I = eye(2)

% The above notation is the same as I = [1,0;0,1]

% What happens when we multiply I*A ? 
IA = I*A 

% How about A*I ? 
AI = A*I 

% Compute A*B 
AB = A*B 

% Is it equal to B*A? 
BA = B*A 

% Note that IA = AI but AB != BA
```

The inverse of a matrix A is denoted A^{-1}A 
−1
 . Multiplying by the inverse results in the identity matrix.

A non square matrix does not have an inverse matrix. We can compute inverses of matrices in octave with the pinv(A)pinv(A) function and in Matlab with the inv(A)inv(A) function. Matrices that don't have an inverse are singular or degenerate.

The transposition of a matrix is like rotating the matrix 90° in clockwise direction and then reversing it. We can compute transposition of matrices in matlab with the transpose(A) function or A':

A =
⎡⎣acebdf⎤⎦
A=[ 
a
​	
  
bc
​	
  
de
​	
  
f
​	
 ]
A^T =
[abcdef]
A 
T
 =[ 
a
​	
  
c
​	
  
eb
​	
  
d
​	
  
f
​	
 ]
In other words:

A_{ij} = A^T_{ji}A 
ij
​	
 =A 
ji
T
​	
```MATLAB
% Initialize matrix A 
A = [1,2,0;0,5,6;7,0,9]

% Transpose A 
A_trans = A' 

% Take the inverse of A 
A_inv = inv(A)

% What is A^(-1)*A? 
A_invA = inv(A)*A

```




