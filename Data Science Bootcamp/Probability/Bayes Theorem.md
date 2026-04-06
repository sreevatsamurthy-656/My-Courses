# Bayes Theorem

## Agenda

* Define Bayes Theorem
* Give Examples of Bayes Theorem

## Definition

* Let S be the Sample Space
* Let S be divided into k disjoint events $A_1, A_2, A_3 \dots A_k$ with respective probabilities $P(A_1), P(A_2), P(A_3), \dots P(A_k)$
* Let B be an event common to all k disjoint events

![Bayes Theorem](https://raw.githubusercontent.com/sreevatsamurthy-656/My-Courses/main/Data%20Science%20Bootcamp/Probability/images/bayes_theorem.png)

This can be defined as:

$$
P(A_i \mid B) =
\frac{P(B \mid A_i) P(A_i)}
{\sum_{j=1}^{k} P(B \mid A_j) P(A_j)}
$$

Here:

$$
\begin{array}{rl}
P(A_i \mid B) & \text{Posterior probability} \\
P(A_i) & \text{Prior (a priori) probability} \\
P(B \mid A_i) & \text{Likelihood} \\
\sum_{j=1}^{k} P(B \mid A_j) P(A_j) & \text{Evidence}
\end{array}
$$


# Conditional Probability

* It is the probability that one event happens given that another event is already known to have happened

* Denoted by P(A|B)

$$
P(A \mid B) = \frac{P(A \cap B)}{P(B)}
$$

## Conditional Probability and Independent Events

Independent Events are those pair of events which:

* neither event is affected by the occurance of the other
* occurnace of one event does not change the probability of the occurance of the others event 
