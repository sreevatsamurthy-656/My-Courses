# MIT 6.S.191
# Deep Sequence Modelling

## Introduction

* So in the previous lecture, we discussed the idea of deep neural networks and we got an intuition of how it works
* So, in that lecture, we learnt about a class of neural network models called as **feed-forward models**
* So when we turn towards processing of sequential data, (i.e. data that is resolved in time) we have a different way of thinking about the model paradigm
* In this lecture, we will discuss the intuition and model framework required for sequential processing from the ground up

## Intuition

Suppose we have a ball in a space (Imagine the ball you use to play itself).

Now if I give you the ball's picture currently, can you predict where the ball will go next?

No. You cannot.

The ball may go up, down, left or right, any direction! There is no way you can use **just** the current picture of the ball to predict its next position.

However, if I give a series of pictures, which show you how the position of the ball changed **with time**, it is a trivial task to predict the next position of the ball 

That is sequence modelling in a nutshell.

## Examples of Sequential Data

Sequential Data is all around us. Some examples of sequential data are:

1. Audio Signals
2. Text data, which can be:
   > a. A sequence of words
   > b. A sequence of letters
3. Medical Signals
4. Stock Values
5. DNA Sequences
6. Videos
7. Movement Signals
8. Weather

## Sequence Modelling Applications

1. One-to-One (E.g. Binary Classification)
2. Many-to-One (E.g. Sentiment Classification)
3. One-to-Many (E.g. Image Classification)
4. Many-to-Many (E.g. Machine Translation)

## Neurons with Recurrence

**Recurrence** - The act of something happening again, reappearing or returning after a period of absence

So when we look at the **perceptrons** used in the initial feed-forward models, we see the following steps:

1. We take in the inputs
2. We multiply the inputs by weights and get their linear combination
3. We apply a non-linearity on the weights to get our output

When we take the **feed-forward neural network** as a whole, we are simply stacking up perceptrons in a layer to get a multi-dimensional output.

So, to introduce the recurrence concept here we will collapse and simplify the feed-forward models to 3 things:

1. Input Block (*x<sub>t</sub>*)
2. Neural Network Block
3. Output Block (*ŷ<sub>t</sub>*)

So here we are using x<sub>t</sub> and ŷ<sub>t</sub> because it is the input and output for time instance t

Now taking individual time-stamps, we have the following image

![Individual Timestamps]([https://raw.githubusercontent.com/sreevatsamurthy-656/My-Courses/main/MIT%20Introduction%20to%20Deep%20Learning%20%7C%206.S191/pictures/perceptron-simplified.png](https://github.com/sreevatsamurthy-656/My-Courses/blob/main/MIT%20Introduction%20to%20Deep%20Learning%20%7C%206.S191/pictures/Handling_individual_time_steps.png))

If we take the input at each instant and keep predicting, that is what the diagram shows. However, the problem here to look at is that the sequential relation between the input time series at each time step is not captured and utilized by the model.

This is where the **hidden state** variable comes in represented by h<sub>t</sub>

It is a representation of the state of the neural network block at time instance t

It basically links whatever the networks computes at the **present instant** to the **past history** of the neural network

It is essentially giving the neural network system the aspect of **memory**
