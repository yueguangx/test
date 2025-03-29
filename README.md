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

# Datasets

To train and evaluate the HGNet model, it's essential to organize your dataset in the COCO format. Below are the steps to prepare your dataset:

**Directory Structure:**

Organize your dataset with the following structure:

```plaintext
coco
├── images
│   ├── train2017
│   └── val2017
└── labels
    ├── train2017
    └── val2017
```

# Usage
Integrating the YOLO model into your Python projects is straightforward with the Ultralytics YOLO library. Below is a concise guide demonstrating how to load a pretrained model, train it on a custom dataset, evaluate its performance, perform inference, and export it to ONNX format:
```
from ultralytics import YOLO
# Load a pretrained YOLO model (recommended for training)
model = YOLO("yolov11n.pt")

# Train the model using the 'coco8.yaml' dataset for 3 epochs
results = model.train(data="coco8.yaml", epochs=3)

# Evaluate the model's performance on the validation set
results = model.val()

# Perform object detection on an image using the model
results = model("https://ultralytics.com/images/bus.jpg")

# Export the model to ONNX format
success = model.export(format="onnx")
```
