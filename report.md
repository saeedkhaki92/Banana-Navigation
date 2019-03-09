# Project Report


## Introduction

Reinforcement learning is a branch of machine learning which trains an agent to make optimal decisions only through interactions with environment. The goal of reinforcement learning agent is to find the optimal action-value function and then act according to these action-value function to maximize the expected discounted cumulative reward.\\

In general, there are two ways to find the q-value function: (1) lookup table (2) function approximation. The lookup table is suitable for discrete state spaces and is not practical when the number of states are large. The function approximation method is well-suited for continuous action spaces which is able to approximate the action value function very well. However, they are hard to train.

In this project, we used Q-learning algorithm (deep Q-network) to approximate the Q-value function. The deep Q-network uses the following two techniques to help the neural network converge to the correct Q-value function:

\begin{enumerate}
\item experience replay
\item fixed Q-target
\end{enumerate}

Experience replay breaks the time correlation between samples and prevents the network from diverging. Fixed Q-target helps the network to converge by using previous fixed weights for computing Q-targets.


In this project, we used a vanilla DQN as in the originl paper, but we did not use image frames as state. So, we replaced the convolutional neural networks with a fully-conntected neural networks.

## Q-network
