# Dog Breed classifier
##Introduction
Dog breeding classiﬁcation is a challenging task since dogs with different breeding may have little visual difference. In order to achieve better result comparing to baseline method on this task, i have reimplemented several wellknown CNN networks and use Stanford Dog Dataset which is a subset from ImageNet used for the task of ﬁne-grained image classiﬁcation to verify the approach. Furthermore, i studied the transfer learning ability from a broad, general classiﬁcation problem in a ﬁne-grained classiﬁcation problem.

##Why CNN?
CNN has been used in various computer vision tasks since LeCun et al ﬁrst introduced it. Due to the advent of large scale training data such as ImageNet, CNN exhibits more advantages over other methods. Impressed by this, researchers adapt CNNs pre-trained on ImageNet to other domains or datasets, such as the ﬁne-grained image classiﬁcation dataset. Most of the current state-of-the-art CNN can be used in ﬁne-grained image classiﬁcation.

##Dataset
Stanford Dogs dataset in the project. The Stanford Dogs dataset contains image of 120 breeds of dogs from all the world. The dataset is built into two parts. The ﬁrst part is images from ImageNet for the task o ﬁne- grained image categorization.
The second part is annotation ﬁles that link images to the path of directory. In total, the number of categories is 120, the number of images is 20580 and the annotation is class labels and bounding boxes, which help us locate the target we want.

##Steps for Model Implementaion :

###Step 1 : **Data Pre-processing**
By apply data augmentation and random ﬂips to images to get better results. Also, due to the high variance of images pixels, i have rescale images to [0, 1] before further applying normalization.
We apply different data augmentation methods for training dataset and validation dataset. For training dataset, we apply data augmentation methods in the following order: resize to [256, 256], randomly rotate 45 degree, randomly crop the image to [224, 224]; for the validation dataset, we apply data augmentation methods in the following order: resize to [256, 256], crop the image to [224, 224] from the center. Finally, we ﬂip the image horizontally and randomly. For all neural network architectures we use, we follow the standard of ImageNet training.

###Step 2 : **Models**
I have used four well-known neural network architectures for this project, which are **AlexNet, GoogLeNet, VGG-16 w/o BN and ResNet18.**



