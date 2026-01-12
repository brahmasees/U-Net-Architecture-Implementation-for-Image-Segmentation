# U-Net Architecture Implementation for Image Segmentation

## Project Overview
This project implements the **U-Net architecture** for semantic image segmentation, specifically applied to **brain tumor segmentation** using MRI scans. The goal is to accurately predict segmentation masks that identify the location of tumors within the MRI images.

## Key Features
- **Deep Learning Model:** Implements a standard U-Net architecture using **TensorFlow/Keras**.
- **Data Pipeline:** Includes data loading, preprocessing, and augmentation (rotation, shifts, zooms, flips) using Keras `ImageDataGenerator`.
- **Custom Metrics & Loss:** Utilizes specialized metrics and loss functions for segmentation tasks:
  - Dice Coefficient & Dice Loss
  - Weighted Cross-Entropy Loss
  - Combined Weighted Loss (Dice + Weighted CE)
  - IoU (Intersection over Union) Coefficient
- **Training & Evaluation:** Scripts for training the model, monitoring performance (accuracy, loss, IoU, Dice), and evaluating on a test set.
- **Visualization:** Tools to visualize training history and compare ground truth masks with model predictions.

## Dataset
The project uses the **LGG (Lower Grade Glioma) MRI Segmentation Dataset** (typically sourced from Kaggle/TCGA). The data consists of MRI images (`.tif`) and their corresponding segmentation masks (`_mask.tif`).

## Project Structure
- **`main.ipynb`**: The primary Jupyter Notebook containing the entire workflow: data preparation, model definition, training loop, evaluation, and visualization.
- **`unet.keras` / `unet_weighted.keras`**: Saved Keras model files containing the trained model weights.
- **`data/`**: Directory containing the dataset images and masks.

## Dependencies
- TensorFlow / Keras
- OpenCV (`cv2`)
- Scikit-learn
- Matplotlib
- Pandas
- NumPy
- skimage
- tqdm
