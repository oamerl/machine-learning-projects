## Project Descriptipn

### Introduction

The Taxi-v3 game is a classic reinforcement learning environment provided by OpenAI Gym, it is a discrete, episodic, and fully observable environment where an agent has to navigate a taxi through a grid-like environment to pick up and drop off passengers.

Although its relatively a simple task but it carries the essence of many real-world problems in which it can be applied and thus provides an excellent testing ground for reinforcement learning models as it mimics real-world challenges, making it an excellent platform for solving problems related to logistics, navigation, resource allocation, autonomous vehicles, robotics, delivery services, and even traffic management as the taxi must learn to navigate the quickest routes, avoid potential barriers and consistently reach its goal.

The aim of this project is to implement different reinforcement learning algorithms such as SARSA, Q-Learning, Double Q-Learning and DQN that can solve this game, and to evaluate its performance by measuring the agent's average reward and the number of steps taken to complete each episode.


### Problem Formulation

The main objective of this project is to develop and train a reinforcement learning agent that can solve the Taxi-v3 game by efficiently navigating the taxi to pick up and drop off passengers. Additionally, the project aims to evaluate the performance of the algorithm by measuring the agent's average reward and the number of steps taken per episode. Beginning from a randomly selected state, our task is to guide the taxi to the location of the passenger, pick up the passenger, travel to the desired destination, and drop off the passenger, after which the episode terminates.

The agent receives a positive reward of +20 for successfully dropping off the passenger at the correct location. Negative reward of -10 for incorrect attempts to pick-up/drop-off passenger and negative reward of -1 for each step where another reward is not received.

The grid contains four specific locations marked by colors: Red corresponds to 0, Green to 1, Yellow to 2, and Blue to 3. For example, for the below Figure 1, The Red denotes the pickup spot while the Blue represents the drop-off point.


<!-- Add an image -->
<img src="https://github.com/oamerl/machine-learning-projects/blob/main/Reinforcement-Learning/taxi-v3-game-environment/openai_taxi_v3_env.png" alt="taxi v3 env" width="500"/>



The state space in this environment is a combination of several elements:
* Taxi Location: This represents the current (row, column) location of the taxi in the 5x5 grid, which can be any of 25 possible values (5 rows * 5 columns).
* Passenger Location: This represents the current location of the passenger. There are five possible values - four representing the passenger being at one of the four specific locations, and one representing the passenger being inside the taxi.
* Destination Location: This represents the target drop-off location. There are four possible locations where the passenger wishes to be dropped off.
* When we combine all of these, we get a total state space of 500 states (5 taxi rows * 5 taxi columns * 5 passenger locations * 4 destinations = 500)


The Action Space
* Move South: The taxi moves down in the grid.
* Move North: The taxi moves up in the grid.
* Move East: The taxi moves to the right in the grid.
* Move West: The taxi moves to the left in the grid.
* Pickup: The taxi attempts to pick up a passenger. This is only successful if the taxi is in the same cell as the passenger and the passenger is not yet in the taxi.
* Drop-off: The taxi attempts to drop off the passenger. This is only successful if the taxi is in the same cell as the destination and the passenger is in the taxi.


For the Taxi problem, we assessed different RL algorithms such as SRASA, Q-Learning, Double Q-Learning and DQN. Below we mention some of the evaluation metrics which we used.
* Average Rewards Per Episode.
* Number of Timesteps per Trip (learning to complete the trip in the least amount of time steps.)

