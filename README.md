
# Partitioning and Law of Total Probabilities

## Introduction 
In this lesson, we shall look at the law of total probability. In probability theory, the law (or formula) of total probability is a fundamental rule relating **marginal probabilities** to conditional probabilities. It expresses the total probability of an outcome which can be realized via several distinct events, hence the name.

## Objectives
You will be able to:
* Understand and explain the concept of event space and partitioning 
* State the law of total probabilities based on a partitioned event space
* Understand and able to perform partitioning based on known and unknown probabilities to solve a problem
* Understand and describe conditional independence

## Partitioning a Sample Space

the Law of Total Probabiliyy can be used to calculate P(B). The law requires that you have a set of disjoint events Ai that collectively "cover" the event B. Then, instead of calculating P(B) directly, you add up the intersection of B with each of the events Ai. Let's see this graphically below:

Let $A_1, A_2, \dots, A_n$ partition sample space $S$ into disjoint regions that sum up to $S$. In the example, 4 regions of A1, .., A4 sum up to sample space $S$.

![](tp1.png)

The probability of a random event $B$ (orange area) can be written down as:

\begin{align}
    P(B) &= P(B \cap A_1) + P(B \cap A_2) + \dots + P(B \cap A_n) \\
         &= P(B|A_1)P(A_1) + P(B|A_2)P(A_2) + \dots + P(B|A_n)P(A_n)
\end{align}

Here we use the first theorem mentioned in the previous lesson to find the combined probabilities. 



Let's try to understand this using a simple example.

In a certain country there are three provinces; B1, B2, and B3 (i.e., the country is partitioned into three disjoint sets B1, B2, and B3). We are interested in the total forest area in the country. Suppose that we know that the forest area in B1, B2, and B3 are 100 km2, 50 km2, and 150 km2, respectively. What is the total forest area in the country? 

100km2 + 50km2 + 150km2 = 300 km2

We can simply add forest areas in each province (known as a partition) to obtain the forest area in the whole country. This is the idea behind the law of total probability, in which the area of forest is replaced by probability of an event A. In particular, if you want to find P(A), you can look at a partition of S (our sample space), and add the amount of probability of A that falls in each partition. 

We can say that for any two events A and B:

$P(A)=P(A∩B)+P(A∩Bc)$

and using the definition of conditional probability, P(A∩B)=P(A|B)P(B), we can write

$$P(A)=P(A|B)P(B)+P(A|Bc)P(Bc)$$

We can state a more general version of this formula which applies to a general partition of the sample space S.
## Law of Total Probability:

If B1,B2,B3,⋯ is a partition of the sample space S, then for any event A we have

$$P(A)=∑_iP(A∩Bi)=∑_iP(A|Bi)P(Bi)$$

Using a Venn diagram, we can pictorially see the idea behind the law of total probability. In the figure below, we have

* A1=A∩B1
* A2=A∩B2
* A3=A∩B3

<img src="ven1.png" width=400>
As it can be seen from the figure, A1, A2, and A3 form a partition of the set A, and thus 

> $P(A)=P(A1)+P(A2)+P(A3)$

Here is a typical scenario in which we use the law of total probability. We are interested in finding the probability of an event A, but we don't know how to find P(A) directly. Instead, we know the conditional probability of A given some events Bi, where the Bi's form a partition of the sample space. Thus, we will be able to find P(A) using the law of total probability
$$P(A)=∑_iP(A|Bi)P(Bi)$$

## Partitions

A lot of reasoning in probability theory involves decomposing a complicated event into simpler events, or decomposing complicated random variables into simpler ones like we saw in this simple problem above. Conditional probability is one way to do that, and it fits into this more general scheme of “decomposing” events and variables into components.

The usual way to break up a set into pieces is via a **Partition**. Recall the following set-theoretic definition. 

> A partition of a set $X$ is a collection of subsets $Xi \in X$ so that every element $x \in X$ occurs in exactly one of the $Xi$.

#### Examples:

* We can partition the natural numbers $\mathbb{N}$ into even and odd numbers. 
* We can partition the set of people in the world into subsets where each subset corresponds to a country and a person is placed in the subset corresponding to where they were born etc.


In statistics choosing the right partitioning is key as bad choices of partitions may results in many, even more difficult to solve sub-problems.

> The total probability law allows us to break up probability calculations into distinct parts. It’s used to find the probability of an event, A, when you don’t know enough about A’s probabilities to calculate it directly. Instead, you take a related event, B, and use that to calculate the probability for A.

![](tp2.png)

The probability for a can be written as sums of event B. The total probability rule is:

> $P(A) = P(A∩B) + P(A∩B^c)$

An alternate version of the total probability rule (found with the multiplication rule) can be used when the necessary probabilities are known  :

> $P(A ∩ B) = P(A | B) * P(B) + P(A ∩ B^c) = P(A | B^c)P(B^c)$

ONe really needs to be careful when dealing with conditional probabilities and conditioning. Let's look at a few examples to see this idea in action. 

### Example 1
In a certain county, 60% of registered voters are Republicans, 30% are Democrats and 10% are Independents.

When those voters were asked about increasing military spending
* 40% of Republicans opposed it
* 65% of the Democrats opposed it
* 55% of the Independents opposed it.

What is the probability that a randomly selected voter in this county opposes increased military spending?

Let:

* Ω = {registered voters in the county}
* R = {registered republicans}, P(R) = 0.6
* D = {registered democrats}, P(D) = 0.3
* I = {registered independents}, P(I) = 0.1
* B = {registered voters opposing increased military spending}

We also know:

* P(B|R) = 0.4 
* P(B|D) = 0.65
* P(B|I) = 0.55

By the total probability theorem:

$$Pr(B) = Pr(B|R) Pr(R) + Pr(B|D) Pr(D) + Pr(B|I) Pr(I)$$

= (0.4 · 0.6) + (0.65 · 0.3) + (0.55 · 0.1) = 0.49.

## Example 2 

Let's consider a 2-card hand drawn from a standard playing deck. What is the probability of drawing 2 aces, given that we know one of the cards is an ace?

\begin{align}
    P(\text{both are aces | one is ace}) &= \frac{P(\text{both are aces})}{P(\text{one is ace})} \\
    &= \frac{P(\text{both are aces})}{1 - P(\text{neither is ace})} \\
    &= \frac{\binom{4}{2}/\binom{52}{2}}{1 - \binom{48}{2}/\binom{52}{2}} \\
    &= \frac{1}{33}
\end{align}

But now think about this: What is the probability of drawing 2 aces, knowing that one of the cards __is the ace of spades__?

\begin{align}
    P(\text{both are aces | ace of spades}) &= P(\text{other card is also an ace}) \\
    &= \frac{3}{51} \\
    &= \frac{1}{17}
\end{align}

_Notice how the fact that we know we have the ace of spades nearly doubles the probability of having 2 aces._

## Example 3

Suppose there is a test for a disease, and this test is touted as being "95% accurate". The disease in question afflicts 1% of the population. Now say that there is a patient who tests positive for this disease under this test.

First we define the events in question:

Let $D$ be the event that the patient actually has the disease.

Let $T$ be the event that the patient tests positive.

Since that phrase "95% accurate" is ambiguous,  we need to clarify that.

\begin{align}
    P(T|D) = P(T^c|D^c) = 0.95
\end{align}

In other words, __conditioning on whether or not the patient has the disease__, we will assume that the test is 95% accurate.

_What exactly are we trying to find?_

What the patient really wants to know is not $P(T|D)$, which is the accuracy of the test; but rather $P(D|T)$, or the probability she has the disease given that the test returns positive. Fortunately, we know how $P(T|D)$ relates to $P(D|T)$.

\begin{align}
    P(D|T) &= \frac{P(T|D)P(D)}{P(T)} ~~~~ & &\text{... Bayes Rule} \\
    &= \frac{P(T|D)P(D)}{P(T|D)P(D) + P(T|D^c)P(D^c)} ~~~~ &  & \text{... by the Law of Total Probability} \\
    &= \frac{(0.95)(0.01)}{(0.95)(0.01) + (0.05)(0.99)} ~~~~ & & \text{... the rarity of the disease competes with the rarity of true negatives}\\
    &\approx 0.16
\end{align}

## Common Pitfalls

- Mistaking $P(A|B)$ for $P(B|A)$. 

This is also known as the [Prosecutor's Fallacy](https://en.wikipedia.org/wiki/Prosecutor%27s_fallacy), where instead of asking about the _probability of guilt (or innocence) given all the evidence_, we make the mistake of concerning ourselves with the _probability of the evidence given guilt_.


- Confusing _prior_ $P(A)$ with _posterior_ $P(A|B)$. 

Observing that event $A$ occurred does __not__ mean that $P(A) = 1$. But $P(A|A) = 1$ and $P(A) \neq 1$.


- Confusing _independence_ with __conditional independence__. 

This is more subtle than the other two. Let's look at this in a bit more detail


## Conditional Independence

Events $A$ and $B$ are __conditionally independent__ given event $C$, if

\begin{align}
    P(A \cap B | C) = P(A|C)P(B|C)
\end{align}

i.e. conditioning on event $C$ does not give us any additional information on $A$ or $B$.

### Conditional independence given $C$ DOES NOT imply unconditional independence.

Consider playing a series of 5 games against a chess opponent of unknown strength. Winning all five games gives would give you a good idea that you are better player. So winning each successive game actually is providing us with information about the strength of our opponent. If you have prior knowledge about the strength of your opponent, you condition on the strength of our opponent i.e. Winning one game would not provide us with any additional information on the probability of winning the next. Having no prior knowledge of your opponent, and winning a string a games will give you information about the probability of winning the next game.

> The games are conditionally independent given the strength of our opponent, but _not_ independent unconditionally.

### Unconditional independence DOes NOT imply conditional independence given $C$

For example Let $A$ be the event of the fire alarm going off, $F$ be the event of a fire and $C$ be the event of someone making popcorn. Suppose that either $F$ or $C$ will result in $A$ and the fire alarm going off. Now if $F$ and $C$ are independent: knowing that there's a fire $F$ doesn't tell me anything about anyone making popcorn $C$; and vice versa. But the probability of a fire given that the alarm goes off __and__ no one is making any popcorn is given by  $P(F|A,C^c) = 1$. After all, if the fire alarm goes off and no one is making popcorn, there can only be one explanation: _there must be a fire_.

So $F$ and $C$ may be independent, but they are not _conditionally independent_ when we condition on event $A$. Knowing that nobody is making any popcorn when the alarm goes off can only mean that there is a fire.

## Additional Resources
You are strongly advised to visit following links to get an indpeth understanding with examples and proofs for formulas highlighted in this lesson. 

[The law of total probability - concept and proof](https://www.youtube.com/watch?v=J7Evcn4lfhc) - Excellent YouTube video by Phil Chan.

[Conditional (Partitioned) Probability — A Primer](https://jeremykun.com/2013/03/28/conditional-partitioned-probability-a-primer/) - Deep dive into partitions (A Must read)

[Law of Total Probability](https://www.sangakoo.com/en/unit/law-of-total-probability) - More examples for a deeper understanding around partitioning

## Summary 

In this lesson, we further built on the ideas of conditional probability covered in the previous lesson to explain the law of total probability using partitioning of the sample space. We saw how we can partition probabilities with respect to some other event, when the direct probabilities are not known. Next we shall look at the "Bayes Theorem" which uses all the ideas covered so far and adds more goodness to the probability calculation. 
