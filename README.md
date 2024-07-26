# ImageTextCoding
A temporal repository for the paper "LMM-driven Semantic Image-Text Coding for Ultra Low-bitrate Image Compression"

# Description 
This is the repository fot the under-review paper "LMM-driven Semantic Image-Text Coding for Ultra Low-bitrate Image Compression".
**This GitHub account is tentative to maintain the anonimity.** This repository will be moved to actual repository of the authors later.  

# Requirements
Python 3.10 and some other packages are needed. Please refer to the `How to Use` section below.
Our experiments and verification are conducted on Linux(Ubuntu 22.04) and Docker container with cuda=1.2.1 and torch=2.1. 

# How to Use

- First, clone this repository. 
```
git clone https://github.com/user475289/TextImageCoding/
cd TextImageCoding
```

- Download the DiffBIR weights and our pre-trained weights to the `/weights` folder and `/lic-weights/cheng` folder respectively.

The weights for DiffBIR is available at https://github.com/XPixelGroup/DiffBIR. 
We adopt 'v1_general' weights through our experiments. 

Our pre-trained weight is avairable at [this link](https://drive.google.com/file/d/1S9Unc_di0x0DyMo0NCpPYeCtL7915RJ2/view?usp=drive_link). Please note that this is nightly release. 
All the weights for the experiment will be released soon. 

- Install requirements (using virtual environment is recommended).
```
pip install -r requirements.txt
```

## demo inference
We prepare compressed text caption for kodak image datasets. Please run
```
bash run_misc.sh
```
with nessessary specification. 

For other datasets, please generate and compress the caption by running `llavanextCaption_Compression.ipynb` and place the output csv to the `df` folder, and specify the dataset in `run_misc.sh`. 

## Training
Our training code is based on CompressAI. Please run `lic/train.sh` with specification of the models, datasets and parameters. 

