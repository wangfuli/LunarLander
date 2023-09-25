## Introduction

CS 7642: Reinforcement Learning and Decision Making -- Project 2

Author: Fuli Wang

The project aims to solve the Lunar Lander enviroment built in the OpenAI gym platform. Specifically, I use double DQN with experience reply to learn an agent.


## How to run the code

### Files
- `project2.ipynb`: My implementation using default hyperparameters, runing this file generates figures:
    - `train.jpg`: The training procedure
    - `test.jpg`: The testing result
    - `rolling100.jpg`: The average training reward of 100 consecutive episodes
    - `best_model.pth`: The saved best model, it is loaded and usesd to get the test result in `test.jpg`

-`tune_hiddendim.ipynb`: Tunning the hidden dimension of neural networks, running this file generates figure:
    - `tune_hiddendim.jpg`: the average training reward of 100 consecutive episodes for different hidden dimensions

-`tune_softw.ipynb`: Tunning the soft updating coefficient, running this file generates figure:
    - `tune_softw.jpg`: the average training reward of 100 consecutive episodes for different soft updating coefficients

-`tune_buffersize.ipynb`: Tunning the size of experience replay buffer, running this file generates figure:
    - `tune_buffer.jpg`: the average training reward of 100 consecutive episodes for different buffer sizes.



### Required dependencies
- numpy=1.18.0
- gym==0.17.2
- pandas
- matplotlib
- torch

### Running the code
The code can be by opening the four Jupyter Notebooks: `project2.ipynb`, `tune_hiddendim.ipynb`, `tune_softw.ipynb`, and `tune_buffersize.ipynb`, and runing them all. Replicated pictures will be shown after the last blocks

## About the replication
The implementation in `project2.ipynb` has no seed, so the replicated result could be different from my figuures. The implementation in the three hyperparameter tuning files has seed 0 for the environment, but could still experience different figures due to the randomness in epsilon greedy, and torch initialization.