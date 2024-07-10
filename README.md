This project implements a Deep Q-Learning (DQL) agent to play the Lunar Lander game from OpenAI Gym's classic control environments. The code trains a neural network to learn the optimal policy for landing the Lunar Lander safely on the moon's surface.
  
Introduction:

The Lunar Lander environment involves controlling a spaceship to land safely on the moon. The agent receives rewards based on its actions that lead to a successful landing, and penalties for crashing or flying out of bounds. The objective is to train a DQL agent to maximize the cumulative rewards.

Training Details:

The agent is implemented using a neural network with two hidden layers. The key components include:

Network: A neural network model with input, hidden, and output layers.
Replay Memory: A buffer to store and sample past experiences.
Agent: The DQL agent responsible for interacting with the environment, storing experiences, and learning from them.
Hyperparameters
Learning rate: 0.0005,
Minibatch size: 100,
Discount factor: 0.99,
Replay buffer size: 100.000,
Interpolation parameter for soft updates: 0.001,

Training Process:

The agent is trained for up to 2000 episodes, with an epsilon-greedy policy for action selection. The epsilon value starts at 1.0 and decays to 0.01 over time. The training loop involves:

Selecting an action based on the current state.
Executing the action in the environment.
Storing the experience in replay memory.
Sampling a random batch from the memory to learn from.
Updating the network weights using the Bellman equation.

Results:

The agent aims to solve the environment by achieving an average score of 200 over 100 consecutive episodes. The training process prints the average score every 100 episodes.

