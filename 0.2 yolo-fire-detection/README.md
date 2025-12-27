# YOLOv8 Fire Detection

This project implements a fire detection model using the YOLOv8 object detection framework.

The focus of this work is **practical fire detection**, prioritizing precision by filtering inference results to fire-only predictions with higher confidence thresholds. This design choice reduces noisy false positives caused by visually ambiguous smoke patterns.

## Contents
- `best-final.pt`: Trained YOLOv8 model weights

## Notebook
The full training and inference workflow is documented in the Kaggle notebook:
[https://www.kaggle.com/code/abdosorour/fire-detection]
## Notes
Prediction images are not included in this repository to keep it lightweight and focused on core deliverables.  
Full qualitative results, visualizations, and experimental analysis are available in the accompanying Kaggle notebook.
