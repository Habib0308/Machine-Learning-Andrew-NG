Cost Function
We can measure the accuracy of our hypothesis function by using a cost function. This takes an average difference (actually a fancier version of an average) of all the results of the hypothesis with inputs from x's and the actual output y's.

J(\theta_0, \theta_1) = \dfrac {1}{2m} \displaystyle \sum _{i=1}^m \left ( \hat{y}_{i}- y_{i} \right)^2 = \dfrac {1}{2m} \displaystyle \sum _{i=1}^m \left (h_\theta (x_{i}) - y_{i} \right)^2J(θ 
0
​	
 ,θ 
1
​	
 )= 
2m
1
​	
  
i=1
∑
m
​	
 ( 
y
^
​	
  
i
​	
 −y 
i
​	
 ) 
2
 = 
2m
1
​	
  
i=1
∑
m
​	
 (h 
θ
​	
 (x 
i
​	
 )−y 
i
​	
 ) 
2
 

To break it apart, it is \frac{1}{2} 
2
1
​	
  \bar{x} 
x
ˉ
  where \bar{x} 
x
ˉ
  is the mean of the squares of h_\theta (x_{i}) - y_{i}h 
θ
​	
 (x 
i
​	
 )−y 
i
​	
  , or the difference between the predicted value and the actual value.

This function is otherwise called the "Squared error function", or "Mean squared error". The mean is halved \left(\frac{1}{2}\right)( 
2
1
​	
 ) as a convenience for the computation of the gradient descent, as the derivative term of the square function will cancel out the \frac{1}{2} 
2
1
​	
  term. The following image summarizes what the cost function does:
