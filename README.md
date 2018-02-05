# Xception V1 model for Tensorflow with pre-trained weights on ImageNet

This repository contains code of the **un-official** re-implement of Xception model.

Xception is a novel deep convolutional neural network architecture, where Inception modules have been replaced with depthwise separable convolutions. With a similar parameter count, Xception significantly outperforms Inception V3 on a larger image classification dataset called JFT. More details can be found in the original paper: [Xception: Deep Learning with Depthwise Separable Convolutions](https://arxiv.org/abs/1610.02357). 
##  ##
In order to accelerate further research based on Xception, I would like to share the pre-trained weights on ImageNet for Xception, you can download from [Google Drive](https://drive.google.com/file/d/1sJCRDhaNaJAnouKKulB3YO8Hu3q91KjP/view?usp=sharing). The pre-trained weights are converted from [Keras Xception in Tensorflow](https://github.com/tensorflow/tensorflow/blob/6c5063a3f099c302412fcefa17edb2efa9921f01/tensorflow/python/keras/_impl/keras/applications/xception.py#L61) using [MMdnn](https://github.com/Microsoft/MMdnn) with other post-processing. All rights related to the pre-trained weights belong to the original author of [Keras](https://keras.io/).

**This code and the pre-trained weights only can be used for research purposes.**

The canonical input image size for this Xception is 299x299, and the input preprocessing function is the same as Inception V3. According to the doc in Keras, this model gets to a top-1 validation accuracy of 0.790 and a top-5 validation accuracy of 0.945 on ImageNet.

The code is tested under Tensorflow 1.5, Python 3.5, Ubuntu 16.04. 

If you need test this code by yourself, just follow the code snippets at the bottom of [Xception.py](https://github.com/HiKapok/Xception_Tensorflow/blob/master/Xception.py), and put the pre-trained weights under the 'model' folder. 

Other scaffold need to be build for training from scratch. You can refer to [resnet/imagenet_main](https://github.com/tensorflow/models/blob/22ded0410d5bed85a88329e852cd20882593652b/official/resnet/imagenet_main.py#L189) for adding weight decay to the loss manually.
##  ##
The MIT License