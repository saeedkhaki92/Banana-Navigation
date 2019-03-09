# Project Report


## Introduction

Reinforcement learning is a branch of machine learning which trains an agent to make optimal decisions only through interactions with environment. The goal of reinforcement learning agent is to find the optimal action-value function and then act according to these action-value function to maximize the expected discounted cumulative reward.\\

In general, there are two ways to find the q-value function: (1) lookup table (2) function approximation. The lookup table is suitable for discrete state spaces and is not practical when the number of states are large. The function approximation method is well-suited for continuous action spaces which is able to approximate the action value function very well. However, they are hard to train.

In this project, we used Q-learning algorithm (deep Q-network) to approximate the Q-value function. The deep Q-network uses the following two techniques to help the neural network converge to the correct Q-value function:


1. experience replay
2. item fixed Q-target
\end{enumerate}

Experience replay breaks the time correlation between samples and prevents the network from diverging. Fixed Q-target helps the network to converge by using previous fixed weights for computing Q-targets.


In this project, we used a vanilla DQN as in the originl paper, but we did not use image frames as state. So, we replaced the convolutional neural networks with a fully-conntected neural networks.

## Q-network


The Q-network that was used in this project was a fully-connected neural network with 3 hidden layers, each having 40 neurons. The Relu activation functions was used for all layers except the output layer which had linear activation function. Following figure shows the modeling structure of the Q-network.

![Alt Text](https://github.com/saeedkhaki92/Banana-Navigation/blob/master/Images/nn.jpg)

## DQN Hyperparameters


* batch size of 32
* buffer size of 100,000
* learning rate of 0.0005
* soft update learning rate of 0.001
* updated the network every 8 time steps
* discount factor of 0.99
* maximum number of episode of 4000
* minimum epsilon of 0.01
* epsilon decay rate of 0.999
* epsilon start point of 1.0
* maximum number of time step of 1000

## Results


We trained the agent using DQN algorithm on GPU and it took about 0.5 hours to be trained. The DQN model solved the problem in 1791 episodes, and scored above 13.01 in 100 episodes. Following figure shows the average score plot.




