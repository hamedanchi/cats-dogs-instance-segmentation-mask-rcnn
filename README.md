# Cats and Dogs Instance Segmentation using Mask R-CNN


# Cats and Dogs Instance Segmentation using Mask R-CNN

A computer vision project for detecting and segmenting cats and dogs at the pixel level using Mask R-CNN.

## Overview

This project implements Mask R-CNN for instance segmentation using Python, TensorFlow, and Keras.  
The model generates bounding boxes and segmentation masks for individual cats and dogs in images.

## Technologies

- Python
- TensorFlow
- Keras
- Mask R-CNN
- Computer Vision
- Jupyter Notebook

## Project Structure

- `Cats_and_Dogs_Mask_RCNN_Instance_Segmentation.ipynb` — model implementation and experiments
- `train1.zip` — training dataset
- `train2.zip` — additional training data
- `val.zip` — validation dataset
- `labels.rar` — annotation and label files

## Model

Mask R-CNN extends Faster R-CNN by adding a segmentation branch that predicts a pixel-level mask for each detected object.

## Results

The model performs:

- Cat and dog detection
- Bounding-box prediction
- Class prediction
- Pixel-level instance segmentation

## Future Improvements

- Add quantitative evaluation metrics
- Add prediction examples
- Improve dataset organization
- Improve reproducibility and code structure
