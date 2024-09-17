# Vehicle Authentication using License Plate Recognition

This project implements vehicle authentication by recognizing license plates using YOLOv10 for object detection and EasyOCR for optical character recognition (OCR). It automatically detects license plates in images or video streams and extracts the text for authentication purposes.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)


## Introduction
The goal of this project is to automate vehicle authentication by reading license plates from images or live video streams. This is useful in applications such as parking management, toll systems, and gate automation. YOLOv10 is used for fast and accurate license plate detection, while EasyOCR is utilized to extract the text from the detected plates.

## Features
- Detects vehicle license plates using YOLOv10.
- Extracts text from the detected plates using EasyOCR.
- Supports both image and video inputs.
- Can be integrated with authentication or access control systems.

## Installation

1. Clone this repository:

    ```bash
    git clone https://github.com/your-username/vehicle-authentication-lpr.git
    cd vehicle-authentication-lpr
    ```

2. Set up a virtual environment (optional but recommended):

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use: venv\Scripts\activate
    ```

3. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

    Ensure the following libraries are installed:
    - `yolov5` (for YOLOv10, we'll use the PyTorch implementation)
    - `easyocr`
    - `opencv-python`
    - `torch`

4. Download the YOLOv10 pre-trained weights for vehicle and license plate detection:

    ```bash
    wget https://path-to-yolov10-weights.com/yolov10-weights.pth
    ```

## Usage

### Detect License Plate in Images

Run the following command to detect a license plate from an image:

```bash
python detect.py --input path_to_image.jpg
```

## Project-structure
```
vehicle-authentication-lpr/
│
├── models/                 # Pre-trained YOLOv10 model files
├── utils/                  # Utility functions for image and video processing
├── detect.py               # Main script for plate detection and OCR
├── requirements.txt        # Required Python libraries
├── README.md               # Project documentation
└── examples/               # Sample input images and videos
