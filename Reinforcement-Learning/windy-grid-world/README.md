## Project Description

Windy Grid World (Sutton & Barto, pg. 130,131)

<!-- Add an image -->
<img src="https://github.com/oamerl/machine-learning-projects/blob/main/Reinforcement-Learning/windy-grid-world/windy_grid_world.PNG" alt="windy grid world" width="500"/>


Considering the game depicted in the following above diagram, we are to implement the following algorithms to solve this problem:
1. Sarsa
2. Q-learning

We compare all solutions in terms of the optimal policies and episodes necessary for convergence and select the best values for 𝜀 and 𝛼 for each case.

We also re-solved the windy gridworld task with King’s moves, assuming that the effect of the wind, if there is any, is stochastic, sometimes varying by 1 from the mean values given for each column.
That is, a third of the time you move exactly according to these values, but also a third of the time you move one cell above that, and another third of the time you move one cell below that.
For example, if the agent is one cell to the right of the goal and it chooses to move left, then one-third of the time the agent will move one cell above the goal, one-third of the time you move two cells above the goal, and one-third of the time you move to the goal.

Mathematically, when the wind is defined by 𝑤, the location of the agent in 𝑦 after the execution of the action without stochastic wind will be 𝑦 = 𝑎(𝑠) + 𝑤. Then, the stochastic output 𝑦' will be:


<!-- Add an image -->
<img src="https://github.com/oamerl/machine-learning-projects/blob/main/Reinforcement-Learning/windy-grid-world/stochastic_y_prime.PNG" alt="windy grid world stochastic y" width="500"/>


