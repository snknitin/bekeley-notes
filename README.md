# bekeley-notes
Simon's institute lectures


## Over-parameterization

- increase the size of the hidden layer to get rid of local minima and change the loss curve.
- if your sgd is not finding a low training error, fit a more expressive model until the training error is near zero
- skip connections avoid vanishing gradients
- you make progress if the polyak gradient domination condition is met.
- avoid spurious vanishing gradients. Using second order info from Taylor series. Run sgd until your gradient vector is zero. Then compute the negative eigen vector. If it is not 0, you move in that direction and loop again. This will find a place where gradient is roughly zero and hessian is positive semi definite which is a second order stationary point, which is sort of like a local min. Third order saddle points can be escaped
-
