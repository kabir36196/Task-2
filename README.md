# Leaf Detection using YOLOv5

This project focuses on detecting leaves using a custom-trained YOLOv5 model. The tutorial guides through dataset preparation, model training, and evaluation.

## Steps Covered
1. **Dataset Collection**: Gather and annotate images.
2. **Dataset Formatting**: Convert to YOLOv5 format.
3. **Model Training**: Train YOLOv5 on the dataset.
4. **Model Evaluation**: Assess performance.
5. **Inference**: Detect leaves in test images.

---

## Installation
Ensure dependencies are installed:
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
- Annotate images using **Roboflow** or LabelImg.
- Export dataset in YOLOv5 format.
- Organize into `train`, `valid`, and `test` directories.

---

## Training the Model
Run the following command:
```sh
python train.py --img 640 --batch 16 --epochs 70 --data dataset.yaml --weights yolov5s.pt
```

---

## Running Inference
Test the model with:
```sh
python detect.py --weights runs/train/exp/weights/best.pt --source test_images/
```

---

## Results & Evaluation
- View Precision, Recall, and mAP scores.
- Use `detect.py` to visualize detections.

---

## References
- [YOLOv5 GitHub](https://github.com/ultralytics/yolov5)
- [Roboflow](https://roboflow.com/) for dataset processing.

---

