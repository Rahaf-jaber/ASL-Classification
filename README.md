# ASL Classification (Arabic Sign Language) 

A clean, beginner-friendly notebook for training and evaluating a CNN-based classifier on an Arabic Sign Language (ASL) image dataset.

## Repo Structure
```
ASL-Classification/
├─ ASL_Classification.ipynb
├─ requirements.txt
├─ README.md
└─ dataset
```

## Setup

### Google Colab

- Open the notebook in Colab.

If using Drive, mount Drive and set dataset paths accordingly.

### Dataset

- Point the notebook to your dataset path.

- Common structure (customize as needed):
```
data/
├─ train/
│  ├─ A/  ├─ B/  ├─ C/  ...
└─ val/
   ├─ A/  ├─ B/  ├─ C/  ...
```

### How to Run

1- Open ASL_Classification.ipynb.
2- Run cells top-to-bottom. Adjust hyperparameters, batch size, image size, and dataset paths as needed.

### Evaluation

The notebook reports:

- Accuracy, loss curves

### Tips

- GPU strongly recommended for training (Colab / local CUDA).
- Use requirements.txt for reproducibility.

## Results

The model was trained on the Arabic Sign Language dataset with the following configuration:
- Image size: 64x64
- Batch size: 128
- Epochs: 17
- Optimizer: Adam
- Loss: Categorical Crossentropy

### Accuracy & Loss
| Metric        | Train | Validation |
|---------------|-------|------------|
| Accuracy      | 96.7% | 98.8%      |
| Loss          | 0.12  | 0.04       |

### Learning Curves
![Accuracy and Loss Curves](assets/accuracy_curve.png)

