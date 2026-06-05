# Age-Group-Estimation-from-Faces

This project focuses on **age-group classification** using facial images from the [UTKFace dataset](https://susanqq.github.io/UTKFace/). The core objective is to categorize images into three distinct age groups (Young, Adult, Old) rather than predicting a specific age, simplifying the learning process and improving performance.

---

# Age Group Classifier

## Project Overview

This project leverages deep learning to perform multi-class classification on facial images. By grouping ages, the model provides a more robust estimate of a person's life stage.

### Age Class Definitions

The dataset is processed into the following categories:

| Class | Age Range |
| --- | --- |
| **Young** | 0–25 years |
| **Adult** | 26–50 years |
| **Old** | 51+ years |

---

## Directory Structure

The project automatically sets up the following structure to manage data, models, and logs efficiently:

```text
project_root/
├── project_data/          # Processed metadata (e.g., metadata.csv)
├── project_figures/       # Visualizations (e.g., age_distribution.pdf)
├── saved_models/          # Trained model weights/checkpoints
├── evaluation_results/    # Confusion matrices, accuracy logs, etc.
└── logs/                  # Training logs

```

---

## Technical Stack

* **Language:** Python 3.12
* **Core Libraries:**
* `TensorFlow/Keras`: For building and training the deep learning model.
* `Pandas/NumPy`: For data manipulation and metadata management.
* `Scikit-learn`: For dataset splitting.
* `Matplotlib/PIL`: For image visualization and processing.



---

## Usage Instructions

1. **Data Preparation:** Ensure the UTKFace dataset is available at the specified path (`/kaggle/input/datasets/jangedoo/utkface-new/UTKFace`).
2. **Execution:** Run the Jupyter notebook cells in order. The notebook performs the following steps:
* **Folder Setup:** Automatically creates the necessary subdirectories.
* **Data Exploration:** Extracts ages from filenames, calculates statistics, and visualizes the distribution to understand the data balance.
* **Modeling (Next Steps):** The structure is prepared for data augmentation, splitting, and model architecture definition.



---

## Key Findings

* **Dataset Size:** 23,708 valid facial images.
* **Age Statistics:**
* Mean Age: ~33 years.
* Age Range: 1–116 years.
* The distribution is right-skewed, which informed the decision to use age-group buckets for better model stability.
