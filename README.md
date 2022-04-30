# Using-Computer-Vision-to-Find-Waldo
## Introduction
In this project we attempted to use computer vision to find Waldo in an image. Our data consisted 39 images of Waldo that were cropped out of the original images, approximately 6000 images without Waldo, also cropped out of the original images, and 19 original images just like in the book. 
## Classification Model
We imported all the images into google collab notebook using `c2.imread` and converted them into arrays. We labeled images with either 1 for images containg Waldo or 0 for images without Waldo. we only used cropped images for the classifier, original images will be used later in the project.
After splitting the images into train and test sets we needed to convert arrays from loading the images into numpy arrays. Then, we needed to flatten them to 1D. Our neural network was made out of 4 layers which 2 of those were hidden layers consisting 64 neurons.The fourth layer is the output layer with only one neuron- our final value.
After running our model, images with probability higher than 0.5 the model were classified as images with Waldo, and images with the probability less than 0.5 were classfified as images withouth Waldo. Our model had the accuracy of ~80%, however the results were inconsistent. 
## R-CNN
We wanted to identify and area on the image with Waldo using R-CNN. In this part of the project we used 19 original images. We anually annotated an area with Waldo on each image by making a bounding box around Waldo. We then reshaped the images into array and then saved into a csv file so that we could use them in our model.Annotatino was a success but then we started facing challenges and couldn't run our model withour RAM runnin ot of storage.
