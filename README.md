[//]: # (Image References)

[image1]: agent.gif "Trained Agent"

# Project : Deep Navigation

### Introduction

In this `Navigation.ipynb` jupyter notebook, I have trained a agent using deep reinforcement learning especially the DQN techinique to collect the yellow bananas and avoid the blue bananas. The environment is built using unity.

![Trained Agent][image1]

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of this agent is to collect as many yellow bananas as possible while avoiding blue bananas. I used Experience replay to avoid the corellation obtained if sampling is done sequentially and fixed q targets are also used to avoid the noise and boost the training speed.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

### Getting Started

1. Download the environment from one of the links below and place it in this directory.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.
2. Edit this line in navigation.ipynb to point to the dowloaded binaries.
   ```
   env = UnityEnvironment(file_name="F:/Jupyter/deep-reinforcement-learning/Deep Navigation/Banana_Windows_x86_64/Banana.exe")
   ```
3. Make sure you have installed numpy, matplotlib, pytorch, and unityagents before starting the notebook.

### Instructions for training

Follow the instructions in `Navigation.ipynb` to get started with training your own agent!  

### Watch a Pretrained Agent
Skip the dqn step in the notebook and run the final cell before `env.close()` to load a pre trained model from `checkpoint.pth` provided with this repository.