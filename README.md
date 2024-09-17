# PSCS-50-CAPSTONE
Repository containing PSCS 50 final year Capstone project

Vehicle Authentication using License Plate Recognition
This project implements vehicle authentication by recognizing license plates using YOLOv10 for object detection and EasyOCR for optical character recognition (OCR). It automatically detects license plates in images or video streams and extracts the text for authentication purposes.

Table of Contents
Introduction
Features
Installation
Usage
Project Structure


Introduction
The goal of this project is to automate vehicle authentication by reading license plates from images or live video streams. This is useful in applications such as parking management, toll systems, and gate automation. YOLOv10 is used for fast and accurate license plate detection, while EasyOCR is utilized to extract the text from the detected plates.

Features
Detects vehicle license plates using YOLOv10.
Extracts text from the detected plates using EasyOCR.
Supports both image and video inputs.
Can be integrated with authentication or access control systems.

Installation

Clone this repository:
git clone https://github.com/your-username/vehicle-authentication-lpr.git
cd vehicle-authentication-lpr

Set up a virtual environment (optional but recommended):
python -m venv venv
source venv/bin/activate  # On Windows, use: venv\Scripts\activate

Install the required dependencies:
pip install -r requirements.txt

Ensure the following libraries are installed:
yolov5 (for YOLOv10, we'll use the PyTorch implementation)
easyocr
opencv-python
torch

Download the YOLOv10 pre-trained weights for vehicle and license plate detection:
wget https://path-to-yolov10-weights.com/yolov10-weights.pth

Usage
Detect License Plate in Images
Run the following command to detect a license plate from an image:
python detect.py --input path_to_image.jpg

Detect License Plate in Video
For video inputs, use:
python detect.py --input path_to_video.mp4 --video




Project Structure
vehicle-authentication-lpr/
│
├── models/                 # Pre-trained YOLOv10 model files
├── utils/                  # Utility functions for image and video processing
├── detect.py               # Main script for plate detection and OCR
├── requirements.txt        # Required Python libraries
├── README.md               # Project documentation
└── examples/               # Sample input images and videos
