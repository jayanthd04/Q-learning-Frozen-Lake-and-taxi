# Q-learning-Frozen-Lake-and-taxi

This repo is a simple implementation of Q-learning on OpenAI gym's FrozenLake and Taxi environments. 

## What is Q-learning? 
Q-learning is a simple value-based model that essentially learns what action is the best for each state. Q-learning works best for discrete action spaces and environments with finite states. We essentially maintain a Q-table which stores a value for each state, value pair. As we train our agent, we update these values to better represent the environment.

## Pre-requisites
```
pip install gym
```

```
pip install tqdm
```
