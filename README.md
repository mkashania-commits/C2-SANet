# C²-SANet: Cascaded Complex-valued CNN with Spatial Attention for Accelerated MRI Reconstruction

This repository contains the official implementation of **C²-SANet**, a **Cascaded Complex-valued Convolutional Neural Network with Spatial Attention** for accelerated MRI reconstruction from undersampled k-space measurements.

The proposed framework exploits **complex-valued convolutions** to jointly process magnitude and phase information while incorporating **spatial attention** within a cascaded reconstruction architecture to improve reconstruction fidelity.

---

## ✨ Features

- Complex-valued convolutional neural network for MRI reconstruction
- Cascaded reconstruction framework
- Spatial attention mechanism
- Complex-valued activation functions
- 1D Cartesian k-space undersampling
- Training and evaluation notebooks
- Predefined train/validation/test splits
- Reproducibility resources including hyperparameters, random seeds, and computational profiling

---

# 📂 Repository Structure

```text
C2-SANet/
│
├── models/
│   ├── attention_train1.ipynb
│   ├── complex_1.ipynb
│   ├── complex_2.ipynb
│   ├── complex_zrelu.ipynb
│   ├── cs_models_sc.ipynb
│   ├── model2_attention_errormap.ipynb
│   ├── model_attention1.ipynb
│   ├── model_cbam_attention2.ipynb
│   └── simple_model.ipynb
│
├── utils/
│   ├── activation.ipynb
│   └── layer.ipynb
│
├── Training_Evaluation_Script/
│   ├── train_complex.ipynb
│   └── Evaluation.ipynb
│
├── UnderSampling_Mask/
│   └── var_sampling_mask.npy
│
├── splits/
│   ├── train.txt
│   ├── val.txt
│   └── test.txt
│
├── Hyperparameters_SEED/
│   └── C2-SANet_Hyperparameters_and_Seed.txt
│
├── requirements.txt
├── environment.yml
├── Computational_profiling.txt
└── README.md
```

---

# 🚀 Getting Started

## 1. Clone the Repository

```bash
git clone https://github.com/mkashania-commits/C2-SANet.git
cd C2-SANet
```

---

## 2. Install Dependencies

### Using Conda

```bash
conda env create -f environment.yml
conda activate c2-sanet
```

### Or Using pip

```bash
pip install -r requirements.txt
```

---

# 📊 Dataset

The experiments are conducted using the **fastMRI singlecoil Knee Dataset**.

Download the dataset and organize it into separate training, validation, and testing folders before running the training notebooks.

The repository also provides predefined dataset splits in the `splits/` directory to ensure reproducible experiments.

Example directory structure:

```text
Dataset/
│
├── train/
├── val/
└── test/
```

---

# 🎯 Undersampling Mask

A variable-density undersampling mask is provided in

```text
UnderSampling_Mask/var_sampling_mask.npy
```

This mask is used to generate undersampled k-space measurements during both training and evaluation.

---

# 🏗️ Model Construction

The proposed C²-SANet is implemented in a modular manner.

### Utility Modules

| Notebook | Description |
|----------|-------------|
| `activation.ipynb` | Complex-valued activation functions |
| `layer.ipynb` | Complex-valued layers and helper functions |

### Network Architectures

| Notebook | Description |
|----------|-------------|
| `complex_1.ipynb` | Complex-valued reconstruction blocks |
| `complex_2.ipynb` | Additional complex-valued modules |
| `model_attention1.ipynb` | Proposed C²-SANet architecture |
| `model_cbam_attention2.ipynb` | CBAM attention-based model |
| `simple_model.ipynb` | Baseline reconstruction model |

---

# 🏋️ Training

The primary training notebook is

```text
Training_Evaluation_Script/train_complex.ipynb
```

The training pipeline performs the following steps:

- Loads the  dataset
- Loads the  undersampling mask
- Constructs the C²-SANet architecture
- Optimizes the network parameters
- Saves trained model checkpoints

---

# 📈 Evaluation

Model evaluation is performed using

```text
Training_Evaluation_Script/Evaluation.ipynb
```

The evaluation notebook reconstructs MR images from undersampled k-space and computes quantitative reconstruction metrics.

---

# 🔄 Reproducibility

To facilitate reproducible research, the repository includes:

- Fixed train/validation/test splits
- Hyperparameter configuration
- Random seed information
- Computational profiling details

These resources are located in:

```text
splits/
Hyperparameters_SEED/
Computational_profiling.txt
```

---

# 📦 Requirements

The implementation is based on **Python** and **TensorFlow**.

Major dependencies include:

- TensorFlow
- NumPy
- SciPy
- h5py
- Matplotlib
- tqdm

All required packages are listed in:

- `requirements.txt`
- `environment.yml`

---

GitHub: https://github.com/mkashania-commits/C2-SANet

For questions, suggestions, or collaborations, please open an issue in this repository.
