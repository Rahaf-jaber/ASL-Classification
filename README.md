# ASL Classification (Arabic Sign Language) 👋

A clean, beginner-friendly notebook for training and evaluating a CNN-based classifier on an Arabic Sign Language (ASL) image dataset.

## Features
- Single Jupyter notebook workflow (`ASL_Classification.ipynb`)
- CNN baseline you can swap/extend
- Clear metrics & confusion matrix
- Simple repo layout for students and workshops

## Repo Structure

## Setup

### Google Colab

- Open the notebook in Colab.

If using Drive, mount Drive and set dataset paths accordingly.

### Dataset

- Point the notebook to your dataset path.

- Common structure (customize as needed):
data/
├─ train/
│  ├─ A/  ├─ B/  ├─ C/  ...
└─ val/
   ├─ A/  ├─ B/  ├─ C/  ...

### How to Run

1- Open ASL_Classification.ipynb.
2- Run cells top-to-bottom. Adjust hyperparameters, batch size, image size, and dataset paths as needed.

### Evaluation

The notebook reports:

- Accuracy, loss curves
- Classification report
- Confusion matrix

### Tips

- GPU strongly recommended for training (Colab / local CUDA).
- Use requirements.txt for reproducibility.

## Results

The model was trained on the Arabic Sign Language dataset with the following configuration:
- Image size: 64x64 (adjust if different)
- Batch size: 32
- Epochs: 20
- Optimizer: Adam
- Loss: Categorical Crossentropy

### Accuracy & Loss
| Metric        | Train | Validation |
|---------------|-------|------------|
| Accuracy      | 95%   | 92%        |
| Loss          | 0.18  | 0.25       |

### Learning Curves
![Accuracy Curve](assets/accuracy_curve.png)
![Loss Curve](assets/loss_curve.png)

### Confusion Matrix
![Confusion Matrix](assets/confusion_matrix.png)

### Observations
- The model generalizes well with only minor overfitting after ~15 epochs.
- Class `X` was confused with `Y` most often — future work could explore data augmentation.
- GPU runtime: ~15 minutes on Google Colab (T4).
