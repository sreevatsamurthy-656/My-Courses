# Introduction to Probability

## Agenda of the Topic:

1. Probability
2. Sample Space
3. Events and their types
4. Types of Probability
5. Independent and Dependent Events
6. Bayes' Theorem

## What is Probability?

* It is the chance of something occurring, or the chance of something not occuring
* It is an important part of statistics as it forms the basis of **inference**
* Most statistics is calculated under **uncertainity**.
* In order to give measurable, understandble and certain results in the face of this uncertainity, probability is used.

## Events

* An Event is the set of outcomes of an experiment.
* An example of an experiment is **rolling a die**
* Events are of two types:
  - Elementary Events
  - Non- Elementary Events
  
### Elementary Events

* An elementary event is an event which does not have any other events in it.
* Example - Proabability that you get 6 on rolling a die.

### Non-Elementary Events

* A non-elementary event is an event which can have other events inside it.
* Example - Probability that you get an even number on rolling a die.

## Sample Space

* All of the different events of a given experiment form the sample space.
* For Example - A set of all the outcomes you can get on rolling a pair of dice.

| Die 1 \ Die 2 | 1     | 2     | 3     | 4     | 5     | 6     |
|---------------|-------|-------|-------|-------|-------|-------|
| 1             | (1,1) | (1,2) | (1,3) | (1,4) | (1,5) | (1,6) |
| 2             | (2,1) | (2,2) | (2,3) | (2,4) | (2,5) | (2,6) |
| 3             | (3,1) | (3,2) | (3,3) | (3,4) | (3,5) | (3,6) |
| 4             | (4,1) | (4,2) | (4,3) | (4,4) | (4,5) | (4,6) |
| 5             | (5,1) | (5,2) | (5,3) | (5,4) | (5,5) | (5,6) |
| 6             | (6,1) | (6,2) | (6,3) | (6,4) | (6,5) | (6,6) |

## Mutually Exclusive Events

* Given two events, if the occurance of one event prevents the occurance of the other and vice versa, then they are called mutually exclusive events

* For example
  - Head and tail occuring in a coin
  - Passing and Failing a Test 

* There is no intersection between these two events

## Collectively Exhaustive events

* All possible elementary events together are called collectively exhaustive
* Collectively Exhaustive Events together form the Sample Space
* For Example - On tossing a Coin, getting a head and getting a tail are collectively exhaustive events

## Independent and Dependent Events

### Independent Events

Given two events - one with outcome 1 and another with outcome 2; If outcome 2 is not affected by outcome 1, then the two events are called independent events

For example:

* The first roll of a die and the second roll of a die
* Removing balls from a bag in 1st and 2nd time **with** replacement
* Person's pen color and the shirt color

### Dependent Events

Two events which are mutually dependednt on each other are called dependent events

For Example:

* Removing balls from a bag 1st and 2nd time **without** replacement
* Seating choices - What choices and number of choices a person has based on turn

## Complementary Events

All events that are **NOT** the 'original event' are called **Complementary Events**

For Example:

* Event of **NOT** getting a 1 on rolling a die (i.e. getting 2, 3, 4, 5 or 6)
* Event of **NOT** getting a head on tossing a coin (i.e. getting a tails)

## Types of Probabilities

The types of probabilities are:

1. Emperical Probability
2. Subjective Probability
3. Classicial Probability


### Classical Proabability

* Classicial Probability is also called as a priori or theoretical probability
* This means that the probability outcome is defined according to how it should be theoretically
* The formula for an event A occuring according to classical probability is:

$$
P(A) = \frac{\text{m ways the required output can happen}}{\text{n ways all outcomes can happen}}
$$

For example in tossing a coin and getting a head:


 - m = 1 event to get head
 - n = 2 events in sample space

So:

$$
P(\text{getting a head}) = \frac{1}{2}
$$ 

* Classical Probability is mostly used for symmetrical situations
* It cannot be used for unequal probabilites
  
### Emperical Probability

* It is also called as A posteriori or frequentist probability
* It is used to deal with unequal or asymmetric probabilities
* In this, we perform a large number of trials of the experiment  and observe the outcomes of each trial. Based on the frequency of each trial, we  can get the proababity

### Subjective Probability

* it is the intuitive belief about the probability of an event
* It can be apriori probability or a posteririori probability
* E.g. I feel there is about an 80% probability we can complete this task
* Different perceptions of different people may lead to different probabilities
* Subjective Probability may also lack continuity or coherence.
* Due to subjective interpretations, probabilities of all possible events in the sample space, when added individually, may not add up to 1.

## Axioms of Probability

Probability has three axioms:

1. Probability of an event must lie between 0 and 1, i.e 0 <= P(E) <= 1
2. A certain event has a probability of 1 and an impossible event has a probability of 0
3. Probability of the union of mutually exclusive events is equal to the sum of probabilities of the events taken seperately

## Conditional Probability

* It is the probability of an event B occuring, given an event A has occured
* The fact that another event A has occured can be proved or recorded by:
   - Assertion
   - Evidence
   - Presumption
   - Assumption
 
$$
P(A \mid B) = \frac{P(A \cap B)}{P(B)}
$$

## Bayes' Theorem

* It is an application of the conditional probabilities
* Conditions of Bayes' Theorem:
 - The Sample Space has mutually exclusive events $${A_1, A_2,...A_k}$$
 - Another event B exists with a non-zero probability (not impossible)

* Bayes Theorem is best understood with a question
----
You are going to camp on a mountain tomorrow. It usually snows heavily only about 5 days in December. There is a heavy snow forecast for tomorrow. However, the weather report is known to come with some inaccuracy. On 90% of the days with heavy snow, there was a forecast of heavy snow. On 10% of the days without heavy snow, there was a forecast of heavy snow. You don't have a tent that can withstand heavy snow. How likely are you to get stranded?

| Description | Formula | Value | Decimal |
|---|---|---|---|
| Probability of Heavy Snow | P(H) | 5/31 | 0.16129 |
| Probability of No Snow | P(N) | 26/31 | 0.83871 |

| Description | Formula | Value | Decimal |
|---|---|---|---|
| Probability of Weatherman Predicting Heavy Snow and it actually Snows Heavily | P(W \| H) | 90% | 0.9 |

| Description | Formula | Value | Decimal |
|---|---|---|---|
| Probability of Weatherman Predicting Heavy Snow and it does not Snow | P(W \| N) | 10% | 0.1 |

| Description | Formula | Value |
|---|---|---|
| Probability of Heavy Snow tomorrow | P(H \| W) | ? |

$$
P(H | W) = \frac{\text{ P(W | H) * P(H) }}{\text{ P(W | H) * P(H) + P(W | N) * P(N) }}
$$

On calculating you get Answer = 63.38% (High chance of Snow) 

---
