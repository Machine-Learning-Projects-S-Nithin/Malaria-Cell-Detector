# Malaria-Cell-Detector
A Deep learning model used to identify the malaria cell and say if a person is suffering from malaria.
## Overview of the dataset
The dataset contains around `22600` different images of malaria cells and a csv file that maps each of the images' file names to a label saying if that cell is a `malaria` cell or a `healthy` cell.</br></br>![Screenshot (536)](https://user-images.githubusercontent.com/84195790/167004468-f7f73307-a6a2-45be-9fac-801cd50cde3b.png)<br/></br>
Since each of these images is of varying dimensions, the mean of the horizontal and vertical components of dimensions are calculated and is found to be `132px` x `132px`. All the cell images are resized to this dimension in order to feed to the model.<br/>
These resized images are then split into training and testing data. From these training and testing data, HOG features are extracted from the images and stored in `train_features` and `test_features` lists respectively.<br/>
## Histogram of Oriented Gradients (HOG)
According to Wikipedia, "The Histogram of oriented gradients (HOG) is a feature descriptor used in computer vision and image processing for the purpose of object detection". The HOG descriptor focuses on the structure or the shape of an object. It is better than any edge descriptor as it uses magnitude as well as angle of the gradient to compute the features.
