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
extracts features and breaks it dow into 32 images further along the line this images meets the seconf conv kernel which
extracts a deeper and more meaningful information from the model.


 


