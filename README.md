# Leaf Detection using YOLOv5

This project focuses on detecting leaves using a custom-trained YOLOv5 model. The tutorial walks through dataset preparation, model training, and evaluation.

## Steps Covered
1. **Gather a dataset**: Collect images and label them with bounding boxes.
2. **Convert dataset to YOLOv5 format**: Use Roboflow or manual annotation tools.
3. **Train YOLOv5 on the dataset**: Perform custom training.
4. **Evaluate model performance**: Analyze results.
5. **Run inference**: Detect leaves in new images.

---

## Installation Requirements
Ensure you have the required dependencies installed:
```sh
pip install torch torchvision torchaudio
pip install ultralytics
pip install opencv-python
```

Clone the YOLOv5 repository:
```sh
git clone https://github.com/ultralytics/yolov5.git
cd yolov5
pip install -r requirements.txt
```

---

## Dataset Preparation
- Use **Roboflow** to label and export images in YOLOv5 format.
- Place the dataset inside the `datasets/` folder with `train`, `valid`, and `test` directories.

---

## Training the Model
Run the following command to train the model:
```sh
python train.py --img 640 --batch 16 --epochs 50 --data dataset.yaml --weights yolov5s.pt
```

---

## Running Inference
Once trained, test the model with:
```sh
python detect.py --weights runs/train/exp/weights/best.pt --source test_images/
```

---

## Results & Evaluation
- Precision, Recall, and mAP metrics will be displayed after training.
- Visualize detections using `detect.py`.

---

## References
- [YOLOv5 GitHub](https://github.com/ultralytics/yolov5)
- [Roboflow for Dataset Processing](https://roboflow.com/)

---
