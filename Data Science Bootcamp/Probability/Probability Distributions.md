# Probability Distributions

## Agenda

* What is Probability Distribution?
* Some Important Probability Distributions
* An example of each distribution
* Computing these distributions in R


## Uniform Distribution

* It is a simple, continuous and rectangular distribution
* Consider a set of numbers a and b where a < b, then:
  - Mean = $$\frac{\text{a+b}}{2}$$
  - Median = $$\frac{\text{a+b}}{2}$$
  - Variance = $$\frac{(b-a)^2}{12}$$
 
### Uniform Distribution in R

```r
dunif(c(1,2,3,4,5,6,7,8,9,10), min = 1, max = 10)
```
### Cumulative Uniform Distribution in R
```r
punif(c(1,2,3,4,5,6,7,8,9,10), min = 1, max = 10)
```

## Normal Distribution (Gaussian Distribution)

* It is characterized by the iconic **bell-shaped curve**
* This is because:
  - Most of the values are near the mean
  - The standard deviation is constant on both sides
* The Normal Distribution is an asymptotic curve, meaning it will always go near the X-axis, but will never truly touch the X-axis

### Normal Distribution in R

```r
dnorm(c(50, 60, 70, 80, 90, 100, 110, 120, 130, 140, 150), mean = 100, sd = 15)

```
### Cummulative Normal Distribution in R

```r
pnorm(c(50, 60, 70, 80, 90, 100, 110, 120, 130, 140, 150), mean = 100, sd = 15)

```
This is also an asymptotic curve.

### Example in R

On average, the milk yield per cow is 4.71kg per day. The standard deviation is 0.95kg.Find probability that the cow yields 3kgs of milk per day
 ```r
dnorm(3, mean = 4.71, sd = 0.95)
 >> 0.08310543
```
Probability is 8.31%.

What is the milk yield that can be suggested with a probability of 85%?

```r
qnorm(0.85, mean = 4.71, sd = 0.95)
>> 5.69
```
A cow will yield 5.69kg and this can be claimed with 85% probability.

## Binomial Distribution

* Here an experiment is repeated for n trials with replacement
* Each trial of the experiment has two possible outcomes: a success and a failure

$$
P(X = x) = \frac{n!}{x!(n-x)!} \, p^x (1-p)^{n-x}
$$

### Example in R

```r
dbinorm(0:10, 10, 0.5)
```
Example: A group of 20 people in a party were asked if they prefer red or white wine

What is the probability that at the party, 8 people preferred red wine.

```r
dbinom(8, size = 20, prob = 0.5)
>> 0.1201344
```
12.013% probability that 8 people preferred red wine

What is the probability that upto 10 people preferred red wine?

```r
pbinom(10, size = 20, prob = 0.5, lower.tail = TRUE)

>> 0.5880385
```
58.8% people in the party preferred white wine

## Poisson Distribution

 * It is concerned with the probability of a particular event occuring in a given interval
 * The assumption here is that the rate at which the event occurs is constant
 * An event is independent of future events
 * Probability of an event occuring depends on the length of that interval.
 * For extremely small intervals, the probability of an event occuring is almost 0
 * Interval doesn't necessary mean time. It can mean area, volume ,length

$$
P(X = x) = \frac{\lambda^x e^{-\lambda}}{x!}
$$

$$
\begin{array}{rl}
P(X = x) & \text{Probability of observing } x \text{ events} \\
x & \text{Number of occurrences/events} \\
\lambda & \text{Average rate (mean number of events)} \\
e & \text{Euler's constant } (\approx 2.71828) \\
x! & \text{Factorial of } x
\end{array}
$$

### Poission Distribution in R

```r
dpois(0:x, lambda = l)
```

```r
ppois(0:x, lambda = l)
```

## Exponential Distribution

* It is concerned with a Poisson Event occuring within a time interval.
* $$\lambda $$ is the rate at which this particular event occurs
* Poisson Events can be any kind of event, $$\lambda $$ can be any kind of event rate such as:
* - failure rate
  - death rate in a population
  - arrival rate in a ticket counter
 
### Example Question
A laptop can last about 1000 charge-discharge cycles. A person is about to go on a year-long holiday to Africa with his laptop. What is the chance that his laptop fails him. Assuming he goes through 180 charge discharge cycles through the trip?

Clearly this depends on the number of charge discharge cycles he has go through before the trip.

* However, this is a non-deterministic, random events.Therefore, this is a Possion Event
* The Rate of Failure is 1/1000
* P(failure) = pexp(180, 1/1000)
* Here we are interested in the probability of the laptop being reliable
*   - P(reliability) = 1- P(failure)

