# Car-and-Truck-classification
![alt text](https://cdn.analyticsvidhya.com/wp-content/uploads/2018/12/Screenshot-from-2018-11-29-13-03-17.png)
## Introduction
This repsitory shows different techniques to identify cars and trucks, namely: SIFT, FRCNN, YOLOv4 and Retinanet. SIFT is the only classical method and the only method that uses classification while the rest are object detection algorithms.  

## SIFT
SIFT extracts features from an image using the following steps: Scale space construction, Key point localization, Orientation assignment, followed by the formation of the key point descriptor. Once the features are extracted from each image of the training set, all image descriptors are put together, and their centres are generated using the K means algorithm. Next, we loop through all features within an image descriptor and generate a bag of features vector for each image descriptor based on their Euclidean distance from the centres computed in the previous step (This contains the  frequency of various features within an  image). This is done for all images and finally these bag of features vectors are put together for classification using an SVM classifier.
## Faster RCNN
The following summarizes the working of the Faster RCNN:
a) A region proposal algorithm to generate “bounding boxes” or locations of possible objects in the image; b) A feature generation stage to obtain features of these objects, usually using a CNN; c) A classification layer to predict which class this object belongs to; and d) A regression layer to make the coordinates of the object bounding box more precise.
## YOLOv4
![alt text](https://thumbs.gfycat.com/IgnorantSkinnyHamadryad-size_restricted.gif)
YOLO is an abbreviation for the term ‘You Only Look Once’. This is an algorithm that detects and recognizes various objects in a picture. Object detection in YOLO is done as a regression problem and it outputs the class probabilities of the detected images. YOLO algorithm employs convolutional neural networks (CNN) to detect objects in real-time and has a total of 53 CNN layers. As the name suggests, the algorithm requires only a single forward propagation through a neural network to detect objects. This means that prediction in the entire image is done in a single algorithm run. The CNN is used to predict various class probabilities and bounding boxes simultaneously.
## RetinaNet
There are four major components of a RetinaNet model architecture:
a) Bottom-up Pathway - The backbone network (e.g. ResNet) which calculates the feature maps at different scales, irrespective of the input image size or the backbone. b) Top-down pathway and Lateral connections - The top down pathway up samples the spatially coarser feature maps from higher pyramid levels, and the lateral connections merge the top-down layers and the bottom-up layers with the same spatial size. c) Classification sub-network - It predicts the probability of an object being present at each spatial location for each anchor box and object class. d) Regression sub-network - It regresses the offset for the bounding boxes from the anchor boxes for each ground-truth object.
