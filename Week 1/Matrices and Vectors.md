Matrices are 2-dimensional arrays:

A vector is a matrix with one column and many rows:

So vectors are a subset of matrices. 

### Notation and terms:

A vector with 'n' rows is referred to as an 'n'-dimensional vector.

In general, all our vectors and matrices will be 1-indexed. Note that for some programming languages, the arrays are 0-indexed.

Matrices are usually denoted by uppercase names while vectors are lowercase.

"Scalar" means that an object is a single value, not a vector or matrix.


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
