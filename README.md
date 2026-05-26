# CIFAR-10 CNN Classification

This repository contains a transfer learning image classification project for CIFAR-10 using TensorFlow/Keras and a ResNet50-based model.

## Repository structure

- `README.md` — project overview and how to run it
- `requirements.txt` — Python dependencies
- `notebooks/01_exploration_and_preprocessing.ipynb` — data loading, inspection, and preprocessing
- `notebooks/02_transfer_learning_resnet50.ipynb` — model building, transfer learning, fine-tuning, and evaluation

## Project goal

Build an end-to-end image classification workflow for CIFAR-10 that demonstrates:

- dataset loading and inspection
- image preprocessing for a pretrained CNN
- transfer learning with a frozen base model
- fine-tuning after unfreezing the base model
- evaluation and interpretation of results

## Dataset

The project uses the CIFAR-10 dataset available from `tensorflow.keras.datasets.cifar10`.

Classes:

- airplane
- automobile
- bird
- cat
- deer
- dog
- frog
- horse
- ship
- truck

## Environment setup

```bash
python -m venv .venv
source .venv/bin/activate  # macOS/Linux
# .venv\Scripts\activate   # Windows PowerShell
pip install -r requirements.txt
```

## Running the notebooks

```bash
jupyter notebook
```

Open the notebooks in the `notebooks/` directory and run them in order.

## Notes on model choice

This project follows the assignment requirement to use ResNet50 with ImageNet weights and an input shape of `(32, 32, 3)`. While pretrained CNNs are often used with larger image sizes, this repository intentionally follows the assignment specification.

## What to discuss in the presentation

- Why CIFAR-10 is a challenging dataset
- Why transfer learning was used
- Why preprocessing is required for ResNet50
- The difference between training only the head and fine-tuning the full model
- Training behavior, limitations, and possible next improvements
