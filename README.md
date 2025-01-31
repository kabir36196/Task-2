# Leaf Detection Using YOLOv11

## Overview
This project implements leaf detection using the YOLOv11 (You Only Look Once) model. YOLOv11 is a real-time object detection system that processes images and identifies objects in a single pass. The model is trained to detect leaves in various environments, helping in applications like plant disease detection and environmental monitoring.

## Features
- Real-time leaf detection
- Uses YOLOv11 for efficient object detection
- Supports custom dataset training
- Can be extended to detect plant diseases

## Installation
1. Clone the repository:
   ```sh
   git clone <repository_url>
   cd Leaf_Detection_Using_YOLOv11
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Download the dataset and place it in the `data/` directory.

## Usage
1. To train the model:
   ```sh
   python train.py --dataset data/leaves --epochs 10
   ```
2. To run detection on an image:
   ```sh
   python detect.py --image test.jpg
   ```
3. To evaluate the model:
   ```sh
   python evaluate.py
   ```

## Dataset
The dataset consists of leaf images annotated with bounding boxes. If using a custom dataset, ensure it follows the YOLO format.

## Results
The model outputs images with detected leaves and confidence scores. These results can be further analyzed for applications like disease classification.


## License
This project is licensed under the MIT License.

## Acknowledgments
- **YOLO Algorithm**: Developed by Joseph Redmon et al.


