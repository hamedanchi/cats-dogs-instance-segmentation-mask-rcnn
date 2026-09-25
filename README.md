# Cats and Dogs Instance Segmentation with Mask R-CNN

A computer vision project for detecting and segmenting cats and dogs at the pixel level using Mask R-CNN, PyTorch, and Detectron2.

## Overview

This project applies instance segmentation to images of cats and dogs using a Mask R-CNN model implemented with Detectron2.

Unlike standard object detection, which only predicts bounding boxes, instance segmentation also generates a pixel-level mask for each detected object.

The model is based on the Mask R-CNN R50-FPN architecture and uses transfer learning from Detectron2's pretrained COCO model.

## Features

- Cat and dog object detection
- Pixel-level instance segmentation
- Bounding-box prediction
- Segmentation mask generation
- Transfer learning with pretrained Mask R-CNN
- COCO-format dataset support
- Model evaluation using COCO metrics
- Visualization of predicted masks and bounding boxes

## Technologies

- Python
- PyTorch
- Detectron2
- Mask R-CNN
- OpenCV
- NumPy
- Matplotlib
- Roboflow
- COCO Dataset Format
- Google Colab

## Dataset

The dataset was prepared using Roboflow and exported in COCO format.

The dataset used in the experiment contains:

- 240 training images
- 40 validation images

COCO annotations are used for object bounding boxes and segmentation masks.

## Model Architecture

The project uses:

`mask_rcnn_R_50_FPN_3x`

from the Detectron2 Model Zoo.

The model combines:

- ResNet-50 backbone
- Feature Pyramid Network (FPN)
- Region Proposal Network (RPN)
- Bounding-box prediction
- Classification
- Instance mask prediction

Pretrained COCO weights are used to initialize the model before fine-tuning it on the custom dataset.

## Training Configuration

The main training configuration includes:

- Batch size: 2
- Base learning rate: 0.00025
- Maximum iterations: 10,000
- Early stopping patience: 500 iterations
- ROI batch size per image: 512

Early stopping is used to terminate training when the loss no longer improves.

## Evaluation

The model was evaluated on the validation dataset using Detectron2's COCOEvaluator.

### Bounding Box Detection

| Metric | Score |
|---|---:|
| AP | 75.88 |
| AP50 | 93.35 |
| AP75 | 91.32 |

### Instance Segmentation

| Metric | Score |
|---|---:|
| AP | 76.58 |
| AP50 | 93.35 |
| AP75 | 89.38 |

These results are from the experiment stored in the current notebook.

## Prediction Visualization

The trained model generates:

- Object bounding boxes
- Predicted classes
- Confidence scores
- Pixel-level segmentation masks

Prediction results are visualized using Detectron2's `Visualizer`.

## Project Structure

```text
cats-dogs-instance-segmentation-mask-rcnn/
│
├── Cats_and_Dogs_Mask_RCNN_Instance_Segmentation.ipynb
├── train1.zip
├── train2.zip
├── val.zip
├── labels.rar
└── README.md
