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

## About the FrozenLake-v1 environment
The FrozenLake environment is a 4x4 grid. The goal of our agent is to reach the bottom right corner of the grid where ther is a treasure chest while avoiding the holes. The agent can move left, down, right or up. If the agent reaches the treasure chest, a reward of +1 is received, while a reward of +0 is given if the agent hits a hole or moves to a frozen block of water. 

## About the Taxi-v3 environment
The taxi environment is also a grid environment where there are four designated locations designated by the colors Red, Green, Yellow, and Blue. The passenger starts the episode at a random location on designated locations and has a destination at one of the other designated locations, while the taxi starts at a random location on the grid and has to pick up the passenger from their pickup location and drop them off at their dropoff location. The taxi can start at 25 different locations and since there are 5 different locations for the the pickup location and 4 different locations for the dropoff location, there are 500 unique discrete states in the environment. The taxi can move left, right, up, down, pickup and dropoff the passenger. The agent is rewarded with -1 reward at each step, +20 for dropping off the passenger and -10 for attempting to pickup a passenger where there is none or dropping off the passenger at a wrong location. 

## FrozenLake-v1 Results 
My simple Q-learning model was able to reach the treausre chest after just 10,000 training episodes. 

## Taxi-v3 Results
After training for just 25,000 episodes, my model was able to receive an average score of 7.4 with a standard deviation of 2.79. This means that on average, our model takes around 12 steps to pickup and drop off the passenger. 
