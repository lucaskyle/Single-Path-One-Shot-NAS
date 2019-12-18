# Single-Path-One-Shot-NAS
This repo provides a Pytorch-based implementation of SPOS([Single Path One-Shot Neural Architecture Search with Uniform 
Sampling](https://arxiv.org/abs/1904.00420))  by Zichao Guo, and et. al.
![SPOS](https://github.com/ShunLu91/Single-Path-One-Shot-NAS/blob/master/img/SPOS.jpg)

This repo only contains 'Block Search' for reference. It's very time consuming to train this network on ImageNet, which
makes it impossible for me to finish the experiment under existing resources. As a result, this repo mainly focuses on 
CIFAR-10 and greatly thanks to Zichao Guo for his advice on some details.
Yet, there are still some differences with the [official version](https://github.com/megvii-model/SinglePathOneShot) 
such as data preprocessing and some hyper parameters.

As for the model search, in my opinion, you can refer to the official version for the Evolutionary Algorithm and also 
you can randomly search 1000 models to find the best for test.

## Environments    
```
Python == 3.6.8, Pytorch == 1.1.0, CUDA == 9.0.176, cuDNN == 7.3.0, GPU == Single GTX 1080Ti 
```

## Dataset   
SPOS can directly train on CIFAR-10 and ImageNet.
CIFAR-10 can be downloaded automatically with this code. ImageNet needs to be manually downloaded and 
[here](https://github.com/pytorch/examples/tree/master/imagenet) are some instructions. 
         
## Usage
```
python cifar_train.py exp_name spso_cifar
```

## To Do
- [x] Block Search
- [x] Train and Evaluate on CIFAR-10

## Reference
[1]: [Differentiable architecture search for convolutional and recurrent networks](https://github.com/quark0/darts)
             
## Citation
```
@article{guo2019single,
        title={Single path one-shot neural architecture search with uniform sampling},
        author={Guo, Zichao and Zhang, Xiangyu and Mu, Haoyuan and Heng, Wen and Liu, Zechun and Wei, Yichen and Sun, Jian},
        journal={arXiv preprint arXiv:1904.00420},
        year={2019}
}
```
