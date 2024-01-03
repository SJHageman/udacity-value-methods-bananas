# udacity-value-methods-bananas

This is a project as part of the Udacity Deep Reinforcement Learning nanodegree.

## Introduction

For this project, I trained an agent to navigate and collect bananas in a large, square world.  

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.

## Requirements

The work for this project was done in AWS SageMaker Sudio (classic).  This requires you to clone the [Value-based-methods repo](https://github.com/udacity/Value-based-methods), and get the unity environment with visualization, found [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip).  The zip file should be unzipped and placed in the p1_navigation folder.

The dqn_agent.py file contains the agent and replay buffer code used in the environment, and the model.py file contains the Q-network code used as the function approximator by the agent.  Note that both of these files are adapted from the solutions to the Lunar Lander lesson in the course.

## Environment setup

The work for this project was performed in AWS SageMaker Studio (Classic).  This takes a bit of setup to prepare.  The steps to run the main notebook (Navigation.ipynb) are as follows:

0. To use the unityagents package, there needs to be one modification made to the requirements.txt file in the path Value-based-methods/python/requirements.txt.  The torch version needs to be changed from torch==0.4.0 to torch>=0.4.0.
1. Open the notebook Navigation.ipynb, and select the following parameters
    - Image: "Data Science 2.0"
    - Kernel: Python 3
    - Instance type: ml.m5.2xlarge
    - Start-up script: No script
2. Once that instance starts up, go into the image terminal of that instance and execute the shell script build_env.sh. This will create the drlnd virtual environment.
3. Once that is complete, close the image terminal and go back to the notebook.  Select change the notebook environment, and you should now be able to select the kernel associated with the drlnd conda virtual environment.
4. Now the Navigation notebook is ready to be executed!

## Output

The main Navigation.ipynb notebook will output a figure of the scores vs epsiode number, and a number of model weights for different hyperparameters.