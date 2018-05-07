# Classifier
A Simple Implementation of a TensorFlow Classifier

## Introduction
This projects implements a simple car image classifier using Python with TensorFlow and Keras (Keras is a layer on top of TendorFlow). It uses an AWS EC2 instance with CPU (I'm waiting on AWS's approval for a GPU instance). The model fine-tunes a ResNet50 CNN (Convolutional Neural Net) which has been pre-trained on [ImageNet](http://www.image-net.org/) and is available within the Keras library. A small car dataset has been setup for training and testing.

It has achieved ~90 % accuracy with the provided data, which is not bad for a dataset of < 1000 images, trained on a CPU.

## Logging In
#### On a Mac 
1. open up a terminal
2. enter: 'ssh -i /*path_to_file*/shauns.pem ubuntu@ec2-18-237-72-20.us-west-2.compute.amazonaws.com'
#### On Windows 
1. ensure that an SSH client such as [Putty](https://www.putty.org/) has been installed and open a command line.
2. enter: 'putty.exe -ssh -i /*path_to_file*/shauns.pem ubuntu@ec2-18-237-72-20.us-west-2.compute.amazonaws.com'



