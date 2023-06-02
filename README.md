# Object Detection with Faster R-CNN-ResNet-FPN in PyTorch

This repository contains code for fine-tuning a pretrained Faster R-CNN-ResNet-FPN model using torchvision in PyTorch for object detection tasks. The goal is to perform one-class object detection using a dataset of hand detection, with the dataset sourced from [Roboflow](https://universe.roboflow.com/zainab-aldhanhani/pen-nsayu/dataset/1). The dataset is provided in a CSV file format, containing information such as the location of the training image, image dimensions (width, height), class annotations (class names), and bounding box coordinates. The datasets, including **train**, **validation**, and **test** sets, are stored in the **pendataset** directory along with their corresponding **annotation files**.

## Contents
1. Data Preprocessing Pipeline
2. Data Visualization
3. Model Selection Pipeline
4. Fine-tuning
5. Model Testing

## Data Preprocessing Pipeline
The data preprocessing pipeline is responsible for loading the dataset, performing any necessary transformations or augmentations, and preparing the data for training. The "CustomDataset" class, defined in the code, reads the CSV file and transforms the data into the required format for training. It loads the images, extracts the class labels and bounding box coordinates, and applies any specified transformations.

## Data Visualization
The data visualization section provides code for visualizing the annotated bounding boxes on the images to verify the correctness of the dataset annotations. It utilizes the matplotlib library to display the images with bounding box overlays.

## Model Selection Pipeline
The model selection pipeline involves selecting a pretrained Faster R-CNN-ResNet-FPN model from the torchvision library. The code imports the model architecture, modifies the last layers according to the number of classes in the dataset, and initializes the model for fine-tuning.

## Fine-tuning
The fine-tuning process involves training the model on the annotated dataset. The code defines the training loop, optimizer. It iterates over the dataset in batches, performs forward and backward passes, and updates the model parameters based on the computed gradients. The model is fine-tuned using the annotated bounding box coordinates and class labels from the dataset.

## Model Testing
During the test phase, the model's ability to detect objects (in this case, pens) in the image is tested using the images located in the **test** directory.

Please refer to the code file for detailed implementation and comments.

**Note**: The dataset used in this code repository is specific to object detection of pens, sourced from [Roboflow](https://universe.roboflow.com/zainab-aldhanhani/pen-nsayu/dataset/1). Adjustments may be required for different datasets or object classes.

For any further questions or inquiries, please feel free to contact the repository owner.
