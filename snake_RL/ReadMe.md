# DQN-based Snake Game Training
This repository highlights our implementation of a Deep Q-Learning Network (DQN) to train an AI to play the classic Snake game. The primary objective is to investigate the effectiveness of reinforcement learning techniques, specifically DQN, in mastering such games.

## Overview
The Snake game, a popular classic, involves navigating a snake on a grid to eat apples. The snake grows longer with each apple consumed, making the game more challenging. A game over occurs when the snake collides with the grid's wall or itself.

In this project, we have:

- Defined the Snake game's environment, including setting rewards and penalties for different outcomes.
- Implemented a DQN agent with its neural network, experience replay buffer, and various essential methods for learning and decision-making.
- Established training routines, visualizations, and statistics gathering to monitor the agent's performance and growth.
- Encoded the game's state into a tensor format suitable for neural network input.
## Results
After rigorous training episodes, our DQN agent showcases significant progress in mastering the Snake game.

### Snake's Movement in Early Training:

image

### Snake's Movement After Extended Training:

image

### Training Statistics:

image

## Future Work
Potential enhancements and investigations include:

Implementing Double DQN or Dueling DQN to evaluate potential performance improvements.
Investigating the impact of various reward schemes on learning speed and final performance.
Exploring the agent's behavior under different grid sizes or challenging game modifications.
Incorporating advanced exploration strategies like Noisy Networks or Bayesian Neural Networks.
Evaluating transfer learning opportunities to see if a trained agent can adapt to new environments faster.
## Acknowledgements
We would like to express our appreciation to the original creators of the Snake game. It has not only provided entertainment for generations but also serves as an intriguing environment for AI and ML experimentation.

Usage
To engage with the code and potentially train your own agents:

1. Initialize the game's configuration in the global settings section.
2. Run the main script to train the agent and visualize the results.
We encourage community participation! Fork the repository, raise issues, or propose changes. Contributions, insights, and feedback are always welcome!
