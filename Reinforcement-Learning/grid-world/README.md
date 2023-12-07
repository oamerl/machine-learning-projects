## Project Description

Consider the following grid in below image, in it, for all the states (cells in the grid), each one of the actions (north, south, east, and west) is chosen with probability 1/4. The agent then moves with probability 1 to the chosen direction.
While moving, if the agent hits a wall, it cannot move and it receives a reward of -1; if moving to a cell in the grid, the reward is 0.; if it reaches cell 𝐴 (1, 2), it moves to cell 𝐴′ (5, 2) and
receives a reward +10; and, if it reaches cell 𝐵 (1, 4) it moves to cell 𝐵′ (3, 4) and receives a reward +5.

In this project we wrote a program to find the state-value for each one of the states for discount rates 𝛾 ∈ {0.75, 0.85, 0.9}.

<!-- Add an image -->
<img src="https://github.com/oamerl/machine-learning-projects/blob/main/Reinforcement-Learning/grid-world/grid_world.PNG" alt="grid world" width="500"/>


