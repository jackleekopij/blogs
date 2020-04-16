---
layout: post
title:  "A summary: Lex Fridman with David Silver interview"
date:   2020-04-06 15:18:30 +0800
categories: jekyll update
---

YouTube video:
https://www.youtube.com/watch?v=uPUEq8d73JI&t=0s

## Journey into AI
Started at a games start up building handcrafted agents however only due to 'twitch-like' patterns. All these were short term fixes; went back to do PhD based on RL approach to GO. All this was pre deep learning.

Game of GO would still be not beat world class champion and win even with exponential growth of compute and heuristic (rules) search methods from the DEEPBLUE win. People tried many a heuristic rules however couldn't over come what David defines as a "human intuitive sense" of how to play and evaluate though these rules could not be programmed into these heuristic rules.

### Learning as part of the system
David always felt learning must always be integrated into AI systems. Learning through understanding; can only been done by understanding. If you are not you must be inputting pre-defined rules which subsequently traces back to "brittle, handcrafted rule based systems".

Backed off and went to first principled approach to allow the system to learn for itself to see if specific actions provide extra reward. Such approach required the system to be able to verify/affirm value of each action.

### H
Evaluation of a static GO board is very hard whereas chess is relatively trivial where a value based count of pieces can act as a proxy. GO on the other hand has very few captures, most of the time white and black will have same number of pieces on board and territory cannot be calculated prior to completion.


### Path to intelligence
Opportunity to frame what the problem of AI is... David separates the AI into two components; the problem and the solution of AI. Problem of AI can be formalised in the RL framework which gives a path towards AGI. However, RL may not necessarily be the solution to the problem other methods may arise that solve the RL formatted version of AI.


### WHAT IS RL

STUDY, SCIENCE AND PROBLEM of intelligence of form of agent that interacts with environment. The agent then gets to act on the environment. The environment then returns both a state and a reward signal. The goal of RL is to optimise this reward signal overtime. Are the a value function; is it trying to calculate rewards into the future? Is there a policy are you trying determine optimal actions? Is it a model based; are you trying to build something to understand dynamics of an environment? Requires to consider what form you are designing for; i.e. prediction trying to predict the long run reward or are you designing to optimise a policy.


### DEEP LEARNING WITH RL (DEEP RL)
Simply using deep learning to approximate each of the three components; value function, policy or model. "Will this deep networks be looked back on as naive first attempts in 100 years?" The conversation turns to the idea of cellular automata; could we be missing something AI such that very simple underlying rules give rise to the complexity of human consciousness.

Simple rules with compute are proving to be most effective - Rich Sutton. Likely, simple clearest ideas will take us into the future of AI. David and Lex discuss that the complexity of current RL systems are too high.

How can you build the intuition of a human into a GO agent i.e. have the agent look at the board and evaluate current state.


### Use or no use of human data?
AlphaGo; deep learning vs rl perspective. Chose to use human data to understand system and build deep learning representation of optimal policies. David makes reference to how he does research; starts off with simple building blocks and incorporates complexity over time. Uses human data (labelled) to assist in understanding the more 'principled' approach.


# AlphaGo/AlphaZero
Puts learning at forefront; system must be able to understand and evaluate the utility of each step independently of humans. AlphaZero is a self play approach where the system has to play itself to figure out the rules. This makes the system less brittle (more robust to changes) and able to scale between environments. AlphaZero plays in a fully _self discovered_ process requiring no home player to achieve learning goals. David states that any AlphaZero-like algorithm, which has _self play_, any algorithm with a larger amount of computational resources will outplay predecessor algorithms (with less compute) 100 games to 0.

Creativity in AlphaGo; where creativity means discovering something previously not known. Therefor self play is the essence of creativity - where you play under current norms then try more creative moves. AlphaZero was able to learn the jusecky of Go; a subset of known rules/best strategies which should always be played given a current world state.

To summarise; AlphaZero is a general approach/toolkit to learning through self play which can be applied to various domains.

# Meaining of life
Humans trying to figure out our own reward function. "David what is the reward function for human life", David responded with "There are many levels, does the universe have a purpose or is it just following laws of mechanics? Then could look to a deeper level is the goal to maximise entropy? Then how could the universe maximise consumption of entropy? Is this evolution the universes method to optimise this entropy?
". Summarising, there are many levels of intelligence at each level we can optimise.
