# Acknowledgement : This project is motivated from Course : CS188 : Introduction to Artificial Intelligence - UC Berkeley.
# Starter code : Project 3 : Reinforcement Learning, CS188 - UC Berkeley. Link : https://inst.eecs.berkeley.edu/~cs188/fa22/projects/proj3/
In this project, you will implement value iteration and Q-learning.
You will test your agents first on Gridworld (from class), then apply them to a simulated robot controller (Crawler) and Pacman.

**Files editted** : 
+ valueIterationAgents.py	A value iteration agent for solving known MDPs.
+ qlearningAgents.py	Q-learning agents for Gridworld, Crawler and Pacman.
+ analysis.py	A file to put your answers to questions given in the project.

**Question 1 : Value Iteration :**

Write a value iteration agent in ValueIterationAgent, which has been partially specified for you in valueIterationAgents.py. 

Your value iteration agent is an offline planner, not a reinforcement learning agent
, and so the relevant training option is the number of iterations of value iteration it should run (option -i) in its initial planning phase. 

ValueIterationAgent takes an MDP on construction and runs value iteration for the specified number of iterations before the constructor returns.

**Question 2 : Policies**

Consider the DiscountGrid layout, shown below. 

This grid has two terminal states with positive payoff (in the middle row), a close exit with payoff +1 and a distant exit with payoff +10.

The bottom row of the grid consists of terminal states with negative payoff (shown in red); each state in this “cliff” region has payoff -10. 

The starting state is the yellow square.

**Question 3 : Q-Learning**

Note that your value iteration agent does not actually learn from experience. 

Rather, it ponders its MDP model to arrive at a complete policy before ever interacting with a real environment. 

When it does interact with the environment, it simply follows the precomputed policy (e.g. it becomes a reflex agent).

This distinction may be subtle in a simulated environment like a Gridword, but it’s very important in the real world, where the real MDP is not available.
