# Image Object Detector
This project is about object detection, one of the areas of computer vision that is substantially advanced over the last couple of years.


## Sample ouput
Following is a sample output of this project showing two detected zebras along with the class label and confidence. A table will also be printed listing all identified objects and their probabilities.

![Sample-output](https://github.com/majid-hosseini/Image-Object-Detector/blob/main/images/zebra_processed.JPG?raw=true)


## Object Detection Task

The object detection task is based on following two prerequisite stages:

- **Image classification:** a supervised learning process to train an algorithm to recognize a set of target classes (objects to identify in images) using labeled example photos.
- **Image classification with localization:** the process of training a supervised algorithm to predict class as well as the bounding box around the object in the image. The term 'localization' refers to identifying the location of the object in the image. 

The **object detection**  task refers to the situation where the model needs to detect multiple objects in the picture and localized them all by defining a bounding box around them. A prime example is an autonomous driving application, which needs to detect not just other cars, but also other pedestrians and motorcycles and even other objects. 


## YOLO algorithm
In recent years, deep learning algorithms are offering cutting-edge improved results for object detection. YOLO algorithm is one of the most popular Convolutional Neural Networks with a single end-to-end model that can perform object detection in real-time. YOLO stands for, You Only Look Once and is an algorithm developed by Joseph Redmon, et al. and first described in the 2015 paper titled [You Only Look Once: Unified, Real-Time Object Detection](https://arxiv.org/abs/1506.02640)

The creation of the algorithm stemmed from the idea to place down a grid on the image and apply the image classification and localization algorithm to each of the grids.
Here the YOLOv3, a refined design which uses predefined anchor boxes to improve bounding box, is utilized for object detection in new images. Source code and pre-trained models of YOLOv3 is available in the [official DarkNet website](https://pjreddie.com/darknet/yolo/).

## Project background and objectives

This project is a collection of developed utility functions to facilitate usage of YOLOv3. The developed functions achieved the following objectives :

* download the YOLOv3 pre-trained model weights
* define a proper Keras model and load the downloaded model weights
* load the image and pre-process it to meet the input requirements 
* run the model and decode outputs to obtain: 
	* detected objects, bounding boxes and class labels
* filter out low confident bounding boxes (<=user defined class_threshold)
* apply non max suppression based on user defined NMS_threshold
* stretch back the bounding boxes into the shape of the original image
* draw a box around the detected objects along with the class label and confidence  


# Requirement
* OpenCV 4.2.0
* Python 3.6


# Quick start
* **Download official** <a href="https://pjreddie.com/media/files/yolov3.weights" target="_blank">**YOLOv3 Pre-trained Model Weights**</a> **and place it in the same folder of project**


## Dependencies
* OpenCV
* Numpy
* Pandas


How to use?
===========
The project is developed in Jupyter Notebooks which is automatically rendered by GitHub. The developed codes and functions for each step are explained in the notebook.



