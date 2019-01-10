# Project 2: Continuous Control

### Project Details

For this project, you will work with the [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment.

![Trained Agent](<https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif>)

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

We used 20 identical agents, each with its own copy of the environment. State and Action spaces are continuous, and we used [DDPG](<https://arxiv.org/abs/1509.02971>) algorithm.


### Getting Started

This codes basically from [Udacity Deep Reinforcement Learning Nanodegree program repo](https://github.com/udacity/deep-reinforcement-learning/). Below from README.md in drlnd repo.

------
To set up your python environment to run the code in this repository, follow the instructions below.

1. Create (and activate) a new environment with Python 3.6.

	- __Linux__ or __Mac__:
	```bash
	conda create --name drlnd python=3.6
	source activate drlnd
	```
	- __Windows__:
	```bash
	conda create --name drlnd python=3.6
	activate drlnd
	```

2. Follow the instructions in [this repository](https://github.com/openai/gym) to perform a minimal install of OpenAI gym.  
	- Next, install the **classic control** environment group by following the instructions [here](https://github.com/openai/gym#classic-control).
	- Then, install the **box2d** environment group by following the instructions [here](https://github.com/openai/gym#box2d).

3. Clone the repository (if you haven't already!), and navigate to the `python/` folder.  Then, install several dependencies.
```bash
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
```

4. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment.  
```bash
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

5. Before running code in a notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu.

![](<https://user-images.githubusercontent.com/10624937/42386929-76f671f0-8106-11e8-9376-f17da2ae852e.png>)

### Instructions

You don't have to run all codes. just run necessary blocks of code.
At first, run '1. Start the Environment' block. and next, run all below '4. It's Your Turn!' block. The training time varies, so we should try many times or apply one of two proposes of *Future works*.
