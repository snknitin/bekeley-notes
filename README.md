# bekeley-notes
Simon's institute lectures



## Generalization

* **Statistical Learning Theory** : 

Predict an outcome y from a set of possible outcomes Y, on the basis of some obsercvation x from a features space X. Choose a function f(x)=y. To define the notion of a good prediction we define a loss function. We can assume that there is a probability distribution onn X * Y and the pairs of (x,y) are chosen independently according to P.The aim is to choose f with small risk such that the L(f) = E{l(f(x),y)}. the data set has to be an IID drawn from this population and same goes for the test set.

Why not estimate the underlying probability P(Y|X) distribution first? This is harder than prediction. The goals are in terms of unknown quantities related to unknown P and we have to use empirical data instead.  

* **Prior Knowledge**

There are 2 ways to introduce the domain knowledge about the problem so that we are better than random chance and converge fast with lesser samples than infinity.
  * Assumptions on the distribution P (e.g. margin, smoothness of the regression function, etc) 
  * Redefine the goal to perform as well as a reference set F of predictors where F encapsulates our inductive bias.



## Over-parameterization

- increase the size of the hidden layer to get rid of local minima and change the loss curve.
- if your sgd is not finding a low training error, fit a more expressive model until the training error is near zero
- skip connections avoid vanishing gradients
- you make progress if the polyak gradient domination condition is met.
- avoid spurious vanishing gradients. Using second order info from Taylor series. Run sgd until your gradient vector is zero. Then compute the negative eigen vector. If it is not 0, you move in that direction and loop again. This will find a place where gradient is roughly zero and hessian is positive semi definite which is a second order stationary point, which is sort of like a local min. Third order saddle points can be escaped
-
