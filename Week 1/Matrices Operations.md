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
