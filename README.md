# Hybrid SAM-U-Net for Flood Segmentation

## Project Overview

This project investigates whether Segment Anything Model (SAM) image embeddings can improve flood segmentation performance when integrated with a U-Net architecture.

The study compares:

1. Baseline U-Net
2. Hybrid SAM-U-Net

using Sentinel-2 RGB imagery.

---

## Datasets

### STRUM Dataset

Used for:

* Training
* Validation
* Testing

Official train/validation/test split provided by STRUM is used.

### SEN12-FLOOD

Used for:

* Cross-dataset inference
* Generalization analysis

---

## Input Data

Only RGB Sentinel-2 bands are used:

* B04 (Red)
* B03 (Green)
* B02 (Blue)

Input Shape:

(3, H, W)

---

## Project Workflow

00_dataset_understanding.ipynb

* Dataset inspection
* Metadata analysis
* Band verification

01_preprocessing.ipynb

* Official split loading
* RGB extraction
* Normalization
* Resize

02_baseline_unet.ipynb

* Train baseline U-Net

03_sam_feature_extraction.ipynb

* Extract SAM image embeddings

04_hybrid_sam_unet.ipynb

* Train Hybrid SAM-U-Net

05_evaluation.ipynb

* Quantitative evaluation
* Metric comparison

06_sen12_inference.ipynb

* Cross-dataset testing

---

## Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1 Score
* Dice Score
* IoU
* mIoU

---

## Repository Structure

dataset/
notebooks/
checkpoints/
results/
reports/


---

## Research Objective

Evaluate whether SAM-enhanced feature representations improve flood segmentation compared to a standard U-Net baseline.

---

## Status

Project under active development.
