# Anonymous project for CVPR 2019 submission #1037

We first release all codes and configurations for image hashing.

# Prerequisties
Ubuntu 16.04

NVIDIA GPU + CUDA and corresponidng Pytorch framework (v0.4.1)

Python 3.6

# Datasets
1. Download database for the retrieval list of imagenet in [here](https://drive.google.com/open?id=1xDfg2liQzjzXxp51DEgSVMEI1trKJ_RA), and put database.txt in 'data/imagenet/'

2. Download MS COCO, ImageNet2012, NUS_WIDE in their own official website: [COCO](http://cocodataset.org/#download). Archive all data in 'data/', corresponding director for every dataset.


# Test

Pretraied models for three ImageNet, COCO, NUS_WIDE are in the anonymous link, [here](https://drive.google.com/drive/folders/1HFLDfPvSrVITCFwolcQ3arym4PTODMHQ?usp=sharing)

You can download the models in the above link and modefiy the model name in test.py, then run test.py
