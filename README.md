# fall-detector
A neural network that detects the falls of elderly people from the data collected by sensors attached to their bodies. It uses a simple Python script with some Tensorflow functions. If you are learning Tensorflow, this can be your code!

![alt text](https://github.com/jjroldangomez/fall-detector/blob/master/FallDetector.png)

# Content
Here you can find the following files and folders:
- FallDetector.py: Try to create, train and use the neural network!
- FallDetectorSolved.py: Here is a solution with good performance.
- Simulated: The dataset with simulated falls. It is used to train and test the neural network.
- Real: The dataset with real falls. Try to adapt the neural network to work with it!

# Datasets
You can find two datasets: one with simulated falls generated by our fall simulator and another with real falls performed by some nice volunteers.

The simulated dataset consists of 20 CSV files with the following columns:
- Time (seconds)
- Hips angles (degrees)
- Spine angles (degrees)
- Neck angles (degrees)
- Head angles (degrees)
- Hips angular velocity (degrees/second)
- Spine angular velocity (degrees/second)
- Neck angular velocity (degrees/second)
- Head angular velocity (degrees/second)
- Hips linear acceleration (m/s2)
- Spine linear acceleration (m/s2)
- Neck linear acceleration (m/s2)
- Head linear acceleration (m/s2)
- Fall (0 before fall, 100 after fall)
- Ground (0 standing, 100 on the ground)

The real dataset consists of 10 CSV file with the following columns:
- Time (seconds)
- Euler angles (degrees)
- Linear accelerations (g)
- Angular speeds (rads/second)
- Tag (0 before fall, 100 after fall)

# Scripts
You can try the code just doing the following things:

main: 
- Set the flag to 'true' if you want to train the model and 'false' if you want to make predictions.
- Set the names of the model and sample that you want to use.

main_train:
- Select the variables to be used as the inputs and outputs of the neural network.
- Define the number of layers and their sizes in the neural network.
- Initialize the weights and biases for the different layers of the neural network.
- Create the functions for forward propagation: compute the outputs from the inputs.
- Create the functions for backward propagation: compute the errors from the outputs to the inputs and update the parameters to minimize them.
- Run the session to train the neural network, providing the inputs and desired outputs and requesting the training error.

main_predict:
- Run the session to make predictions with the neural network, providing the inputs and requesting the outputs.

# Contact
Juan Jesús Roldán Gómez - PhD on Automation and Robotics - www.jjrg.org - jj.roldan.gomez@gmail.com.

# Acknowledgements
Thanks to Elena for giving me the idea and helping me to develop it, as well as to Marta and Juve for providing us with valuable data of real falls. :)

# Warning:
This code was developed using Python 2.X with Tensorflow 1.X. 

If you want to execute it under Python 3.X with Tensorflow 2.X, you will need to make the following changes:

Replace:

import tensorflow as tf

by:

import tensorflow.compat.v1 as tf

tf.disable_v2_behavior()
