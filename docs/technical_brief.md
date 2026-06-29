# Technical Brief

## What This Shows

This project demonstrates a complete object-detection loop: annotation inspection, detector training, validation, and inference.

## Technical Decisions

- YOLO format keeps labels compact and directly compatible with Ultralytics.
- Bounding-box plotting verifies annotation quality before training.
- YOLOv8 nano is a sensible first detector for fast experimentation.
- mAP50 and mAP50-95 are both reported to distinguish loose detection from tighter localisation.

## Strongest Evidence

- End-to-end detector workflow rather than isolated inference.
- Multi-class setup with emergency and non-emergency vehicle classes.
- Metric reporting at the validation stage.
- Clear data contract for train/valid/test splits.

## Engineering Direction

- Add `train.py`, `evaluate.py`, and `predict.py` wrappers around Ultralytics.
- Export confusion matrix, PR curves, and example prediction images.
- Track dataset version, augmentation settings, and model weights.
- Add a model card covering intended use, class definitions, and operating boundaries.
