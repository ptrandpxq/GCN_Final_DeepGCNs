# GCN_Final_DeepGCNs
Final project of the course Graph Convolutional Networks. </br> 
This repository is partly borrowed from original paper's code, and I fixed part of code for running without problem. <br/>
This repository is only for the final porject. <br/>


## DeepGCNs: Can GCNs Go as Deep as CNNs?
* [Paper](https://arxiv.org/pdf/1904.03751.pdf)

<div style="text-align:center"><img src='./images/deepgcns.png' width=800>


## Requirements
There are many package version requirements, so please install a new conda enviroment to run the code.

Install the conda enviroment by running:
```
conda env create -f deepgcn.yml
conda activate deepgcn
```

## Code Architecture
    .
    ├── images                  # images
    ├── utils                   # common useful modules
    ├── gcn_impl                # gcn library
    ├── sem_seg                 # code for point clouds semantic segmentation on S3DIS 
    └── ...

## How to train, test and evaluate the models (important!)

Please look the details in `README.md` in `sem_seg` folder.<br/>
All the information of the code, data, and pretrained models can be found there.

### A simple example (training from scratch)
First enter the example directory,
```
cd sem_seg/
```
and then run:
```
CUDA_VISIBEL_DIVICES=0,1,2,3 python train.py --phase train --multi_gpus --batch_size 8
```
Lower the batch size if out of memory. The batch size will not influence the test results.


## Contact
Tairen Piao

E-mail: piaotairen@snu.ac.kr
