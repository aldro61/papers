# Adam

* Adam calcules a different learning rate for each optimization variable.

* The individual learning rates are calculated based on the first (mean) and second (variance) moments of the gradient of the objective with repect to each variable.

* If there is a lot of variance in the gradient of a variable, we don't make a big step.
