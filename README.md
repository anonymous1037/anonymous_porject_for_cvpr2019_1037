# Anonymous project for CVPR 2019 submission #1037

We first release all codes and configurations for image hashing.

# Prerequisties
Ubuntu 16.04

NVIDIA GPU + CUDA and corresponidng Pytorch framework (v0.4.1)

Python 3.6


# Datasets
1. Download database for the retrieval list of imagenet in the anonymous link [here](https://drive.google.com/open?id=1xDfg2liQzjzXxp51DEgSVMEI1trKJ_RA), and put database.txt in 'data/imagenet/'

2. Download MS COCO, ImageNet2012, NUS_WIDE in their own official website: [COCO](http://cocodataset.org/#download), [ImageNet](http://image-net.org/download-images), [NUS_WIDE](https://lms.comp.nus.edu.sg/research/NUS-WIDE.htm). Archive all data in 'data/', corresponding director for every dataset.



# Train

## Train on imagenet, 64bit hash bits

```
python train.py --data_name imagenet --hash_bit 64 --gpus 0,1 --model_type resnet50 --lambda1 0  --lambda2 0.05
```

Trained model will be saved in 'data/imagenet/models/'



Train on coco, 64bit hash bits

```
python train.py --data_name coco --hash_bit 64 --gpus 0,1 --model_type resnet50 --lambda1 0  --lambda2 0.05 --multi_lr 0.05
```

Trained model will be saved in 'data/coco/models/'



Train on nus_wide, 64bit hash bits

```
python train.py --data_name nus_wide --hash_bit 64 --gpus 0,1 --model_type resnet50 --lambda1 0  --lambda2 0.05  --multi_lr 0.05
```

Trained model will be saved in 'data/nus_wide/models/'


# Test

If you want to evaluate our pretraied models for three ImageNet, COCO, NUS_WIDE (64bit, 32bit, 16bit) are in the anonymous link, [here](https://drive.google.com/drive/folders/1HFLDfPvSrVITCFwolcQ3arym4PTODMHQ?usp=sharing)



Test for imagenet:

download pre-trained model 'imagenet_64bit_0.8734_resnet50.pkl' for imagenet, put it in 'data/imagenet/', then run:

```
python test.py --data_name imagenet --gpus 0,1 --model_name 'imagenet_64bit_0.8734_resnet50.pkl' 
```


Test for coco:

download pre-trained model 'coco_64bit_0.8612_resnet50.pkl' for coco, put it in 'data/coco/', then run:

```
python test.py --data_name coco --gpus 0,1 --model_name 'coco_64bit_0.8612_resnet50.pkl' 
```



Test for nus_wide:

download pre-trained model 'nus_wide_64bit_0.8391_resnet50.pkl' for nus_wide, put it in 'data/nus_wide/', then run:

```
python test.py --data_name nus_wide --gpus 0,1 --model_name 'nus_wide_64bit_0.8391_resnet50.pkl' 
```

# Hash Center
Here, we put hash centers for imagenet we used in 'data/imagenet/hash_centers', we will release the algorithm for hash center generation in the future.
