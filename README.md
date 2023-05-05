This project tries to use gaming to implement reinforcement learning. To be able to play Mario and witness the back and forth as we build up this model, we are going to develop an AI model especially a reinforcement learning model.

We're going to operate this in Python. We'll be using the open ai gym.This is a typical framework that makes it simple to teach artificial intelligence to interact with other simulated environments and play games. For our objective, we are using the gym super mario brothers environment that has been constructed on top of the NES emulator for Python at "https://pypi.org/project/gym-super-mario-bros/".

Each line of our code includes an explanation. The environment operates utilizing a "Reward function" that is familiar from the gym.-super-mario-bros

Preprocessing the Environment: As you may be aware, poor data leads to poor AI. To prepare our mario game data for AI combat, we performed two preprocessing techniques: grayscale and frame stacking. Our AI will use these images to understand how to play the game. Frame stacking gives our artificial intelligence (AI) model context by stacking consecutive frames, we're basically providing our AI model memory it'll be able to notice Mario and his adversaries moves and reduce the amount of data it has to learn from. A color image takes three times as many pixels to process.
Set up the RL libraries: To display your output, you must have GPU acceleration running CUDA or ROCm 4.2(beta). One can check GPU versions and install the version that best suits their GPU from https://pytorch.org/get-started/locally/.

Install Stable-Baselines3: We may examine the available algorithms at "https://stable-baselines3.readthedocs.io/en/master/". DQN will be used in this situation. All of them were used in wrappers, which are described in the code.

Applying Vectorization: Using VecFrameStack(env, 4, channels_order='last'), we will stack our frame.We're going to employ the Proximal Policy Optimization technique for our training reinforcement learning model. First, we import those dependencies, and after that, we'll have a sample code that allows you to save models as you train them so you can later review the various models you've actually built. So let's move forward with this, and we'll be able to import our dependencies.

#Import OS for managing file paths: os import

#Import PPO for algos: import PPO from stable_baselines3

#Import the stable_baselines3.common Base Callback for saving models.import BaseCallback in callbacks The class TrainAndLoggingCallback(BaseCallback) in the code contains the training code for our model.

Finally, testing: First, we will load our model from memory. If, for instance, we stop training or close this notebook, we would like to be able to reload it from a file rather than relying on the model that is currently in memory. To accomplish this, we can use either the model.load or the actual ppo.load method. We are going to train our model and use that trained model in the code as per quoted, says the code.

Finally, when we run our code, the output will be displayed in a new window as shown in the image below.

![image](https://user-images.githubusercontent.com/63110030/236347644-a28751d8-0637-4d41-a9a3-e252d28e1324.png)

