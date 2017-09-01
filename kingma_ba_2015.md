# Adam

* Adam calcules a different learning rate for each optimization variable.

* The individual learning rates are calculated based on the first (mean) and second (variance) moments of the gradient of the objective with repect to each variable.

* Mean over variance is similar to a signal to noise ratio. If the signal to noise ratio is small, we make a small step.

* The value of the learning rate (alpha) is actually an (approximate) upper bound on the maximum step size (i.e., modification to the value of a variable) that we can make. So it's not so hard to choose its value.

* The parameter updates are invariant of the scale of the gradient. Using gradient * c will have no effect on the update, since it cancels out in the mean/variance ratio.
