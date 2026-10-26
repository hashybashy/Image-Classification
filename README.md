# Image Classification with Convolutional Neural Networks
Ever wondered how a computer can look at an image and recognise what's in it? That's what I set out to explore with this project!
I built an image classification model using Python, TensorFlow and Convolutional Neural Networks (CNNs), training a neural network to recognise different objects and animals from images
This project has been a hands-on way for me to understand how neural networks learn patterns from data, rather than just learning the theory behind them

### What does it actually do ?
The model is trained on the CIFAR-10 dataset, which contains 60,000 small colour images across 10 different classes
These include:
 Aeroplanes·Cars·Birds·Cats·Deer·Dogs·Frogs·Horses·Ships·Trucks
The aim is to train a model that can identify which category an image belongs to, then test it on images it hasn't seen before

### How it works !!!
The core of the project is a Convolutional Neural Network (CNN), a type of deep learning model particularly suited to image data
Rather than manually defining what makes a car different from a deer, the network learns useful visual features from the training images

The pipeline I worked through:
Loading the data: importing the CIFAR-10 dataset and separating the images into training and testing sets
Preprocessing: normalising pixel values from 0–255 to 0–1, giving the network consistent numerical inputs
Feature extraction: using convolutional layers to learn visual patterns, from simpler features such as edges to more complex combinations of patterns
Pooling: reducing the spatial dimensions of the feature maps while retaining useful information
Classification: flattening the extracted features and passing them through dense layers to produce predictions across the 10 classes
Training: using the Adam optimiser to update the network's weights and sparse categorical cross-entropy to measure prediction error over multiple epochs

The final layer uses softmax to produce a probability score for each class. The class with the highest score becomes the model's prediction

### Testing on random images
One of the most interesting parts of the project is testing the trained model on individual images, rather than only looking at its performance on the dataset
Using OpenCV, I can load an image, convert its colour channels from BGR to RGB, resize it to the model's expected 32 × 32 pixel input and normalise its pixel values before making a prediction
In hindsight it was slightly more complicated than this as what I did was take the image from Google for instance and screen snip it, edit it on Paint and resize the image to 32 x 32
This lets me experiment with images of cars, deer and other supported categories, then compare the model's predictions with what's actually in the image
It's also a useful reminder that a model's output isn't always correct: real-world photographs can look quite different from the small images it was trained on

Tech used:
Python: the main programming language.
TensorFlow / Keras: building, training and using the neural network
NumPy: working with image arrays and numerical operations
OpenCV: loading, converting and resizing custom images
Matplotlib: visualising images and inspecting results
Jupyter Notebook: experimenting with the model and documenting the workflow
