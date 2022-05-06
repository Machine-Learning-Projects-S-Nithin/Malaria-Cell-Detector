# Malaria-Cell-Detector
A Deep learning model used to identify the malaria cell and say if a person is suffering from malaria.
## Overview of the dataset
The dataset contains around `22600` different images of malaria cells and a csv file that maps each of the images' file names to a label saying if that cell is a `malaria` cell or a `healthy` cell.</br></br>![Screenshot (536)](https://user-images.githubusercontent.com/84195790/167004468-f7f73307-a6a2-45be-9fac-801cd50cde3b.png)<br/></br>
Since each of these images is of varying dimensions, the mean of the horizontal and vertical components of dimensions are calculated and is found to be `132px` x `132px`. All the cell images are resized to this dimension in order to feed to the model.<br/>
These resized images are then split into training and testing data. From these training and testing data, HOG features are extracted from the images and stored in `train_features` and `test_features` lists respectively, which are later converted to `numpy` arrays.<br/>
## Histogram of Oriented Gradients (HOG)
According to Wikipedia, "The Histogram of oriented gradients (HOG) is a feature descriptor used in computer vision and image processing for the purpose of object detection". The HOG descriptor focuses on the structure or the shape of an object. It is better than any edge descriptor as it uses magnitude as well as angle of the gradient to compute the features.
## Deep Learning Model
### Activation Functions used 
- Leaky ReLU
- Tanh
- Softmax
- Sigmoid<br/>
### Libraries used and their documentations:
- [Numpy](https://numpy.org/doc/stable/reference/index.html#reference)
- [Pandas](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html)
- [LabelEncoder - Sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.LabelEncoder.html)
- [Imread, Imshow - Scikit-image](https://scikit-image.org/docs/stable/api/skimage.io.html)
- [Resize - Scikit-image](https://scikit-image.org/docs/dev/api/skimage.transform.html#skimage.transform.resize)
- [Train test split](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html)
- [Hog](https://scikit-image.org/docs/stable/api/skimage.feature.html#skimage.feature.hog)
- [Sequential - Keras.models](https://keras.io/guides/sequential_model/)
- [Dense - Keras.layers](https://keras.io/api/layers/core_layers/dense/)
- [LeakyReLU - Keras.layers.advanced_activations](https://keras.io/api/layers/activation_layers/leaky_relu/)<br/><br/>


The Deep learning model consists of 5 layers with 128 perceptrons in the first three layers, 64 perceptrons in the fourth layer and 128 in the fifth layer. The output layer uses only 2 perceptrons as the cell has to be classified as either `healthy` or `malaria`.<br/>
The deep learning model can be represented similar to the diagram shown below:<br/><br/>
![Figure1-1024x429](https://user-images.githubusercontent.com/84195790/167010451-92d8ab29-c953-4f78-ae95-51be00d8f872.jpg)
<br/><br/>This model is accurate up to 80.3% when implemented on test data.<br/>
I'm looking forward to learn and implement better machine learning and Deep learining models that has a better performance.<br/> Thank You.
