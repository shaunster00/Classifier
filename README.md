# Classifier
A Simple Implementation of a TensorFlow Classifier

## Introduction
This projects implements a simple car image classifier using Python with TensorFlow and Keras (Keras is a layer on top of TendorFlow). It uses an AWS EC2 instance with CPU (I'm waiting on AWS's approval for a GPU instance). The model fine-tunes a ResNet50 CNN (Convolutional Neural Net) which has been pre-trained on [ImageNet](http://www.image-net.org/) and is available within the Keras library. A small car dataset has been setup for training and testing.

It has achieved ~90 % accuracy with the provided data, which is not bad for a dataset of < 1000 images, trained on a CPU.

## Logging In
To log in you will need to have received a file 'shauns.pem' providing AWS credentials. Store this file somehere reliable.

#### On a Mac 
1. open up a terminal
2. enter: '~ ssh -i /*path_to_file*/shauns.pem ubuntu@ec2-18-237-72-20.us-west-2.compute.amazonaws.com'
#### On Windows 
1. ensure that an SSH client such as [Putty](https://www.putty.org/) has been installed and open a command line.
2. enter: '> putty.exe -ssh -i /*path_to_file*/shauns.pem ubuntu@ec2-18-237-72-20.us-west-2.compute.amazonaws.com'

A session on the EC2 machine should have opened.

## Usage
2 programs are provided, an image prediction (testing) program and a training program.
All commands are given relative to '/home/ubuntu/classifier', so enter '$ cd /home/ubuntu/classifier' if you are not already there.

#### Image Prediction (testing)
To do image prediction you will need an already-trained model and an image.

enter: **$ python3 -W ignore src/predict_image.py *path_to_model* *path_to_image* **

eg. for the provided model and an example image

**$ python3 -W ignore src/predict_image.py model/training_run_1/car_model_resnet50.h5 test_data/neg_car/bg_graz_355.jpeg**

#### Training


## Other
A requirements file is provided in the project folder listing installed Python packages.

