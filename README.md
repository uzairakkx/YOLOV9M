# CCTV-Based Violence and Weapon Detection using YOLOv9m
This project implements real-time violence and weapon detection using the YOLOv9m object detection model trained on a custom CCTV surveillance dataset. The goal of this system is to automatically detect violent activities and weapons in surveillance footage, which can help improve public safety, smart surveillance systems, and automated security monitoring.

The repository includes both initial training and resume training implementations of YOLOv9m, allowing users to continue training from saved checkpoints.

# Project Overview

Violence and weapon-related incidents in public places are a major concern for security systems. Manual monitoring of CCTV cameras is inefficient and prone to human error. This project provides an AI-based automated solution capable of detecting:

# Violent activities
Weapons
Normal background scenes

The model is designed for real-time deployment in CCTV monitoring systems, enabling early threat detection and faster response.

# Dataset Description

A custom CCTV surveillance dataset was created specifically for this project.

Dataset Size
Total Images: ~8,000 images
Includes: Train, Validation, and Test sets
Classes

# The dataset contains 3 classes:

Weapon
Includes multiple types of weapons such as:
Knife
Gun
Rifle
Blunt weapons
Other weapon-like objects
Violence
Includes various violent activities such as:
Fighting
Snatching
Physical assault
Aggressive interactions
Background
Images without violence or weapons
Label files are empty .txt files
Annotation Format

# Annotations follow the YOLO format:

class_id x_center y_center width height

Each image has a corresponding .txt annotation file.

# Model Architecture

This project uses YOLOv9m (Medium version), a modern object detection architecture designed for high accuracy and real-time performance.

# Key characteristics:

One-stage object detection model
Efficient feature extraction
Multi-scale detection
Real-time inference capability
Optimized for GPU training

YOLOv9m provides a good balance between detection accuracy and computational efficiency, making it suitable for CCTV surveillance applications.

# Data Augmentation

To improve model generalization and robustness, heavy data augmentation was applied during training.

Augmentation techniques include:

Random horizontal flipping
Random scaling
Rotation
Color jittering
Mosaic augmentation
Random cropping
Brightness and contrast adjustments

These augmentations help the model learn robust features from different lighting conditions and viewpoints common in CCTV footage.

Training Strategy

The model was trained using two training strategies:

Initial Training

The model is trained from pretrained YOLOv9 weights using the custom dataset.

Steps include:

Dataset loading
Augmentation pipeline
Model initialization
Training with optimized hyperparameters
Resume Training

Resume training allows the model to continue training from a saved checkpoint, which is useful when:

Training is interrupted
Additional epochs are required
Fine-tuning is needed

Checkpoint files store:

Model weights
Optimizer state
Training progress
