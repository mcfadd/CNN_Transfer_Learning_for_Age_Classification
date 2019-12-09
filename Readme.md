# CNN Transfer Learning for Age Classification

This project was inspired by the paper, *Age and Gender Classification Using Convolutional Neural Networks* [[1]](#1).

The main goal of this project is to compare the performance of transfer learning on a pre-trained [ImageNet](http://image-net.org/) CNN classifier to the CNN classifier described in the paper [[1]](#1).

The pre-trained CNN used in the experiment is ResNet-34, which comes from [torchvision](https://pytorch.org/docs/stable/torchvision/models.html).

### Transfer Learning

Transfer learning is a technique where you use a model trained on a very large data set and then adapt it to another (smaller) data set. An advantage of this is that it takes far less time to do transfer learning than to train a model from scratch. 
The ResNet-34 CNN used in this project was trained on [ImageNet](http://image-net.org/).

### Data Set

This project makes use of the [Adience Benchmark](https://talhassner.github.io/home/projects/Adience/Adience-data.html) Unfiltered faces for gender and age classification data set [[2]](#2). The data set includes 26,580 images, 2,284 subjects, and 8 age-range categories (0-2, 4-6, 8-13, 15-20, 25-32, 38-43, 48-53, 60-100). 

### Evaluation

5-fold cross validation is used to evaluate the performance of the transfer learned model across the following metrics:

- **Accuracy**: Percentage that the classifier predicted the correct age-group
- **One-off Accuracy**: Percentage that the classifier predicted a label that is off by one adjacent age-group

## Setup

This project requires the use of a GPU to process images.
If you don't have a GPU available you can still run the project using [Colab](https://colab.research.google.com/notebooks/welcome.ipynb) by following [Colab.md](Colab.md).

## References

##### [1]
*Gil Levi and Tal Hassner, Age and Gender Classification Using Convolutional Neural Networks, IEEE Workshop on Analysis and Modeling of Faces and Gestures (AMFG), at the IEEE Conf. on Computer Vision and Pattern Recognition (CVPR), Boston, June 2015* ([Project and code](https://www.openu.ac.il/home/hassner/projects/cnn_agegender/), [PDF](https://talhassner.github.io/home/projects/cnn_agegender/CVPR2015_CNN_AgeGenderEstimation.pdf))

##### [2]
*Tal Hassner, Shai Harel\*, Eran Paz\* and Roee Enbar, Effective Face Frontalization in Unconstrained Images, IEEE Conf. on Computer Vision and Pattern Recognition (CVPR), Boston, June 2015* ([Project and code](https://talhassner.github.io/home/publication/2015_CVPR_1), [PDF](https://talhassner.github.io/home/projects/frontalize/CVPR2015_frontalize.pdf))

