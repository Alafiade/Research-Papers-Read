## This Repo contains some  of my insights on the LeNet 5 paper ##

The Novel Deep LeNet-5 Convolutional Neural Network Model for Image Recognition is a model designed
to  solve the generalization problem of Image Recognition.

Image recognition technology extracts features from our data and passes it to a classifier for classification.
They were three Image recognition methods the paper mentioned which are:
- K nearest Neighbor
- Basic Neural Network
- Support vector machine.

All these methods has their shortcomings when trying to solve the generalization problem of Image Recognition.
So to combat this shortcomings the Deep LeNet model was proposed .
The DeeP LeNet is a type of Convolutional Neural Network
The convolutional neural network has five layers which are the input layer , convolutional layers , downsampling layers,
fully connection layer and output layer.
- Input layer:- This layer of the model takes the image as a whole into the network.
- Covolutional layer:- This extracts important information from the image for prediction, its also known as the feature extraction layer.
- Downsampling Layer:- Also known as the pooling layer this converts images from high resolution to low resolution to improve network
  speed.
- Fully connection layer:- Thesee takes the reduced resolution images to lead to a prediction.

## STRUCTURE OF LENET 5
The LeNet5 CNN consists of the input layer , hidden layer and output layer.


The input layer is a 32x32 single channel image. The hidden layer is responsible for the extraction and classification of object features(features of image).
The hidden layer is responsible for extraction and classification of object features.
The output layer  outputs an integer representing the category.

The hidden layer is generally composed of Convolutions , Subsampling and fully connection layer.

This paper architecture contains two conv layers and they have a 32 5x5 conv kernels and a 645x5 convolutional kernels
respectively. So basically once the image is passed through the model the first conv layer which contais 32 5x5 kernel 
extracts features and breaks it down into 32 images further along the line this images meets the second conv kernel which is
64 5x5 and extracts a deeper and more meaningful information from the model.
The model has two pooling layers also called sub-sampling layers which can help reduce the size of our images  for faster training and 
eliminate repeated extracted features.

The Fully Connected layers which are similar to MLP (Multi Layer Preceptron) meaning they are connected from one previous layer to another.
The two first fully connected layers consist of 1024 neurons and the second 67 neurons and each neurons computes a dot product between its
input features and weights and the output goes through a sigmoid function which gives the result classification.

Take aways  :- What i understand so far is that the basic LeNet 5 architecture is slow and to fix it the activation function L-RELU was introduced.  

## Activation Function Optimization ##
The reason LeNet 5 activation model has a slow convergence speed is because of the sigmoid activation function.
The sigmoid function basically computes a value between 0 and 1 so if the value is too negative or too positive then the gradients in 
the gradients descent diminish another term for this is called vanishing gradients.   This affects our model because the Gradient descent
is an optimization technique that helps the model calculate the loss value from the actual label vs the predicted label.

So in backpropagation the model's final layer takes the loss of the model and the signal is propagated backward, so the gradient goes back to the layer of the network and through the activatin layer (sigmoid) and as said earlier if the values are too high or too low it produces a low gradient value which causes the model not to converge. To fix this the L-ReLU activation function was introduced  which is a modified version of the ReLU activation  function.

## Leaky-RELU ##
The paper presented the statistized Rectified Linenear Unit (L-ReLU) in the activation function optimization.
L-Relu has basic properties that makes it necessary to  become an activation function:
1. Non linearity:- L-Relu plays a good role of a non linear mapping in CNN because the L-Relu activation function keepws a positive input as it is but converts a negative input to a small number instead of 0 and learns from it. Sometimes complex patterns in the image such as textures and curves could be represented as these negative numbers so instead of converting them to 0 it converts them to small numbers like we said so we could learn complex patterns from  it.
2. Differentiability:- This is the ability of the network to calculate its slope(gradient) and adjust its weights during training.  If the L-Relu is not differentiable backpropagation cant happen. 
3. Monotonicity :- As the input increases the output increases, lets say we have a feature map [0.2 -2.0 0.4] the negative means those pattens might be missing and we know that L-Relu  converts our negative input to a small number p.s [0.2 -0.3 0.4] is being inputed into the L-Relu layer and its supposed to have an output right ? so we get something like [0.2 -0.2 0.4] which would be the output. So if you make comparisons -0.2 is bigger than -2.0 it is a small number but it still increased as it passed into the L-Relu.
4. Infinite:- The L-Relu is inifinite becausr the output grows infinitely for large positive inputs making it good for deep networks.

The paper also uses a 3x3 convolutional kernel. In addition it adopts a dropout rate of 0.7 which helps combats overfitting.

 


 


