
# Super-Market Shelves Detection Object-Detection

## Overview

This repository contains the code, annotated datasets, and models for the "Super-Market Shelves Detection Object-Detection" project. The project aims to automate the detection of empty and misaligned spaces on supermarket shelves using advanced machine learning techniques. By leveraging AI and computer vision, this project enhances inventory management and improves customer satisfaction in the retail sector.

## Features

- **Annotated Datasets**: Contains annotated datasets for each class (Empty, Misaligned, and Multi-class).
- **Pre-trained Models**: Includes all 9 models that were tested:
  - Base Model: SSD MobileNet V2 320x320
  - Intermediate Model: SSD MobileNet V2 FPNLite 320x320
  - Final Model: SSD MobileNet V2 FPNLite 640x640
- **Evaluation Scripts**: Tools for evaluating the models' performance using various metrics.

## Project Description

This project focuses on automating the monitoring of retail shelves by detecting empty and misaligned spaces. Using the SSD MobileNet V2 architecture, the project implements transfer learning to adapt pre-trained models for specific retail tasks. The goal is to improve inventory management and ensure continuous product availability, thereby enhancing customer satisfaction and driving sales.

### Findings

The table below summarizes the mean Average Precision (mAP) scores for each model configuration:

| Dataset                          | Models                        | mAP (%)                         |
|----------------------------------|-------------------------------|---------------------------------|
| **Empty Shelves**                | ssd-mobilenet-v2              | 9.07                            |
|                                  | ssd-mobilenet-v2-fpnlite-320  | 16.72                           |
|                                  | ssd-mobilenet-v2-fpnlite-640  | 35.93                           |
| **Misaligned Shelves**           | ssd-mobilenet-v2              | 0.95                            |
|                                  | ssd-mobilenet-v2-fpnlite-320  | 1.15                            |
|                                  | ssd-mobilenet-v2-fpnlite-640  | 0.23                            |
| **Empty and Misaligned Shelves** | ssd-mobilenet-v2              | Empty: 13.16, Misalignment: 0.65 |
|                                  | ssd-mobilenet-v2-fpnlite-320  | Empty: 17.40, Misalignment: 2.0 |
|                                  | ssd-mobilenet-v2-fpnlite-640  | Empty: 27.99, Misalignment: 1.13 |

## Usage

### Prerequisites

- Python 3.x
- TensorFlow
- Keras
- Other dependencies listed in `requirements.txt`

### Steps to Use the Repository

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Brxerq/Super-Market_Shelves_Detection_Object-Detection.git
   cd Super-Market_Shelves_Detection_Object-Detection
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt


3. **Data Collection and Annotation**
   - Use the scripts in the `data_collection` folder to gather and annotate images of supermarket shelves.

4. **Train the Model**
   - Configure your training parameters in the configuration file.
   - Run the training script:
     ```bash
     python train_model.py
     ```

5. **Evaluate the Model**
   - Use the evaluation scripts to assess model performance on test datasets:
     ```bash
     python evaluate_model.py
     ```

### Hugging Face Interface

Interact with the model using the Hugging Face interface provided:

[ShelvesDetection - a Hugging Face Space by brxerq](https://huggingface.co/spaces/brxerq/ShelvesDetection)

#### Instructions for Using the Hugging Face Interface

1. **Select the Model**: Choose the appropriate model for your task (Empty, Misaligned, or Multi-class). The Multi-class model is set by default.
2. **Image Upload**: Select a sample image or upload your own, then press "Submit Image".
3. **Video Upload**: Select the video option for processing. Note that it will take longer as each frame is processed individually.

## Prepared by

- Syed Muhammad Hassan Bin Ghayas
- Tan Chai Ching
- Chong Chao Sen
- Lau Lik Yang

## Git Repository

[GitHub Repository](https://github.com/Brxerq/Super-Market_Shelves_Detection_Object-Detection)

---

