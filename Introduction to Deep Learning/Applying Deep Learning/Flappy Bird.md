you'll get to see a deep learning agent playing Flappy Bird! You have the option to train the agent yourself, but for now let's just start with the pre-trained network given by the author. Note that the following agent is able to play without being told any information about the structure of the game or its rules. It automatically discovers the rules of the game by finding out how it did on each iteration.
We will be following [this repository](https://github.com/yenchenlin/DeepLearningFlappyBird) by Yenchen Lin.

Instructions
-
Install miniconda or anaconda if you have not already.


Create an environment for flappybird
Mac/Linux: conda create --name=flappybird python=2.7
Windows: conda create --name=flappybird python=3.5


Enter your conda environment
Mac/Linux: source activate flappybird
Windows: activate flappybird


conda install opencv 


If you encounter an error here, you may try an alternate download path and instead type conda install --channel https://conda.anaconda.org/menpo opencv3


pip install pygame


pip install tensorflow==0.12


git clone https://github.com/yenchenlin/DeepLearningFlappyBird.git


cd DeepLearningFlappyBird


python deep_q_network.py


If all went correctly, you should be seeing a deep learning based agent play Flappy Bird! The repository contains instructions for training your own agent if you're interested!
You can also, typically, force-quit out of the game by returning to your terminal window and typing Command or Ctrl + C.
