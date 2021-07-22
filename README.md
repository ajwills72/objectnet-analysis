# Overview

This repository is designed to do performance analyses of classifiers against the objectnet image set, using Tensorflow.

## A note on GPUs and Tensorflow

Setting this up is a pain in the ass, long-winded, and prone to breaking. Don't do it unless run-time is getting prohibitive, and you'll probably need a £500+ graphics card to speed things up considerably.


## Add models

The repo does not contain the models, you must add these yourself (and do not add them to the repo, they're too big). All models you want to test are downloaded to `downloads`. Here's an example for ResNet50:

```
cd downloads
wget https://storage.googleapis.com/tensorflow/keras-applications/resnet/resnet50_weights_tf_dim_ordering_tf_kernels.h5
cp resnet50_weights_tf_dim_ordering_tf_kernels.h5 ../model
```

Only one model should be in the `models` directory at any one time.

## Add images

The repo does not contain images, you must add these yourself (and do not add them to the repo, they're too big). On the `willslab-ply` server, the easiest solution to gain full access to objectnet is to make a symbolic link to the dataset drive:

`ln -s /mnt/datasets/objectnet/images/ input/images`

On my home desktop

`ln -s ~/objectnet/images input/images`


