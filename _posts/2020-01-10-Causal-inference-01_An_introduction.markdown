---
layout: post
title:  "The EM algorithm"
date:   2020-01-10 15:18:30 +0800
categories: jekyll update
---

"Correlation does not imply causation", one of statistics most famed lines, used extensively throughout heated discussions which use data as evidence. This phrase has been popularised since the early 1900's by prominent statistician Karl Pearson in his battle against spurious correlation; Per capita cheese consumption vsNumber of people who died by becoming tangled in their bed sheets and Divorce rate in Maine vs Per capita consumption of margarine both of which attain a correlation coefficient > 0.95. Pearson was trying to directly attack such scenarios, to be conscious of the fact although correlation exists between two variables such relation may be caused by random phenomena. As time has progressed continuous efforts have been made to tackle the implications of this phrase delivered through the field of Causal Inference.

Advancements into the field of Causal Inference has provided scope for statisticians and machine learning practitioners to attack the "Correlation does not imply causation" restriction. **This tutorial will provide an introduction to a series of blog posts exploring causation and more over the benefits of approaching problems from a causal.** The series will explore causation topics such as missing data, intervention and counter-factuals. Each of these will be explored in details in their own blog though to explore each of topics the Causal Ladder first must be discussed. This introduction will briefly cover the Causal Ladder and its rungs, a summary of Causal Inference's benefits and introduce a basic causal model.

Seeing, doing and imaging these are three rungs of Causal Ladder as created by the god father of Causal Inference, Judea Pearl and articulated in his book, The Book of Why. Ascending the ladder from as Pearl describes as the base, Seeing is the art of strictly observing a phenomena more put as observational data and correlations. Machine learning algorithms for the majority are classified into this category; the is no consideration as to "how" or the cause of the data generation. Stepping to level, doing is the practice of intervention the first step towards causality. Interventions implement a practice of do-calculus, a special method of setting variables differing from conditioning a conditional distribution. Summarising the difference, conditional distributions (rung 1) are set the parameter value after the fact or data has been collected where as intervention is strict about how the data is collected. Ascending to the highest level is imaging, the counter-factuals, "what would have happened if I had of done A instead of B". Pearl argues this is what separates humans from other animals our ability to imagine what could have been and rapidly learn from past experience. Again counter-factuals will be explored in depth in their own post.

The Causal Ladder provide as framework to classify a data set's capacity and usefulness; if Causal Inference is available what are the benefits? 



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
