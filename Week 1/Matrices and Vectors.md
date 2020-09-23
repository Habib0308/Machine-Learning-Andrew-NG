Matrices are 2-dimensional arrays:

⎡⎣⎢⎢⎢adgjbehkcfil⎤⎦⎥⎥⎥
[ 
a
​	
  
b
​	
  
cd
​	
  
e
​	
  
fg
​	
  
h
​	
  
ij
​	
  
k
​	
  
l
​	
 ]
The above matrix has four rows and three columns, so it is a 4 x 3 matrix.

A vector is a matrix with one column and many rows:

⎡⎣⎢⎢wxyz⎤⎦⎥⎥
[ 
wxyz
​	
 ]
So vectors are a subset of matrices. The above vector is a 4 x 1 matrix.

Notation and terms:

A_{ij}A 
ij
​	
  refers to the element in the ith row and jth column of matrix A.
A vector with 'n' rows is referred to as an 'n'-dimensional vector.
v_iv 
i
​	
  refers to the element in the ith row of the vector.
In general, all our vectors and matrices will be 1-indexed. Note that for some programming languages, the arrays are 0-indexed.
Matrices are usually denoted by uppercase names while vectors are lowercase.
"Scalar" means that an object is a single value, not a vector or matrix.
\mathbb{R}R refers to the set of scalar real numbers.
\mathbb{R^n}R 
n
  refers to the set of n-dimensional vectors of real numbers.
Run the cell below to get familiar with the commands in Octave/Matlab. Feel free to create matrices and vectors and try out different things.


```MATLAB
% The ; denotes we are going back to a new row.
A = [1, 2, 3; 4, 5, 6; 7, 8, 9; 10, 11, 12]

% Initialize a vector 
v = [1;2;3] 

% Get the dimension of the matrix A where m = rows and n = columns
[m,n] = size(A)

% You could also store it this way
dim_A = size(A)

% Get the dimension of the vector v 
dim_v = size(v)

% Now let's index into the 2nd row 3rd column of matrix A
A_23 = A(2,3)

```
