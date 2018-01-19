# Simple-Neural-Network in Python
Very simple NN with 2 inputs and 1 baias

We have two sensors, each one with 2 states, 1 for on and 0 for off.

If two sensors is on then output must be 1,otherwise output is 0.

Sensor 1 | Sensor 2 | Output
   1          1         1
   1          0         0
   0          1         0
   0          0         0


Objective is to train an NN to recognize a result through the inputs of the sensors

NN architecture:
-1 neuron
-Activation function is Degrau
-All inputs have bias 1
-Training ends when the total error is less than 0.01
