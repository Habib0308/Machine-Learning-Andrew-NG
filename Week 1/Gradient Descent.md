# Grradient Descent
So we have our hypothesis function and we have a way of measuring how well it fits into the data. Now we need to estimate the parameters in the hypothesis function. That's where gradient descent comes in.

Gradient descent is an optimization algorithm used to find the values of parameters (coefficients) of a function (f) that minimizes a cost function (cost). For a really detailed explaination [click here](https://machinelearningmastery.com/gradient-descent-for-machine-learning/) and for summarirzed short explaination [click here](https://ml-cheatsheet.readthedocs.io/en/latest/gradient_descent.html)

we are graphing the cost function as a function of the parameter estimates. We are not graphing x and y itself, but the parameter range of our hypothesis function and the cost resulting from selecting a particular set of parameters.


We will know that we have succeeded when our cost function is at the very bottom of the pits in our graph, i.e. when its value is the minimum.

The way we do this is by taking the derivative (the tangential line to a function) of our cost function. The slope of the tangent is the derivative at that point and it will give us a direction to move towards. We make steps down the cost function in the direction with the steepest descent. The size of each step is determined by the parameter α, which is called the learning rate.

[Nice explaination of derivative](https://www.youtube.com/watch?v=WUvTyaaNkzM&ab_channel=3Blue1Brown)

A step is determined by our parameter α. A smaller α would result in a smaller step and a larger α results in a larger step. The direction in which the step is taken is determined by the partial derivative of cost function.



## NOTE
On a side note, we should adjust our parameter alpha "α" to ensure that the gradient descent algorithm converges in a reasonable time. Failure to converge or too much time to obtain the minimum value imply that our step size is wrong.
