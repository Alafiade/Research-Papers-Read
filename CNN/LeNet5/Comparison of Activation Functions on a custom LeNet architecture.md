## Evaluating the Impact of Activation Functions on LeNet-5 Performance

This project compares the effect of different Activation Functions on the performance  of the LeNet 5 architecture in image classification tasks.

Activation Function introduces non-linearity to the network to help the network  predict complex patterns in an an image.
The activation function used to perform this evaluation are Tanh, ReLU and Leaky Relu 

1. Tan-h: This activation function transforms its input value between -1 and 1, what this means is that if the input is positive the output approaches 1 but if the input is negative the output represents -1.
2.  ReLU(Rectified Linear Unit): If x > 0 = X , if X<= 0 = 0 , what this means is that if our input is positive it gives the same positive value eg:  5> 0 = 5 and -5>0 = 0. Do you get it now ? A positive input gives back that same positive value but a negative input gives 0. The problem with ReLU is that once we get a value of 0 are model doesnt update which is baf.
3.   Leaky Relu : This is a modification of the ReLU but instead of converting the negative input to it converts it to a small number eg:- 0.01 which solves the vanishing gradient problem.

The LeNet-5 architecture used in this experiment had minimal changes except from the activation function in different versions of the  model.

Initially these models were tested on the CIFAR10 dataset but peformed badly due to LeNet5 being unable to handle complex datasets. Therefore models were  MNIST dataset  was used.

The Leaky ReLU model outperformed both the Tanh and the ReLU model in terms of accuracy and generalization. 


