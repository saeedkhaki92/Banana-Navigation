# Banana Navigation


![Alt Text](Banana-Navigation/Images/banana-intro.gif

## Environment Details


In this project, we train an agent to navigate (and collect bananas) in a large, square world. A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. As such, the agent must collect yellow bananas as much as possible while avoiding the blue ones.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction:

Given this information, the agent has to learn how to best select actions. Four discrete actions are available :

* `0` move forward
* `1` move backward
* `2` turn left
* `3` turn right. 

The task is episodic, and in order to solve the environment, the agent must get an average score of +13 over 100 consecutive episodes.



## Getting Started

1. Download the environment that matches your operating system from <a href="https://github.com/udacity/deep-reinforcement-learning/blob/master/p1_navigation/README.md/" target="_blank">this link</a>.

2. Place the file in the DRLND GitHub repository, in the p1_navigation/ folder, and unzip the file. 

Python 3.6 should be installed on your machine to run the codes.


## Instructions

To train the your agent, you should run the Navigation.ipynb. There are 3 main cells there for training the agent:

1.  QNetwork which defines the architecture of the neural network

2.  DQN which difines the hyperparameters of the DQN algorithm

3.   dqn function which trains the agnet 
