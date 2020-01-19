---
layout: post
title:  "Causal Inference 02: Spurious Correlations"
date:   2020-01-10 15:18:30 +0800
categories: jekyll update
---

In part 1 *An Introduction*, many examples of spurious or implausible relations were discussed. Per capita cheese consumption vs Number of people who died by becoming tangled in their bed sheets and Divorce rate in Maine vs Per capita consumption of margarine each with a calculated correlation coefficient > 0.95. These were followed by an example analysing 'blood pressure' and 'yoga or running' where by a correlation was 'explained' through the inclusion of a third variable referred to as a *Confounder*, 'health conscious'. Although these examples all suffer from spurious correlations resulting in erroneous analyses there is a difference between the first two relations and the third; the first being a result of what one could determine as coincidence the third being a true causal effect simply with the incorrect causal structure. In this blog, a defining line between the coincidental and the incorrect causal structure is discussed along with helpful causal structures and a distributional proof as to how spurious correlations are "created" by incorrect use of data in analyses.

Spurious correlations of the coincidental type can be found through most fields and provide a caution for scientists aiming to crank the statistical handle and present a result. The question may arise as to why these 

Machine learning and its famed subset, deep learning, has made significant advancements in fields of speech recognition, computer vision and language processing. Although results have been impressive only minimal progress has been made in understanding the 'how' these algorithms are achieving state of the art results. A favourite issue caused by an incorrect causal structure comes from the world of computer vision; discussion (here)[https://arxiv.org/pdf/1602.04938.pdf] highlights the importance of understanding models. In summary, an algorithm was trained to differentiate between dogs and wolves using standard observational data yielding a 96% accuracy. A closer inspection resulted in a strange finding; if you placed a dog on snowy background it would be classified as a wolf and wolf on grassed background it would be classified as a dog. The algorithm had learnt to classify images using the pixels of the background NOT the pixels of the animal! An interesting finding but how can this be expressed as from a causal view; causal structures are now presented to highlight importance of understanding the power of our models and not just finding correlations.


### Every accomplishment in this field to this point has been as a result of observational data

### Causal structures; mediators, confounders and colliders

### Colliders and spurious correlations: be careful on what you condition on


### Conclusion associational data, deep learning rules and combined with Causal structures will get us to level 2 of the Casual Ladder. Need for experimental design/dose dependent

"Correlation does not imply causation", one of statistics most famed lines, used extensively throughout heated discussions which use data as evidence. This phrase has been popularised since the early 1900's by prominent statistician Karl Pearson in his battle against spurious correlation; Per capita cheese consumption vs Number of people who died by becoming tangled in their bed sheets and Divorce rate in Maine vs Per capita consumption of margarine both of which attain a correlation coefficient > 0.95. Pearson was trying to directly attack such scenarios, to be conscious of the fact although correlation exists between two variables such relation may be caused by random phenomena. As time has progressed continuous efforts have been made to tackle the implications of this phrase delivered through the field of Causal Inference.

Advancements into the field of Causal Inference has provided scope for statisticians and machine learning practitioners to attack the "Correlation does not imply causation" restriction. **This tutorial will provide an introduction to a series of blog posts exploring causation and more over the benefits of approaching problems from a causal.** The series will explore causation topics such as missing data, intervention and counter-factuals. Each of these will be explored in details in their own blog though to explore each of topics the Causal Ladder first must be discussed. This introduction will briefly cover the Causal Ladder and its rungs, a summary of Causal Inference's benefits and introduce a basic causal model.


![test5](../../../../../assets/Causal_ladder.png)
*Figure 1. The Causal Ladder*

Seeing, doing and imaging these are three rungs of Causal Ladder as created by the god father of Causal Inference, Judea Pearl and articulated in his book, The Book of Why. Ascending the ladder from as Pearl describes as the base, Seeing is the art of strictly observing a phenomena more put as observational data and correlations. Machine learning algorithms for the majority are classified into this category; the is no consideration as to "how" or the cause of the data generation. Stepping to level, doing is the practice of intervention the first step towards causality. Interventions implement a practice of do-calculus, a special method of setting variables differing from conditioning a conditional distribution. Summarising the difference, conditional distributions (rung 1) are set the parameter value after the fact or data has been collected where as intervention is strict about how the data is collected. Ascending to the highest level is imaging, the counter-factuals, "what would have happened if I had of done A instead of B". Pearl argues this is what separates humans from other animals our ability to imagine what could have been and rapidly learn from past experience. Again counter-factuals will be explored in depth in their own post.

The Causal Ladder provide as framework to classify a data set's capacity and usefulness; if Causal Inference is available what are the benefits? Breadth and depth of questions adressable by employing Causal Inference is the answer. Briefly touched on through the Casual Ladder when Causal Inference is unavailable analysis is constrained to be purely observational in nature, or "what happened". It is quite plausible to believe a random sample of people who do yoga or run on a weekly basis will have a lower blood pressure than those who don't.

Observing metrics on these groups would provide evidence to support this hypothesised correlation. Through a Causal Inference lense it can be identified that this is not complete story, we are missing the *Why* or "why does doing yoga or running on a weekly basis" reduce blood pressure, is it reduced muscle tension which increases blood flow thus decreasing pressure, is it people who have lower blood pressure feel better and thus spend more time doing healthy activities like "yoga or running"? Both of these interpretations are valid from a pure correlation view though fall short of addressing the *Why*.

![test5](../../../../../assets/Causal_model_health.png)
*Figure 2. An example of a Confounder, Health conscious, affecting both blood pressure and "yoga or running" variables. Such confounding can introduce spurious correlation*

To truly explore Causal Inference we must introduce the first structure of Causal Inference, the Confounder. A Confounder is a variable which has an affects variables you are measuring. A Confounder in the previous example would be a more health conscious person is more likely to run and a also be healthier. So from the previous correlation found between "yoga or running" and blood pressure, directly attributing any blood pressure improvement effect from running will over state the running effect as the "health conscious" Confounder of a person has not been accounted for. As a primer, this should illustrate the need for Causal Inference with more complex "causal structures" being explored in subsequent posts detailing consequences of getting these structures incorrect.


This blog aimed to introduce the framework of the Causal Ladder (and its rungs; Seeing, Doing and Imagining), a brief display of the need for causal inference finally concluding with a first acquaintance of a causal structure by illustration of a DAG.


Stay tuned for the next post Causal Inference 02: Missing Data including examples of catastrophic consequences arising from inadequate data collection procedures.




Resources:
https://ftp.cs.ucla.edu/pub/stat_ser/r350.pdf
