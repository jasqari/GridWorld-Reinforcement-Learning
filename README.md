# Reinforcement Learning in 2D Grid World
<p align="center">
 <img src="https://github.com/jasqari/GridWorld-Reinforcement-Learning/assets/44480584/307890e2-4f24-4fa2-9c0b-3395500ca049" width="50%" height="50%"/>
</p>

## Overview
This repository provides Python implementations of some of the reinforcement learning methods and simulations of agents based on these methods in a 2D grid world.
* `Algorithms/` contains the implementations of methods,
* `Grid.py` defines the 2D grid world object class and is the tool to simulate the environment,
* `main.py` is a framework that finds and saves optimal values, runs simulations in the environment, etc.

Refer to [Sutton & Barto 2018](http://incompleteideas.net/book/the-book-2nd.html) for more information.

## Requirements
```
pip3 install -r requirements.txt
```

## Usage
See the full list of options:
```
python3 main.py -h
```

Choose the grid world size and RL algorithm:
```
python3 main.py 8 mc
```

Provide initial state like 'row,col' and goal states in the form of 'row1,col1-row2,col2-...':
```
python3 main.py 5 sarsa --init_state 0,4 --goal_states 3,0-4,0
```

Tune some of the parameters:
```
python3 main.py 8 val_iter --N 200 --gamma 0.9 
```
```
python3 main.py 5 ql --N 500 --epsilon 0.9 --gamma 0.7 --alpha 0.6
```

Simulate an episode and display the agent's path:
```
python3 main.py 5 dql --simulate
```

