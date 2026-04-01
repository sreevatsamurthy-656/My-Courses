# MIT 6.S191
# Introduction to Deep Learning

## What is Deep Learning?

Before starting deep learning, we must first understand what intelligence and artificial intelligence are.

Intelligence is the ability to process information to make and inform future decisions. It is an innate ability of many living things at various levels. For Example:
1. A bee decides which flower to take nectar from based on the olfactory information it receives
2. A sunflower decides which direction to move based on the directional information of the sun
3. A person, like yourself, decides to take a course or not based on the information you receive

Artificial Intelligence, in the same line of thought, is the practice of building artificial algorithms to process information in order to make and inform of future decisions. 

Machine Learning is a subset of Artificial Intelligence. It mainly deals with designing a machine in such a way that it does not need to have explicit programming on how to process the information given. The machine learns to process the information by learning from the data provided

1. For example, Mailing services use Machine learning to detect spam mail. Instead of hardcoding rules by the programmer (like block these senders, etc.), the system learns from millions of emails of what looks like spam.

2. Streaming Platforms like Netflix and YouTube have movie and content recommendations personalized for the user (which is you). These recommendations are made by algorithms analyzing user watch history and user behavior 
This behavior of doing things isn’t that different from what normal living beings do. We also learn how to do some things or how to behave based on the information we receive, without even being related to social constructs.
3. For example, in animals like humans, monkeys, giraffes, elephants, etc. the young ones learn to differentiate between what is food and what is not by repeatedly observing others around them. There are some funny occurrences of this like how Tarzan or Mowgli, being in the company of animals, have adapted some of their behaviors.

4. Learning to recognize faces also works on a same principle. You repeatedly see a person’s face, you learn to differentiate him from others

5. Learning a language or skill also works in the same way.  You learn to work with it in the real world, like talking to people or doing a project or solving problems, you will learn to pick up patterns and structures over time. That is why practicing a skill is an essential advice given to people to master a skill.

Deep Learning is a subset of machine learning which makes use of neural networks (specifically, deep neural networks) in order to learn from data and make future decisions

In a nutshell, this entire field is all about teaching computers how to learn a task directly from raw data.


## Why Deep Learning and Why Now? 

### Why are we learning Deep Learning?
Deep learning isn’t just using a fancy apparatus and architecture to study machine learning
So a disadvantage of Traditional Machine Learning Algorithms is that we need to have a sort of human intervention in building the model. This is mainly about things like  hand engineering the model’s features. It is not exactly  having a machine as intelligent if we are having a human determine what features to look at.  

Deep learning has an edge in this regard as the machine is able to directly learn the features to look at from the data that is given. These features are observed by the network in a hierarchical fashion.
Let us take face recognition as an example.
Thinking in absolute basic, low-level steps. If a human is presented with a image to look at, he/she looks at:
1. The lines, edges and shades in an image (Low-Level Features)
2. Then these features are composed together. We then observe if these features are those present usually on a face like eyes, ears, nose, etc. (Mid-Level Features)
3. Then you look at the configuration of these features in the image to see if there is a face (High Level Features)

So, as you can see, there is a hierarchical order to observe the features.

Similar to the human interpretation, neural networks also do the three steps given:
1. It looks at the low-level features in the image like lines, edges, etc.
2. It then composes these into things like corners, curves and shapes. They form the features of the model
3. These corners and curves are then looked into to see if we have a face or not.

Note: The shapes or corners are not necessarily things like nose, ears, etc. that we see. They can be anything...it is what the neural network 'sees' or 'observes' after going through millions of images. 

### Why are we learning Neural Networks and Deep Learning Now?

If you notice the timeline, we see that a lot of the concepts and algorithms in deep learning have existed since the 1950s or 70s. For example:

* Gradient Descent was developed in 1952
* The Perceptron was developed in 1958
* Backpropogation was developed in 1986
* Deep Convolutional Neural Networks were developed in 1995

1. Big Data
   - Deep Learning algorithms develop and thrive on huge amounts of data
   - In the current world, there is a massive amount of data available to use, comprehend, and store for various purposes

2. Hardware
   - There are inexpensive devices available in the market that can store huge amounts of data like 1 TB
   - Companies like AMD and Nvidia are providing new Graphical Processing Units (GPUs) that accelerate parallel computing, which subsequently parallelizes the deployment and development of Deep Neural Networks

3. Software
   - In the past couple of years, different kinds of software like TensorFlow, PyTorch, and JAX were developed which support building deep neural networks
   - These software tools allow us to democratize the ability to create, train, and deploy these models on a very large scale
## Perceptron

It is THE MOST basic building block of a neural network. It is very important to understand while doing deep learning


At the basic level, the goal of the neuron is to take m inputs and create some output.

The steps involved in the working of a perceptron are:
1. Take each of the inputs $$x_1, x_2, x_3...x_m$$ and multiply each of them by some corresponding weight $$w_1, w_2, w_3...w_m$$ 
2. Then take these products and add them up (i.e. Make a linear equation)
3. Then this sum is passed through an activation function to yield an output

An Activation Function is, simply put, a transformation. It is a non-linear transformation which converts the linear equation into a non-linear output

Simply put, the perceptron does this
a. Make a linear equation of the inputs
b. Pass it through a non-linear transformation to yield an output.

### Why we use an activation function?

The output of the first stage of a perceptron is a linear output. There is a linear relationship between input and output. But in reality, there is very rarely a linear relationship between the input and output. So, a non-lineariy has to be introduced. That is where the activation function comes in.

Mathematically, it is written as:

$$
\hat{y} = g\Bigg( \sum_{i=1}^{m} x_i w_i \Bigg)
$$

In addition to this, there is also a bias term $$w_0$$  in the linear eqaution. It shifts the linear combination to a certain direction in the m-dimensional feature space, keeping the decision boundary away from the origin

Now, expressing this in Matrix Form, we get:

$$
\hat{y} = g\left(w_0 + X^T W\right)
$$

where \(X\) is the input feature vector,

$$
X = 
\begin{bmatrix}
x_1 \\
x_2 \\
\vdots \\
x_m
\end{bmatrix}
$$

and \(W\) is the weight vector,

$$
W =
\begin{bmatrix}
w_1 \\
w_2 \\
\vdots \\
w_m
\end{bmatrix}
$$

Thus,

$$
X^T W = x_1 w_1 + x_2 w_2 + \dots + x_m w_m
$$

and $$\(g(\cdot)\)$$ is the perceptron activation function.

![Perceptron Diagram](https://raw.githubusercontent.com/sreevatsamurthy-656/My-Courses/main/MIT%20Introduction%20to%20Deep%20Learning%20%7C%206.S191/pictures/perceptron.png)

Some commonly used activation functions are:

### Sigmoid Function

$$
g(z) = \frac{1}{1 + e^{-z}}
$$

The sigmoid function maps the input to a value between 0 and 1.

### Tanh Function

$$
g(z) = \tanh(z)
$$

or equivalently,

$$
g(z) = \frac{e^z - e^{-z}}{e^z + e^{-z}}
$$

The tanh function maps the input to a value between -1 and 1.

### ReLU Function

$$
g(z) =
\begin{cases}
z, & z > 0 \\
0, & z \leq 0
\end{cases}
$$

ReLU outputs the input directly if it is positive; otherwise, it outputs 0.

### Leaky ReLU Function

$$
g(z) =
\begin{cases}
z, & z > 0 \\
\alpha z, & z \leq 0
\end{cases}
$$

where $$\(\alpha\)$$ is a small constant such as 0.01.

### Softmax Function

For a vector input \(z\),

$$
g(z_i) = \frac{e^{z_i}}{\sum_{j=1}^{n} e^{z_j}}
$$

Softmax converts the input values into probabilities that sum to 1.

![Activation Functions](https://raw.githubusercontent.com/sreevatsamurthy-656/My-Courses/main/MIT%20Introduction%20to%20Deep%20Learning%20%7C%206.S191/pictures/activation-functions.png)

## Building Neural Networks using Perceptrons

A simplified depiction of the perceptron is as follows


![Simplified Perceptron](https://raw.githubusercontent.com/sreevatsamurthy-656/My-Courses/main/MIT%20Introduction%20to%20Deep%20Learning%20%7C%206.S191/pictures/perceptron-simplified.png)

Here the variable 'z' refers to the linear combination of the inputs and the bias terms

Now there can be more than one output and each output has its own set of weights for the output it gives. This is called a multi-output perceptron

![Activation Functions](https://raw.githubusercontent.com/sreevatsamurthy-656/My-Courses/main/MIT%20Introduction%20to%20Deep%20Learning%20%7C%206.S191/pictures/multi-output-perceptron.png)

Now we add a **layer** to this perceptron (multi and/or Simple Perceptron, either works)

![Activation Functions](https://raw.githubusercontent.com/sreevatsamurthy-656/My-Courses/main/MIT%20Introduction%20to%20Deep%20Learning%20%7C%206.S191/pictures/multi-output-perceptron-layer.png)

## Applying Neural Networks

Because all the inputs are densely connected to all outputs, these layers are called **Dense** layers

Now you can add further layers. Here is an image of a deep neural network with the connections very much abstracted for simplicity

![Activation Functions](https://raw.githubusercontent.com/sreevatsamurthy-656/My-Courses/main/MIT%20Introduction%20to%20Deep%20Learning%20%7C%206.S191/pictures/deep-neural-networks.png)

## Loss, Loss Functions and Gradient Descent

So let us take an example scenario where we are using a neural network model to predict something. For example, predicting the price of a house depending on various parameters like house area, location, weather, number of bedrooms, years since construction, etc.

So, given that we have a previous record of the house price and the parameters like:

| House Area (sq ft) | Location      | Weather | Bedrooms | Years Since Construction | Price ($) |
|--------------------|---------------|----------|-----------|--------------------------|---------------------|
| 1200               | Urban         | Sunny    | 2         | 5                        | 250,000             |
| 1800               | Suburban      | Rainy    | 3         | 10                       | 320,000             |
| 2500               | Urban         | Cloudy   | 4         | 2                        | 500,000             |
| 900                | Rural         | Sunny    | 2         | 20                       | 150,000             |
| 3000               | Urban         | Rainy    | 5         | 1                        | 650,000             |

So we know that for a 5 year-old house of area 1200 sq.ft, in an urban area, with a sunny weather and 2 bedrooms, its price it was purchased for was $250,000. 

This value - the Price of $250,000 which is an actual, real-world value, is called the **true value** .

Now, suppose we have 3 neural networks we have designed to predict house prices. Now the weights and stuff, we have put it based on some calculations, let's assume. 

1. The first network, when it is fed the values 1200 sq ft, Urban area, Sunny weather, 2 bedrooms and 5 year old house -> It tells that the price of the house can be $247,549

2. The second network, when it is fed the same parameters on House Area, Location, Weather, Bedrooms and Years since Construction -> It tells us that the price of the house can be $559,345

3. The third network, when it is fed the same parameters on House Area, Location, Weather, Bedrooms and Years since Construction -> It tells us that the price of the house can be $124,569

The prices told by the the three networks are called **predicted values** . As the name suggests, it is the value predicted by the neural network.

Now, whether you look at it from the buyer or seller point of view, both parties will agree to have the house to be priced according to how previous houses of the same kind were purchased.

That is true for most scenarios. To put it in the Machine Learning Terminology, the closer the predicted values are to the true values, the better the model is. 

So how do we make such a model?

We can't obviously tune the parameters ourselves. That defeats the whole purpose of Machine Learning. The way we do this is by something called **Gradient Descent**

In simple terms, Gradient Descent means that a model looks at how different the predicted values are from the true values, and then it modifies its weights in a way such that the difference gets reduced.

So how is the difference between the predicted and true values observed?

It is done by measuring the **loss** of the network

The loss of a network measures the cost incurred from incorrect predictions.

The loss of a network is measured by a **loss function**. A general depiction is given by:

$$
\mathscr{L}\left(f\left(x^{(i)}; W\right), y^{(i)}\right)
$$

