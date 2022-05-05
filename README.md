# Malaria-Cell-Detector
A Deep learning model used to identify the malaria cell and say if a person is suffering from malaria.
## Overview of the dataset
The dataset contains around `22600` different images of malaria cells and a csv file that maps each of the images' file name to a label saying if that cell is a `malaria` cell or a `healthy`.</br>
Since each of these images is of varying dimensions, the mean of the horizontal and vertical components of dimensions are calculated and is found to be `132px` x `132px`. All the cell images are resized to this dimension in order to feed to the model.
