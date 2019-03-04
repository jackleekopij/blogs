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
Recent year has seen a surge in corperations from medicine to agriculture to oil & gas to technology all try to harness the power of Big Data. 
Promises of the value data has grown with the size of the data sets; unfortunately, growth of datasets has also increased difficulty levels in distinguishing signal from noise. 
Luckily, for the budding data scientist numerous methods exist to denoise data. A popular technique used to remove high frequency artifacts from data is the application of a low pass filter. 
Applying a low pass filter smooths a process removing sharp (and abrupt) features of the data i.e. images captured in unfavourably lighting conditions exhibit large amounts of white noise.
Of the low pass filters, Gaussian Smoothing Filters (GSFs) are among the most popular and poweful. 
Covered in this post will be a general intuition of filters from a signal processing lens, an exploration into GSFs including their pros & cons and finally concluding with an application.



Intuition of filters, with a focus on Gaussian Smoothing Filters
Filtering is central to the field of Signal Processing, the reduction of noise from a signal. 
An example would be the removal of static noise from a radio signal, specifically this is an example of a low pass filter which removes the high frequency noise of the signal. 
Low pass filters also have extensive application to electrical and optical processing. 
	Why would you use a filter (low pass filter)?
	i.e. images captured in unfavourably lighting conditions exhibit large amounts of white noise.  
	Applications to signal processes
	What is a kernel, specifically mathematical characteristics of a kernel? 
	What types of kernels exist?

Where GSFs are both effective and ineffective. 
	Easy to implement
	Intuitive (weighted average) of results. 
	Pro and con: symmetric


Hands on example. 
	1-d stock returns high amount of noise 
	2-d image of Richard Feynman
	
