# Surveillance-monitoring-model-based-on-gaze-direction-tracking
This repository contains two annotated datasets, created and augmented with Roboflow, and exported in formats ready for training and evaluation.
Repository Contents
1. eye-detection.zip
   
Annotated dataset for eye region detection. Images are split into train / val / test. For every image, the corresponding label file is a YOLOv8 .txt containing bounding‑box coordinates (one line per object) in the format: <class_id> <x_center> <y_center> <width> <height>. All coordinates are normalized to [0, 1] relative to image width/height.

2. gaze-classification.zip
   
Dataset for gaze classification, prepared for training and evaluation with clearly separated train / val / test subsets and class labels.

**Export & Provenance**

- Exported via: roboflow.com

- Export time: October 19, 2025 at 10:27 AM GMT

- Provided by: a Roboflow user

- License: CC BY 4.0

**Pre‑processing (applied to each image)**

- Auto‑orientation of pixel data (EXIF orientation stripped)

- Resize to 640×640 (fit within)

**Augmentations (2 versions per source image)**

- Random rotation between −10° and +10°

- Random brightness adjustment between −18% and +18%

- Salt‑and‑pepper noise applied to 0.3% of pixels

- Grayscale applied with 15% probability

**Quick Start**

YOLOv8 detection training (for eye-detection.zip): use the provided data.yaml with the standard Ultralytics command (adjust paths as needed).

Gaze classification: load images and labels from the train / val / test splits into your preferred framework (PyTorch/TensorFlow) and train a classifier.

**Citation**

If you use these datasets in your research, please cite this repository and include the license information (CC BY 4.0).



