---
layout: post
title:  "Bayes Nets: d-Separation"
date:   2019-03-05 20:18:30 +0800
categories: jekyll update
---

Aim:
Provide an introduction to the idea of d-separation, its importance/applications to Bayes Nets and distributional proofs for d-sepatation.


Introduction:
Bayesian networks, in a sense a misnomer provides a flexible framework to express causality of variables using a directed acyclic graph (DAG) format. Defining a graph in using a DAG structure naturally imposes ideas of causality by formation of conditional distributions. At the core of Bayes net representation these set of conditional independence assumptions which identify the **flow** of causality through a network.

The large majority of statistical and machine learning models require an assumption of independence. Bayes nets require also a machine learning method depend on a specific type of independence; conditional independence. Where as traditional independence can be thought of in a two variable case where knowing information about X provides no additional knowledge about Y, **conditional independence** further refines defined as knowing X provides no additional knowledge of Y *given* we observed Z. The observed set of variables Z is also referred to as evidence.

A Markov chain is an example of conditional independence where by conditioning on knowledge of the *present*, knowing the *past* provides no additional knowledge of the *future*. Under Markov assumption the *past is conditionally independent of the future*.

Bays Nets are defined as a collection of conditional probability distributions, d-separation (where d stands for dependency) is an algorithm to determine (conditional) independence in Bayes Net. d-separation provides a set of rules which can be used in analysis of a Bayes Nets to derive conditional independency (or lack thereof).

Determining d-separation between two variables conditional on evidence is calculated by using four substructures:

A -> B -> C
A <- B <- C
A <- B -> C
A -> B <- C

In the above, the first three rules A and C are conditionally independent given C while the forth (what is termed a collider) is conditionally independent ONLY when B is NOT observed. Facts for these rules are derived from the distributional rules of inverse probability.

***DEFINE THE RULES FROM INVERSE PROBABILITY***

***CONCLUDE THE BAYES NETS AND D-SEPARATION***



Intuition of filters, with a focus on Gaussian Smoothing Filters
Filtering is central to the field of Signal Processing, the reduction of noise from a signal.
An example would be the removal of static noise from a radio signal, specifically this is an example of a low pass filter which removes the high frequency noise from the signal.
Low pass filters also have extensive application to the fields of electrical and optical processing. Although numerous filtering techniques exist, focus will be on the smoothing filters; a technique which updates a data point's value by averaging over a proximal neighbourhoood.

Calculating the a smoothed value for a data point requires constructing a weighted average of the neighbouring data points. Weights used in this calculation are referred to as the kernel i.e. the smoothed value of a data point is  the dot product of the kernel and respective data points in the neighbourhood. A reader may currently be asking, what exactly is a kernel? Simply put a kernel is weighting function of non-negative real values, where the function integrates to 1 and is symmetrical. As definition so broad there exists many different kernels which fit such a definition. Examples include Gaussian kernel, logistic kernel, sigmoid function kernel, uniform kernel, triangular kernel and more. Note: this list of kernels is not exhaustive and simply serves to extenuate the point that the kernel is nothing more than a symmetrical of positive real valued function which integrates to 1. Of the listed kernel functions provided the Gaussian kernel is most widely used which we will explore further.

The Gaussian distribution is a symmetric probability distribution meaning it's a real valued function which integrates 1 thus fitting the requirements of a kernel function.
Use of the Gaussian distribution in kernel smoothing methods has produced various methodologies each with slightly varying titles Gaussian Kernel methods, Gaussian filters, Gaussian Smoothing Filters, Gaussian Blur. However, at the core of each of these methods is the process of the convolution of a Gaussian distribution with the observed data producing a new weighted (smoothed) average for each data point.



Where GSFs are both effective and ineffective.
	Easy to implement
	Intuitive (weighted average) of results.
	Pro and con: symmetric


Hands on example.
	1-d stock returns high amount of noise
	2-d image of Richard Feynman
