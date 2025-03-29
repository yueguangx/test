# Installation
Follow these steps to set up and run the HGNet project on your local machine:

**Clone the repository**:


```
git clone https://github.com/yueguangx/HGNet.git
cd HGNet
conda create -n HGNet python=3.8
conda activate HGNet
pip install -r requirements.tx
```




# Dataset Preparation

To train and evaluate the HGNet model, it's essential to organize your dataset in the COCO format. Below are the steps to prepare your dataset:

Directory Structure:

Organize your dataset with the following structure:

plaintext
复制
编辑
├── coco
│   ├── images
│   │   ├── train2017
│   │   └── val2017
│   └── labels
│       ├── train2017
│       └── val2017
