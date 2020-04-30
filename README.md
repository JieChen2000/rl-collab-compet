[//]: # (Image References)

[image1]: tennis.png "Trained Agent"

# Collaboration Competetion RL Example

## Introduction

For this project, we work with the [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis) environment.

![Trained Agent][image1]

In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.
The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

### Solving the Environment

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,
After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
This yields a single score for each episode.
The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.

## Enviroment Setup

The code is written in PyTorch and Python 3.

1.Clone this repo by
* git clone https://github.com/JieChen2000/rl-collab-compet.git

2.Current code is tested with the Unity Machine Learning Agents (ML-Agents) tennis environment on windows 64-bit operating system, download the enviroment
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)

3.Place the file in the this GitHub repository, and unzip (or decompress) the file.

4.Install openai gym, which is required by ML-Agents.

* `git clone https://github.com/openai/gym.git`
* `cd gym`
* `pip install -e .`

5.Install udacity git repo with unityAgent enviroment.

* `git clone https://github.com/udacity/deep-reinforcement-learning.git`
* `cd deep-reinforcement-learning/python`
* `conda install pytorch=0.4.0 -c pytorch`  
* `pip install .`  

## Running Instructions

* `python train_agent.py`
* `python run_agent.py`  //this will call the trained model and run the smart agent to interact with enviroment.

## Demo and Algorithm Description

The report `report.ipynb` describes the learning algorithm, along with the chosen hyperparameters. It also describes the model architectures. A plot of rewards per episode is included to illustrate that the agent is able to receive an average reward of at least +0.5 over 100 episodes.
