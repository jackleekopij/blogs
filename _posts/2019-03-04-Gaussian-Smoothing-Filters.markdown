---
layout: post
title:  "Smoothing over the little things: Gaussian Smoothing Filters"
date:   2019-03-05 20:18:30 +0800
categories: jekyll update
---

Aim:
Create a simple tutorial on Gaussian Smoothing Filters (GSFs) upon completion the reader understands intuition of filters specifically GSFs, understand the where GSFs are both effective and ineffective
are able to implement 1-dimensional and 2-dimensional GSFs to real life data.


Introduction:
Recent year has seen a surge in corporations from medicine to agriculture to oil & gas to technology all try to harness the power of Big Data.
Promises of the value data has grown with the size of the data sets; unfortunately, growth of datasets has also increased difficulty levels in distinguishing signal from noise.
Luckily, for the budding data scientist numerous methods exist to de-noise data. A popular technique used to remove high frequency artifacts from data is the application of a low pass filter.
Applying a low pass filter smooths a process removing sharp (and abrupt) features of the data i.e. images captured in unfavourable lighting conditions exhibit large amounts of white noise.
Of the low pass filters, Gaussian Smoothing Filters (GSFs) are among the most popular and powerful.
Covered in this post will be a general intuition of filters from a signal processing lens, an exploration into GSFs including their pros & cons and finally concluding with an application.



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
