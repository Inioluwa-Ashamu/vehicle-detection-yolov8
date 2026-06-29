# Vehicle Detection with YOLOv8

Computer-vision portfolio project for detecting vehicle classes in road imagery using YOLO-format annotations and Ultralytics YOLOv8.

## Overview

The project trains an object detector for five classes:

- Ambulance
- Bus
- Car
- Motorcycle
- Truck

It includes notebook code for visualising YOLO bounding boxes, training a YOLOv8 nano model, validating detection metrics, and running sample predictions.

## Methods

- YOLO label parsing and bounding-box conversion.
- Image and annotation visualisation with OpenCV and matplotlib.
- Ultralytics YOLOv8 training.
- Validation with precision, recall, mAP50, and mAP50-95.
- Example inference on held-out test images.

## Results Snapshot

The assessment notebook reports validation performance around:

| Metric | Value |
| --- | ---: |
| Precision | 0.537 |
| Recall | 0.495 |
| mAP50 | 0.497 |
| mAP50-95 | 0.343 |

The project is useful as a compact demonstration of object-detection workflow literacy rather than a production-grade traffic model.

## Repository Structure

```text
.
├── notebooks/
│   └── vehicle_detection_yolov8.ipynb
├── data/
│   ├── data.yaml
│   └── README.md
├── docs/
│   └── portfolio_notes.md
├── requirements.txt
└── README.md
```

## Data

The full image dataset is not included in this portfolio copy. Place YOLO-format data under:

```text
data/Cars Detection/
├── train/images
├── train/labels
├── valid/images
├── valid/labels
├── test/images
└── test/labels
```

Then update `data/data.yaml` if paths differ.

## How to Run

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
```

Open `notebooks/vehicle_detection_yolov8.ipynb`.

## Limitations

- The dataset license/source should be documented before publishing data.
- The notebook is Colab-oriented and should be converted into scripts for repeatable local training.
- A future version should include a small public sample image plus an exported prediction visual.
