---
layout: post
title:  "Causal Inference 02: Spurious Correlations"
date:   2020-01-17 15:18:30 +0800
categories: jekyll update
---

In part 1 *An Introduction*, many examples of spurious or implausible relations were discussed. Per capita cheese consumption vs Number of people who died by becoming tangled in their bed sheets and Divorce rate in Maine vs Per capita consumption of margarine each with a calculated correlation coefficient > 0.95. These were followed by an example analysing 'blood pressure' and 'yoga or running' where by a correlation was 'explained' through the inclusion of a third variable referred to as a *Confounder*, 'health conscious'. Although these examples all suffer from spurious correlations resulting in erroneous analyses there is a difference between the first two relations and the third; the first being a result of what one could determine as coincidence the third being a true causal effect simply with the incorrect causal structure. In this blog, a defining line between the coincidental and the incorrect causal structure is discussed along with helpful causal structures and a distributional proof as to how spurious correlations are "created" by incorrect use of data in analyses.

Spurious correlations of the coincidental type can be found through most fields and provide a caution for scientists aiming to crank the statistical handle and present a result. The question may arise as to why these 'coincidental' results arise given there 'probabilities' of occurrence are so low? The answer is found with the use of a simple coin. Imagine a coin is flipped 5 times and with the coin landing on heads all 5 times. Such a results will yield an extremely low probability of happening if the coin was perfectly fair, in fact it would produce a significant result at the 5% level. What is missing here though is the idea that even if the coin was perfectly fair, 1 out of 32 flips of 5 flip sequences would yield a 5 head result. Could it simply be the case that in our previous result was observed purely out of random luck; observing this 1/32 chance? Using this lens in analysing the previous correlations; these correlations arise from simple chance, there is no explainable causal model as to why Divorce rate in Maine impacts margarine consumption or vice versa. Change this correlation to Divorce rate in Maine vs Per capita consumption of butter a significant correlation coefficient is lost. Divorce rate and margarine consumption was the 1/32 chance of the coin flip, a high correlation but coincidental and EXPECTED through the laws of probability.

Machine learning and its famed subset, deep learning, has made significant advancements in fields of speech recognition, computer vision and language processing. Although results have been impressive only minimal progress has been made in understanding the 'how' these algorithms are achieving state of the art results. A favourite issue caused by an incorrect causal structure comes from the world of computer vision; discussion (here)[https://arxiv.org/pdf/1602.04938.pdf] highlights the importance of understanding models. In summary, an algorithm was trained to differentiate between dogs and wolves using standard observational data yielding a 96% accuracy. A closer inspection resulted in a strange finding; if you placed a dog on snowy background it would be classified as a wolf and wolf on grassed background it would be classified as a dog. The algorithm had learnt to classify images using the pixels of the background NOT the pixels of the animal! An interesting finding but how can this be expressed as from a causal view; causal structures are now presented to highlight importance of understanding the power of our models and not just finding correlations.

At the centre of Causal Inference lie the three causal structures; confounders, mediators and colliders the first of which has already be encountered. Every causal relationship can be depicted as a derivation of these three structures where each structure exhibits a different dependence structure relative to observed data. Of these three causal structures, dependent upon the whether certain data is observed or unobserved, certain variables within the structure can become dependent which introduces biases. Think back to the example of "yoga or running" and "blood pressure", when the variable "health conscious" marginalised over, a fancy word for left out in this scenario, a bias was introduced causing over estimate of effect of "yoga or running" on "blood pressure". Addition of the confounder provides a mechanism to first control for people of varying "health consciousness" levels and then analyse effects of "yoga or running". Conditioning on a Confounding variable, a fancy word for setting a variable equal to, eliminates biases between child variables, here, "yoga or running" and "blood pressure". Formally, statisticians term this bias removal **conditional independence**.

When we have access to data, should every variable be 'controlled for' as we saw in the Confounder use case? The answer is NO and this stems from the third type of causal structure, Colliders. In fact, 'controlling for' all variables WILL DO THE REVERSE and will INTRODUCE BIAS. This is an artifact of the dependency structures introduced by Colliders.


### Every accomplishment in this field to this point has been as a result of observational data

### Causal structures; mediators, confounders and colliders

### Colliders and spurious correlations: be careful on what you condition on


### Conclusion associational data, deep learning rules and combined with Causal structures will get us to level 2 of the Casual Ladder. Need for experimental design/dose dependent


Resources:
https://ftp.cs.ucla.edu/pub/stat_ser/r350.pdf
