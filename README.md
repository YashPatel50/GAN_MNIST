# Creating a GAN for the MNIST Dataset

Yash Patel
Big Data Analytics, Worcester Polytechnic Institute, yppatel@wpi.edu

## Introduction
Being able to generate completely new images is one of the benefits of unsupervised learning. One of the classic examples of this is the MNIST dataset, which are images of numbers from 0 - 9. This is a good starting dataset to be able to practice creating GAN’s which is what this report is about

## Generator
I created a Generator with 4 fully connected layers with leaky relu activation function with dropout 0.2 at every layer. I then use tanh at the end for my final activation function because the it was stated on multiple sites that this would be the best activation function to use. I use the Adam optimizer for momentum and descent.

Neurons per layer:
400 -> 800 -> 1600 -> 784

## Discriminator
My Discriminator is 4 fully connected layers with leaky relu activation function and dropout of 0.2 at every layer. I use sigmoid activation function at the end for classification. I use the Adam optimizer.

Neurons per layer
784 -> 1568 -> 512 -> 256 -> 1

I also used the Binary Cross Entropy loss for the generator and discriminator. I attempted to use the Wasserstein loss function however I couldn’t get a better model.

![image](https://github.com/YashPatel50/GAN_MNIST/assets/33602468/4a92284e-64c0-4905-99cb-d514d872bd57)
