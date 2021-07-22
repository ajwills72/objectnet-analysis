# Overview

This repository is designed to do performance analyses of classifiers against the objectnet image set.

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


