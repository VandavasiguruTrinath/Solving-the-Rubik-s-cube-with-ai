# **Solving the Rubik’s cube with ai**





##### **Introduction**



**This project shows how a Deep Q-Network (DQN) can use reinforcement learning to learn how to solve a 2x2 Rubik's Cube.  The system is made up of an AI training engine (ai\_learner.py) that encodes cube states, chooses actions, calculates rewards, and updates the model through experience replay, as well as a custom cube environment (rubiks.py).  The objective is to demonstrate how an agent, independent of predetermined human algorithms, can enhance its problem-solving skills through trial-and-error interaction.  For educational and research purposes, this documentation describes how to operate, utilise, and expand the project.**



**rubiks.py — a custom-built Rubik’s Cube environment that simulates cube rotations, scrambling, and state representation.**



**ai\_learner.py — a reinforcement learning system that encodes cube states, selects actions via an ε-greedy policy, trains a DQN model using experience replay, and attempts to solve the cube through iterative learning.**



##### **Dependencies**



**The project requires the following libraries and tools:**



**Python Version**



**Python 3.8 or above**



**Core Libraries**



**Library			Purpose**

**NumPy			Matrix operations, cube face manipulation**

**PyTorch			Deep Q-Network (DQN), neural network training**

**Random / Time / Sys	Training control \& simulation**

**Collections (deque, namedtuple)	Experience Replay buffer**

**Signal			Safe interrupt handling during training**





##### **Usage**



**Displays a cube, rotates it, and scrambles it.**

**1.) Run the Cube Simulation (rubiks.py)**

    **python rubiks.py**

**2.) Train the Reinforcement Learning Agent (ai\_learner.py)**

    **Start DQN training:**

    **python ai\_learner.py**

**| Command      | Description                             |**

**| ------------ | --------------------------------------- |**

**| `--size=2`   | Choose cube size (2 recommended for RL) |**

**| `--layers=3` | Choose DQN depth: 2, 3, or 4 layers     |**

**| `--seed=123` | Use a fixed training seed               |**

**| `--random`   | Run without RL (random moves)           |**





##### 

##### **Performance**



**As training continues, the AI agent consistently improves, learning to rotate cubes more successfully and achieving higher correctness and reward scores.  The model successfully avoids redundant moves, stabilises learning through experience replay, and shows significant progress towards solving states, even though fully solving the 2x2 cube is still difficult because of sparse rewards and a large action space.  Longer training times, deeper networks, and GPU acceleration all improve overall performance.**



**ai.learner.py**

![alt text](image.png)

**rubicks.py**
![alt text](https://github.com/VandavasiguruTrinath/Solving-the-Rubik-s-cube-with-ai/blob/main/rubicpic.jpg?raw=true)













