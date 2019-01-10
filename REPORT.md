# Project 2: Continuous Control - Report

### Learning Algorithm

Basically I used [DDPG(Deep Deterministic Policy Gradients) in ddpg-pendulum from Udacity DRLND Repo](<https://github.com/udacity/deep-reinforcement-learning/tree/master/ddpg-pendulum>). Because DDPG can be used for continous action, it compensates for the disadvantages of DQN.
DDPG uses two pairs of networks, Actor and Critic. *The Actor-Critic learning algorithm is used to represent the policy function independently of the value function. The policy function structure is known as the actor, and the value function structure is referred to as the critic.* (from [link](<https://pemami4911.github.io/blog/2016/08/21/ddpg-rl.html>))
Each pair consists of a Regular network and a Target network, like DQN. DQN is updated at regular time steps from regular network to target network at one time, but DDPG updates little by 0.01% in a way called soft update.


### Plot of Rewards

I struggled about a week for this project. At first I tried first version, but it never got over 20 points for four days. So I switched to second version, and I passed 20 very easily but I needed hyperparametric tuning to get to the project goal of average 30 points over 100 runs.

![](<plot_of_reward.png>)


### Future Work

Reinforcement learning is very unstable, it very often lost its ways on training, even [it diverges after finding solution](<https://www.reddit.com/r/MachineLearning/comments/8pcykb/d_actor_critic_ddpg_diverging_after_finding/>). For more stable result, I can try this things.

* [Hyperparameter optimization](<https://en.wikipedia.org/wiki/Hyperparameter_optimization>) : Some Hyperparameter is more stable than others. There are many hyperparameters in machine learning, so we should find good enough but save our time. There are some search algorithms for these work - grid search, random search, bayesian optimization, gradient-based optimization, evolutionary optimization, and so on.

* [add parametric noise](<https://blog.openai.com/better-exploration-with-parameter-noise/>) : According to Deepmind, adding adaptive noise to the parameters of reinforcement learning algorithms frequently boosts performance. In this code I just added action noise but not parametric noise.

![](<p_diag_1.png>)
