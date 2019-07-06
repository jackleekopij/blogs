---
layout: post
title:  "The EM algorithm"
date:   2019-07-01 20:18:30 +0800
categories: jekyll update
---

GOAL: The EM algorithm provides a method of computation when the Maximum Likelihood Estimates or Maximum Apriori Predictions cannot directly be computed.
Typically, this situation arises in scenarios of missing or latent variables exist within the model.
Applications of the EM algorithm include clustering in machine learning, natural language processing where HMMs are used and psychometrics in item response modelling.

There are three defining steps of the EM algorithm:

  1. Initialisation of \theta
  2. Iterative improvements to \theta through iterative Expectation and Maximisation steps
  3. A step out condition; once likelihood tapers end process/ exit condition.

EXPECTATION-MAXIMISATION steps
The motive for the EM algorithm is that if a model contains know parameter \theta and latent variable Z where Z's domain is known, a estimate for Z can be calculated maximising the likelihood over Z's domaind given \theta.
Conversely, if Z is known deriving a new estimate for \theta is simple. However, when both are unknown we find ourselves in a chicken and egg problem.
The EM algorithm provides a solution through an iterative approach; where by an intialisation of \theta produces an estimate for Z which in turn produces an estimate for \theta.
From this iterative process the two steps of the EM are formed where:
  the Expectation step calculates the expectation of the likelihood given the current parameters.
  the Maximisation step maximises the parameters given the parameters from the Expected log likelihood.

Proof of why latent variables can't simply be factored out.
  i.e. \theta_z and \theta_x are not d-Separated.

AUXILIARY function Q(\theta, \theta^{t-1})
As previously mentioned, when direct calculation of the likelihood of the data is not possible due latent variables the parameters \theta_z and \theta_x are no longer d-Separated and therefore dependent.
To find estimates for parameters, a modified function is optimised called the auxiliary function.
The function is defined as the expected value of the log likelihood function of {\displaystyle {\boldsymbol {\theta }}} {\boldsymbol {\theta }}, with respect to the current conditional distribution of {\displaystyle \mathbf {Z} } \mathbf {Z}  given {\displaystyle \mathbf {X} } \mathbf {X}  and the current estimates of the parameters {\displaystyle {\boldsymbol {\theta }}^{(t)}} \boldsymbol\theta^{(t)}

Application to Gaussian Mixture Model


Resources:
http://www-bcf.usc.edu/~liu32/567/lec17.pdf
http://bjlkeng.github.io/posts/the-expectation-maximization-algorithm/
Kevin Murphy, Machine Learning; A probabilistic approach.
