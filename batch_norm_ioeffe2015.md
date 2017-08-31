# Batch Normalization: Accelerating Deep Network Training by Reducing Internal Covariate Shift

* **Internal covariate shift:** The task of a layer is to take the output of the previous layer and transform it into the input of the next layer. However, as the weights of the previous layer are trained, the distribution of its outputs also changes. Therefore, the distribution of the inputs of a hidden layer changes during training and the network must adapt to that.

* **Parameters**: There are two learned parameters for each features: gamma and beta. They are used to perform an affine transformation of the standardized activations (activation = the output of the previous layer). The affine transformation allows to learn the identity transform and cancel the bacth normalization if this is what works best.
