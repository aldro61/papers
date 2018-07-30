# Variational inference

This is a way to do inference with posterior distributions that are intractable. The idea is to estimate the posterior using a family of distributions that are tractable and parametrizable, and to learn the parameters such that the approximate posterior is close to the true one (in terms of KL divergence).


* Variational methods turn inference into an optimization problem.
* Maximizing the ELBO is equivalent to minimizing the KL (30:40)
* Mean field family of approx posteriors q assumes that each random variable has it's own (independant) distribution. It is the optimization that pulls the independant distributions (with their parameters) to be close to the true posterior.
