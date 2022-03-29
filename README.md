# Traffic Sign Detection
### Object Detection:
Object detection is advanced image classification in which the neural network identifiees multiple objects in an image and also places a bounding box on those objects
##### Object detection thus refers to the detection and localization of objects in an image
##### There are two kinds of Object detections Two-stage or region proposal object detection and one-stage or proposal-free object detection
#### Two-stage object detection:
The algorithm approaches the problem into two stages
##### 1) Detecting possible object regions
##### 2) Classifing the objects in those regions into object classes
##### Fast-RCNN and Faster-RCNN are most popular two-stage algorithms
### YOLO (You Only Look Once):
 The YOLO algorithm divids the image into N grids, each of dimensional region SxS. These N grids is responsible for the detection and localization of the objects in it. These grids predict B bounding box coordinates relative to their cell coordinates, along with the object label and probability of the object being present in the cell.
##### Due to multiple cells predicting the same object we get a lot of duplicate predictions and different bounding boxes
##### Yolo implements a Non-Maximal Suppression to solve this issue
In Non Maximal Suppression, YOLO suppresses all bounding boxes that have lower probability scores.
YOLO achieves this by first looking at the probability scores associated with each decision and taking the largest one. Following this, it suppresses the bounding boxes having the largest Intersection over Union with the current high probability bounding box.
#####
![yolo working](https://github.com/VAMSEE92/TrafficSignDetection/blob/main/Images/grids.png)
#####
### Yolo Architecture
YOLO’s architecture has a total of 24 convolutional layers with 2 fully connected layers at the end. 
#####
![architecture](https://github.com/VAMSEE92/TrafficSignDetection/blob/main/Images/archetecture.png)
#####
### YOLO Vs other detectors
Methods that use Region Proposal Networks thus end up performing multiple iterations for the same image, while YOLO gets away with a single iteration.

## Darknet
Darknet is a command-line tool used to train and test neural networks. It is free, in every sense of the word.

You can clone the darknet from below link
https://github.com/AlexeyAB/darknet

## YOLO-v3 Implementation on traffic signs

Detailed yolov3 implementation is present in the notebook
####
Image before prediction

![test Image](https://github.com/VAMSEE92/TrafficSignDetection/blob/main/Images/test.jpg)

Predictions in Image

![predictions](https://github.com/VAMSEE92/TrafficSignDetection/blob/main/Images/predictions.jpg)
#### Predicting from video
Video before prediction
#####
https://github.com/VAMSEE92/TrafficSignDetection/blob/main/Videos/tes.mp4
#####
Predicted Video
#####
https://github.com/VAMSEE92/TrafficSignDetection/blob/main/Videos/results.mp4
