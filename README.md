# CNN Classification Characteristics

## Project Goal

It's known that image recognition systems are easily fooled by well-known objects that appear in unnatural positions, e.g., a school bus on its side: [Google's image recognition AI fooled by new tricks](https://www.zdnet.com/article/googles-best-image-recognition-system-flummoxed-by-fakes/).

So we wonder what characteristics are having more of an impact on CNNs failing to correctly classify an object in an image. We will use a model (ResNet, Inception) pre-trained on the ImageNet dataset and then introduce images of common objects in a variety of situations to see which are most problematic for the models.

Proposed scenarios:

* standard objects in standard postions but with the whole image rotated 90, 180, 270 degrees prior to being fed to the model

* standard objects in unnatural postions (chair lying on its back on the floor)

* standard objects in unnatural postions but rotated 90, 180, 270 degrees to make their position appear natural (teapot lying upside down on a countertop, with the image being rotated 180 degrees so that it appears upright)

* standard objects in unnatural locations (an upright chair facing a bed or a toilet)

We will also **attempt** to implement [LIME](https://arxiv.org/abs/1602.04938) to see if we can't ascertain what the models are having the most trouble with when failing to identify the objects.


## Tools

We will utilize Keras and TensorFlow when working with the CNNs and we will use Matplotlib to display our findings.
