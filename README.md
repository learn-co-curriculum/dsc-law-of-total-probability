
# Partitioning and the Law of Total Probability

## Introduction 
In this lesson, we'll look at the law of total probability. In probability theory, the law (or formula) of total probability is a fundamental rule relating **marginal probabilities** to conditional probabilities. It expresses the total probability of an outcome that can be realized via several distinct events.

## Objectives
You will be able to:
- State the law of total probabilities based on a partitioned event space
- Explain the concept of event space and partitioning
- Describe conditional independence
- Perform partitioning based on known and unknown probabilities to solve a problem

## Partitioning a Sample Space

the Law of Total Probability can be used to calculate  <img src="https://render.githubusercontent.com/render/math?math=P(B)"> . The law requires that you have a set of disjoint events  <img src="https://render.githubusercontent.com/render/math?math=A_i"> that collectively "cover" the event  <img src="https://render.githubusercontent.com/render/math?math=B"> . Then, instead of calculating  <img src="https://render.githubusercontent.com/render/math?math=P(B)"> directly, you add up the intersection of  <img src="https://render.githubusercontent.com/render/math?math=B"> with each of the events  <img src="https://render.githubusercontent.com/render/math?math=A_i"> . Let's see this graphically below:

Let  <img src="https://render.githubusercontent.com/render/math?math=A_1, A_2, \dots, A_n"> partition sample space  <img src="https://render.githubusercontent.com/render/math?math=S"> into disjoint regions that sum up to  <img src="https://render.githubusercontent.com/render/math?math=S"> . In the example, the four regions  <img src="https://render.githubusercontent.com/render/math?math=A_1, A_2, A_3"> and  <img src="https://render.githubusercontent.com/render/math?math=A_4"> sum up to sample space  <img src="https://render.githubusercontent.com/render/math?math=S"> .

![](images/Image_55_TotProb.png)

The probability of a random event  <img src="https://render.githubusercontent.com/render/math?math=B"> (orange area) can be written down as:

<img src="https://render.githubusercontent.com/render/math?math=P(B)">
<img src="https://render.githubusercontent.com/render/math?math==P(B \cap A1) %2b P(B \cap A2) %2b P(B \cap A3)%2b P(B \cap A4)\"> <img src="https://render.githubusercontent.com/render/math?math==P(B \mid A1)P(A1) %2b P(B \mid A2)P(A2) %2bP(B \mid A3)P(A3)+ P(B \mid A4)P(A4">

Here we use the first theorem mentioned in the previous lesson to find the combined probabilities. 



### Example 

Let's use a simple example to clarify the image above! The example is created to match the image.

In a certain country, there are four provinces (eg. disjoint regions)  <img src="https://render.githubusercontent.com/render/math?math=A_1, A_2"> ,  <img src="https://render.githubusercontent.com/render/math?math=A_3"> and  <img src="https://render.githubusercontent.com/render/math?math=A_4"> .

You are interested in the total forest area,  <img src="https://render.githubusercontent.com/render/math?math=B"> , in the country. 

Suppose that you know that the forest area in  <img src="https://render.githubusercontent.com/render/math?math=A_1"> ,  <img src="https://render.githubusercontent.com/render/math?math=A_2"> , and <img src="https://render.githubusercontent.com/render/math?math=A_3"> are 100<img src="https://render.githubusercontent.com/render/math?math=\text{km}^2"> , 50<img src="https://render.githubusercontent.com/render/math?math=\text{km}^2"> , and 150<img src="https://render.githubusercontent.com/render/math?math=\text{km}^2"> , and 0<img src="https://render.githubusercontent.com/render/math?math=\text{km}^2"> respectively. What is the total forest area in the country? 

100<img src="https://render.githubusercontent.com/render/math?math=\text{km}^2"> + 50<img src="https://render.githubusercontent.com/render/math?math=\text{km}^2"> + 150<img src="https://render.githubusercontent.com/render/math?math=\text{km}^2"> + 0<img src="https://render.githubusercontent.com/render/math?math=\text{km}^2"> = 300<img src="https://render.githubusercontent.com/render/math?math=\text{km}^2"> 

We can simply add forest areas in each province to obtain the forest area in the whole country. 

This is the idea behind the law of total probability, in which the area of forest is replaced by probability of an event  <img src="https://render.githubusercontent.com/render/math?math=B"> . In particular, if you want to find  <img src="https://render.githubusercontent.com/render/math?math=P(B)"> , you can look at a partition of  <img src="https://render.githubusercontent.com/render/math?math=S"> (our sample space composed of  <img src="https://render.githubusercontent.com/render/math?math=A_1,\ldots, A_4"> ), and add the amount of probability of  <img src="https://render.githubusercontent.com/render/math?math=A"> that falls in each partition. 


### Two Events 

In general, we can say that for any two events  <img src="https://render.githubusercontent.com/render/math?math=A"> and  <img src="https://render.githubusercontent.com/render/math?math=B"> :

 <img src="https://render.githubusercontent.com/render/math?math=P(A)=P(A  \cap B)%2bP(A  \cap B')"> 

and using the definition of conditional probability,  <img src="https://render.githubusercontent.com/render/math?math=P(A  \cap B)=P(A \mid B)P(B)"> , we can write

 <img src="https://render.githubusercontent.com/render/math?math=P(A)=P(A \mid B)P(B)%2bP(A \mid B')P(B')"> 

The law of total probability is basically a general version of this. 


## Law of Total Probability 

If  <img src="https://render.githubusercontent.com/render/math?math=B_1"> , <img src="https://render.githubusercontent.com/render/math?math=B_2"> , <img src="https://render.githubusercontent.com/render/math?math=B_3"> , <img src="https://render.githubusercontent.com/render/math?math=\dots"> is a partition of the sample space S, then for any event A we have

 <img src="https://render.githubusercontent.com/render/math?math=P(A)= \sum_i P(A  \cap B_i)= \sum_i P(A \mid B_i)P(B_i)"> 

Using a Venn diagram, we can pictorially see the idea behind the law of total probability. In the figure below, we have

*  <img src="https://render.githubusercontent.com/render/math?math=A_1 = A  \cap B_1"> 
*  <img src="https://render.githubusercontent.com/render/math?math=A_2 = A  \cap B_2"> 
*  <img src="https://render.githubusercontent.com/render/math?math=A_3 = A  \cap B_3"> 

<img src="images/Image_56_vent.png" width="400">

As it can be seen from the figure,  <img src="https://render.githubusercontent.com/render/math?math=A_1"> ,  <img src="https://render.githubusercontent.com/render/math?math=A_2"> , and  <img src="https://render.githubusercontent.com/render/math?math=A_3"> form a partition of the set A, and thus 

 <img src="https://render.githubusercontent.com/render/math?math=P(A)=P(A_1)%2bP(A_2)%2bP(A_3)"> 

Here is a typical scenario in which we use the law of total probability. We are interested in finding the probability of an event  <img src="https://render.githubusercontent.com/render/math?math=A"> , but we don't know how to find P(A) directly. Instead, we know the conditional probability of  <img src="https://render.githubusercontent.com/render/math?math=A"> given some events  <img src="https://render.githubusercontent.com/render/math?math=B_i"> , where the  <img src="https://render.githubusercontent.com/render/math?math=B_i"> 's form a partition of the sample space. This way, you can use  <img src="https://render.githubusercontent.com/render/math?math=P(A)"> using the law of total probability

 <img src="https://render.githubusercontent.com/render/math?math=P(A)=\sum_i P(A \mid B_i)P(B_i)"> 


## More on Partitions

* The natural numbers  <img src="https://render.githubusercontent.com/render/math?math=\mathbb{N}"> can be partitioned into even and odd numbers. 
* The set of animal species in the world can be partitioned into subsets where a subset reflects a continent and each species is positioned in a subset depending on which continent they originated from. 

In statistics, choosing the right partitioning is key as bad choices of partitions may results in many sub-problems that are even more difficult to solve.

![](images/Image_57_TotProb_2.png)

The probability of  <img src="https://render.githubusercontent.com/render/math?math=A"> can be written as sums of event  <img src="https://render.githubusercontent.com/render/math?math=B"> (note that  <img src="https://render.githubusercontent.com/render/math?math=B^c"> is another way of writing  <img src="https://render.githubusercontent.com/render/math?math=B'"> ) The total probability rule is:

 <img src="https://render.githubusercontent.com/render/math?math=P(A) = P(A  \cap B) %2b P(A  \cap B^c)"> 

An alternate version of the total probability rule (found with the multiplication rule) can be used when the necessary probabilities are known:  

 <img src="https://render.githubusercontent.com/render/math?math=P(A) = P(A \mid B)  P(B) %2b P(A \mid B^c)P(B^c)"> 

You need to be careful when dealing with conditional probabilities and conditioning. Let's look at a few examples to see this idea in action. 

### Example 1
In a certain county in the United States, 60% of registered voters are Republicans, 30% are Democrats and 10% are Independents.

When those voters were asked about increasing military spending. 

*  40% of Republicans opposed it. 
*  65% of the Democrats opposed it. 
*  55% of the Independents opposed it.

What is the probability that a randomly selected voter in this county opposes increased military spending?

You know that:

*  <img src="https://render.githubusercontent.com/render/math?math=\Omega"> = {registered voters in the county}
*  <img src="https://render.githubusercontent.com/render/math?math=R"> = {registered republicans},  <img src="https://render.githubusercontent.com/render/math?math=P(R)"> = 0.6
*  <img src="https://render.githubusercontent.com/render/math?math=D"> = {registered democrats},  <img src="https://render.githubusercontent.com/render/math?math=P(D)"> = 0.3
*  <img src="https://render.githubusercontent.com/render/math?math=I"> = {registered independents},  <img src="https://render.githubusercontent.com/render/math?math=P(I)"> = 0.1
*  <img src="https://render.githubusercontent.com/render/math?math=B"> = {registered voters opposing increased military spending}

You also know that:

*  <img src="https://render.githubusercontent.com/render/math?math=P(B \mid R) = 0.4 "> 
*  <img src="https://render.githubusercontent.com/render/math?math=P(B \mid D) = 0.65"> 
*  <img src="https://render.githubusercontent.com/render/math?math=P(B \mid I) = 0.55"> 

By the total probability theorem:

 <img src="https://render.githubusercontent.com/render/math?math=Pr(B) = Pr(B \mid R) Pr(R) %2b Pr(B \mid D) Pr(D) %2b Pr(B \mid I) Pr(I)"> 

 <img src="https://render.githubusercontent.com/render/math?math== (0.4 * 0.6) %2b (0.65 * 0.3) %2b (0.55 * 0.1) = 0.49 "> 

### Example 2 

Let's consider a 2-card hand drawn from a standard playing deck. What is the probability of drawing 2 aces, given that we know one of the cards is an ace?

 <img src="https://render.githubusercontent.com/render/math?math=P(\text{both are aces | one is ace}) = \dfrac{P(\text{both are aces})}{P(\text{one is ace})} = \dfrac{P(\text{both are aces})}{1 - P(\text{neither is ace})} =\dfrac{\binom{4}{2}/\binom{52}{2}}{1 - \binom{48}{2}/\binom{52}{2}}=\dfrac{1}{33}"> 

But now think about this: What is the probability of drawing 2 aces, knowing that one of the cards __is the ace of spades__?

 <img src="https://render.githubusercontent.com/render/math?math=P(\text{both are aces | ace of spades}) = P(\text{other card is also an ace}) = \dfrac{3}{51}= \dfrac{1}{17}"> 

_Notice how the fact that we know we have the ace of spades nearly doubles the probability of having 2 aces_

### Example 3

Suppose there is a test for a disease, and this test is said to be "95% accurate". The disease in question afflicts 1% of the population. Now say that there is a patient who tests positive for this disease under this test.

First, we define the events in question:

Let  <img src="https://render.githubusercontent.com/render/math?math=D"> be the event that the patient actually has the disease.

Let  <img src="https://render.githubusercontent.com/render/math?math=T"> be the event that the patient tests positive.

Since that phrase "95% accurate" is ambiguous,  we need to clarify that.

 <img src="https://render.githubusercontent.com/render/math?math=P(T|D) = P(T^c|D^c) = 0.95"> 

In other words, __conditioning on whether or not the patient has the disease__, we will assume that the test is 95% accurate.

_What exactly are we trying to find?_

What the patient really wants to know is not  <img src="https://render.githubusercontent.com/render/math?math=P(T|D)"> , which is the accuracy of the test; but rather  <img src="https://render.githubusercontent.com/render/math?math=P(D|T)"> , or the probability she has the disease given that the test returns positive. Fortunately, we know how  <img src="https://render.githubusercontent.com/render/math?math=P(T|D)"> relates to  <img src="https://render.githubusercontent.com/render/math?math=P(D|T)"> .

<img src="https://render.githubusercontent.com/render/math?math=P(D|T)">  
<img src="https://render.githubusercontent.com/render/math?math== \frac{P(T|D)P(D)}{P(T)} ~~~~">... Bayes Rule (1)   
<img src="https://render.githubusercontent.com/render/math?math== \frac{P(T|D)P(D)}{P(T|D)P(D) %2b P(T|D^c)P(D^c)} ~~~~">... by the Law of Total Probability (2)   
<img src="https://render.githubusercontent.com/render/math?math== \frac{(0.95)(0.01)}{(0.95)(0.01) %2b (0.05)(0.99)} ~~~~">... the rarity of the disease competes with the rarity of true negatives (3)   
<img src="https://render.githubusercontent.com/render/math?math=\approx 0.16"> (4)

## Common Pitfalls

- Mistaking  <img src="https://render.githubusercontent.com/render/math?math=P(A|B)"> for  <img src="https://render.githubusercontent.com/render/math?math=P(B|A)"> . 

This is also known as the [Prosecutor's Fallacy](https://en.wikipedia.org/wiki/Prosecutor%27s_fallacy), where instead of asking about the _probability of guilt (or innocence) given all the evidence_, we make the mistake of concerning ourselves with the _probability of the evidence given guilt_.


- Confusing _prior_  <img src="https://render.githubusercontent.com/render/math?math=P(A)"> with _posterior_  <img src="https://render.githubusercontent.com/render/math?math=P(A \mid B)"> . 

Observing that event  <img src="https://render.githubusercontent.com/render/math?math=A"> occurred does __not__ mean that  <img src="https://render.githubusercontent.com/render/math?math=P(A) = 1"> . But  <img src="https://render.githubusercontent.com/render/math?math=P(A \mid A) = 1"> and  <img src="https://render.githubusercontent.com/render/math?math=P(A) \neq 1"> .


- Confusing _independence_ with __conditional independence__. 

This is more subtle than the other two. Let's look at this in a bit more detail


## Conditional Independence

Events  <img src="https://render.githubusercontent.com/render/math?math=A"> and  <img src="https://render.githubusercontent.com/render/math?math=B"> are __conditionally independent__ given event  <img src="https://render.githubusercontent.com/render/math?math=C"> , if

 <img src="https://render.githubusercontent.com/render/math?math=P(A  \cap B \mid C) = P(A \mid C)P(B \mid C)"> 

i.e. conditioning on event  <img src="https://render.githubusercontent.com/render/math?math=C"> does not give us any additional information on  <img src="https://render.githubusercontent.com/render/math?math=A"> or  <img src="https://render.githubusercontent.com/render/math?math=B"> .

### Conditional independence given  <img src="https://render.githubusercontent.com/render/math?math=C"> DOES NOT imply unconditional independence

Consider playing a series of 5 games against a chess opponent of unknown strength. Winning all five games would give you a good idea that you are a better player. So winning each successive game is actually providing us with information about the strength of our opponent. If you have prior knowledge about the strength of your opponent, you condition on the strength of our opponent i.e. winning one game would not provide us with any additional information on the probability of winning the next. Having no prior knowledge of your opponent and winning a string a games will give you information about the probability of winning the next game.

The games are conditionally independent given the strength of our opponent, but **not** independent unconditionally.

### Unconditional independence DOES NOT imply conditional independence given  <img src="https://render.githubusercontent.com/render/math?math=C"> 

For example, let  <img src="https://render.githubusercontent.com/render/math?math=A"> be the event of the fire alarm going off,  <img src="https://render.githubusercontent.com/render/math?math=F"> be the event of a fire, and  <img src="https://render.githubusercontent.com/render/math?math=C"> be the event of someone making popcorn. Suppose that either  <img src="https://render.githubusercontent.com/render/math?math=F"> or  <img src="https://render.githubusercontent.com/render/math?math=C"> will result in  <img src="https://render.githubusercontent.com/render/math?math=A"> and the fire alarm going off. Now if  <img src="https://render.githubusercontent.com/render/math?math=F"> and  <img src="https://render.githubusercontent.com/render/math?math=C"> are independent: knowing that there's a fire  <img src="https://render.githubusercontent.com/render/math?math=F"> doesn't tell you anything about anyone making popcorn  <img src="https://render.githubusercontent.com/render/math?math=C"> , and vice versa. But the probability of a fire given that the alarm goes off **and** no one is making any popcorn is given by   <img src="https://render.githubusercontent.com/render/math?math=P(F \mid A,C^c) = 1"> . After all, if the fire alarm goes off and no one is making popcorn, there can only be one explanation: _there must be a fire_.

So  <img src="https://render.githubusercontent.com/render/math?math=F"> and  <img src="https://render.githubusercontent.com/render/math?math=C"> may be independent, but they are not _conditionally independent_ when we condition on event  <img src="https://render.githubusercontent.com/render/math?math=A"> . Knowing that nobody is making any popcorn when the alarm goes off can only mean that there is a fire.

## Additional Resources
You are strongly advised to visit following links to get an indepth understanding with examples and proofs for formulas highlighted in this lesson. 

[The law of total probability - concept and proof](https://www.youtube.com/watch?v=J7Evcn4lfhc) - Excellent YouTube video by Phil Chan.

[Conditional (Partitioned) Probability — A Primer](https://jeremykun.com/2013/03/28/conditional-partitioned-probability-a-primer/) - Deep dive into partitions (A Must Read)

[Law of Total Probability](https://www.sangakoo.com/en/unit/law-of-total-probability) - More examples for a deeper understanding around partitioning

## Summary 

In this lesson, you further learned about the ideas of conditional probability covered in the previous lessons to explain the law of total probability using partitioning of the sample space. You learned how you can partition probabilities with respect to some other event, when the direct probabilities are not known. Let's move on to some practice!
