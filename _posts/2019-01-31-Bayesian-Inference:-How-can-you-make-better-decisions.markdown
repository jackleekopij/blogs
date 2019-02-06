Discuss how Bayesian inference is immensely important for making decisions; moreover how humans tend to forget base rates. 

Did Winston Churchill study probability in his time away from being Prime Minister - articulating the famous quote "When the facts change, I change my mind. What do you do, madam?". And what does this statement tell us about decision making under the Bayesian perspective. 
Well, you might not realise it but like Churchill you apply the same probabilistic reasoning everyday without your knowing. Termed Bayesian Inference, among other names, it's the process of first observing an unfolding scenario, secondly contextualising the observations with your prior worldly experience and finally formulating a degree of belief about the scenario. 
Technical aspects of Bayesian inference followed by an exploration into how these methods of degree of belief differ from simple frequency counts for probability concluding on how to implement this line of reasoning into our everyday life. 

In a world where we are inundated with data decisions are becoming increasingly complex and difficult to make. Bayesian inference provides, an albeit, simplified framework to make these decisions which most likely already how you shape your decisions and beliefs. 
The goal of the framework is to derive a degree of belief (the posterior) from the what has just been observed (the likelihood) and previously held beliefs (the prior). Simplifying, Bayesian inference is written as: 

	Posterior ~= Likelihood * Prior

Above is a simplification to Bayesian probability but what do each of these parameters actually mean and how does is relate to formulating beliefs and decision making? 
First, let's define a hypothesis, H = 'the chance of flipping a coin and getting heads is 50%'.
Secondly, let's define our previously held beliefs about the hypothesis (before the coin is flipped) i.e. the prior. Note: if there isn't a reason to suspect the coin is any but fair the prior is set to a 50/50 chance of heads or tails. 
Then, collect the data by flipping the coin and recording the number of flips and heads. Calculating the proportion of observed heads is sufficeint to quantify the likelihood.
Finally, to construct a degree of belief, Posterior, the Likelihood and Prior are multiplied together (which is from the reasonable assumption that our Prior beliefs don't affect the observed data). 
The Posterior distrbution calculates the probability of our hypothesis being true given the data observed (the proportion of heads flipped).

<Coin example: i.e. flipping 10000 coins in row then being asked to make a bet on whether coin is fair> 


*The Prior* 
	is a distrbution of the

Difference between posterior and likelihood (Bayes vs frequentist)
	The need to understand uncertainty
	If using MLE or MAP (single point) don't use frequentist methods. Will yield the same

How to use Bayesian thinking in everyday life.
	Never forget to use the base rate when making decisions.
	Resist the urge to think you are something special.

