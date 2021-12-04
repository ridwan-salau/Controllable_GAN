# Controllable DCGAN 

## Summary
 While DCGAN makes it possible to train a neural network using deep convolutional layers, Controllable DCGAN allows us to control specific features that are generated. This control is achieved by modifying the latent vector (z) input through the use of a classifier network. The classifier network is trained to classifier an image into one of 40 labels. The output of this classifier is used to update the latent input vector through stochastic gradient accent. 

## Inputs
 The input for this project is the CelebA database of images of celebrities. Each of the image is assigned one of 40 features as label. 

## Architecture
 The setup of the project involves training a DCGAN generator using a generator-critic pair. Further, classifier is trained on the image dataset with the 40 features as labels. 

> ### The generator
 5-layer network of transpose convolutions with batch normalization at each layer but the last. ReLU activation function is used at each layer but the last which uses Tanh. 

> ### The critic
 4-layer network of convolutions with batch normalization at each layer but the last. LeakyReLU activation function is used at each layer except the last which has none. 

> ### The classifier
4-layer network of convolutions with batch normalization at each layer but the last. LeakyReLU activation function is used at each layer except the last which has none. 


## Outputs
 The output of the project are images which have some specific features added as defined in the code. 