 ## AlexNet Implementation 

I tried replicating the AlexNet architecture from the  ImageNet Classification with 
Deep Convolutional Neural Networks paper by Alex Krizhevsky with a little tweaks.

The AlexNet architecture contains 60 million parameters consisting of 5 convolutional 
neural network and 3 Fully Connected layers plus some maxpooling layers. This architecture
was built to handle large datasets for object recognition tasks.

What made this paper special was the certain techniques they use to ensure
a succesful training :
* Local Response Normalization
* ReLU activation functions
* GPU parallelism
* Data augmentation

I tried to follow the exact details the paper gave sticking as close as possible
to their original architecture. I implemented all the specific layers they mentioned and
tried to keep everything faithful to what they described but i ran into  some constraints
along the way.

The Alexnet architecture consist of Five Convolutional layer with the local response normalization
after the relu activation function before the maxpool layer in the first and second layer.  
The AlexNet architecture also comes with 3 Fully Connected layer.

Some of the constraints that i came across where:
* Gpu parallelism: The paper mentions training the AlexNet  using  two GPUs because of the architectures
  large size. My training was done on Google Colab using T4 GPUs, which had enough memory to handle the
  entire network without needing to split across multiple GPUs.

* Dataset: The AlexNet was trained on a subset of ImageNet which contained about 1.2 million training images.
I ran into  some  issues with the training pipeline, so i opted to use the CIFAR 10 data with data augmentation
ofcourse to make up for the dataset size. Data augmentation was added to the training images and i resized the size of the image to 227 which was
the standard image size used in the architecture

* Optimizer: The SGD optimizer was used  in the paper with a weight_decay of 0.0005 a momentum of 0.9 and a weight_decay
  of 0.01. I went with  the Adam optimizer instead with a learning rate of 0.0001 and added a learning rate scheduler with a step-size
  of 30.

* Training: The AlexNet architecture was trained ofor 90 epochs but due to slow training time and and early signs of good generalization i manually
stopped the training early.

The purpose of implementing this architecture was to understand how the AlexNet architecture worked and why it was a breakthrough in deep learning
architecture



 

