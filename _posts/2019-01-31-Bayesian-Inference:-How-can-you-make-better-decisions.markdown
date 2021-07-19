Discuss how Bayesian inference is immensely important for making decisions; moreover how humans tend to forget base rates. 

Did Winston Churchill study probability in his time away from being Prime Minister - articulating the famous quote "When the facts change, I change my mind. What do you do, madam?". And what does this statement tell us about decision making under the Bayesian perspective.
Well, you might not realise it but like Churchill you apply the same probabilistic reasoning everyday without your knowing. Termed Bayesian Inference, among other names it's the process of first observing an unfolding events within context of your prior worldly experience which is then formulated into YOUR degree of belief about the situation.
This post provides an introduction to technical aspects of Bayesian inference followed by an exploration into how these methods of degree of belief differ from simple frequency counts for probability concluding on how to implement this line of reasoning into our everyday life.

In a world where we are inundated with data decisions are becoming increasingly complex and difficult to make. Bayesian inference provides, an albeit, simplified framework to make these decisions which most likely already how you shape your decisions and beliefs.
The goal of the Bayesian inference is to derive a degree of belief (the posterior) from the what has just been observed (the likelihood) and previously held beliefs (the prior). Simplifying, Bayesian inference is written as:

	Posterior ~= Likelihood * Prior

Above is a simplification to Bayesian reasoning but what do each of these parameters actually mean and how does they relate to formulating our degrees of beliefs in decision making?
First, let's define a hypothesis, H = 'the chance of flipping a coin and getting heads is 50%'.
Secondly, let's define our previously held beliefs about the hypothesis (before the coin is flipped) i.e. the prior. Note: if there isn't a reason to suspect the coin is any but fair the prior is set to a 50/50 chance of heads or tails.
Then, collect the data by flipping the coin and recording both the total number of heads and flips of the coin. Calculating the proportion of observed heads is sufficient to quantify the likelihood.
Finally, to construct a degree of belief, the posterior; the Likelihood and Prior are multiplied together (which is from the reasonable assumption that our Prior beliefs don't affect the observed data).
The Posterior distribution calculates the probability of our hypothesis being true given the data observed (the proportion of heads flipped).

<Coin example: i.e. flipping 10000 coins in row then being asked to make a bet on whether coin is fair>

With an overview of Bayesian inference covered; focus is placed on highlighting the differences traditional (frequentist) and Bayesian methods. A simplified view is that frequentist methods will only use the likelihood of to make inference, forgoing the application of any prior knowledge that the Bayesian would use. A rationale for this is that the frequentist remains objective in his analysis of the data where as Bayesian will introduce subjectivity into his analysis by including the prior.


At first, these differences may seem minor or trivial; however by excluding the prior distribution the resultant distribution drastically changes. From a frequentist analysis the distribution used for inference is the likelihood, P(x|theta), whereas the Bayesian use the posterior (the inverse of the likelihood), P(theta|x). Analysing the likelihood, P(x|theta), an astute reader may have questioned what the likelihood is actually modeling. Explicitly, the likelihood is modeling the P-value, moreover 'under hypothesis theta how likely is the data that was observed'. If the data was relatively different from the hypothesised parameter, thus hypothesis will be rejected. Measuring this relative difference is achieved by use of a p-value, where if the p-value is less than 0.05 then the null hypothesis is rejected. Contrary, the Bayesian makes use of all prior knowledge and will utilise it as such in his analysis to formulate the posterior distribution, P(theta|x). Subtile, the posterior distribution has a largely different interpretation to the likelihood. In English, the distribution is now 'given an observed set of data what is the probability of parameter theta'. Wait what! Theta our parameter is a distribution? Correct, a distinguishing feature between frequentist and Bayesian methods is that frequentists make inference about whether the data supports a hypothesis about a single parameter value parameter whereas Bayesian inference produces a probability distribution over possible parameter values. There are more consequences of each distribution that will be explored in subsequent posts about uncertainty.

After exploring the methodology of Bayesian inference you are now equipped with a toolkit to make better decisions in your daily life but where do such situations arise? Well, they may be more numerous and frequent than you think. An example, is taken from the fantastic book, Thinking Fast and Slow by Daniel Kahneman; "you are "

Tom W is of high intelligence, although lacking in true creativity. He has a need for order and clarity, and for neat and tidy systems in which every detail finds its appropriate place. His writing is rather dull and mechanical, occasionally enlivened by somewhat corny puns and flashes of imagination of the sci-fi type. He has a strong drive for competence. He seems to have little feel and little sympathy for other people, and does not enjoy interacting with others. Self-centered, he nonetheless has a deep moral sense.


Difference between posterior and likelihood (Bayes vs frequentist)
	The need to understand uncertainty
	If using MLE or MAP (single point) don't use frequentist methods. Will yield the same

How to use Bayesian thinking in everyday life.
	Never forget to use the base rate when making decisions.
	Resist the urge to think you are something special.
