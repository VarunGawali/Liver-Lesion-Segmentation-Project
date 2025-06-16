# Liver-Lesion-Segmentation-Project
This repository contains a Jupyter Notebook implementing a U-Net model for liver lesion segmentation in CT scans, enhanced with a multi-cycle training loop to improve performance. The project focuses on preprocessing medical imaging data, training a deep learning model, and visualizing results through plots of training loss, Dice scores, and segmentation predictions.

## Project Overview
Liver lesion segmentation is a critical task in medical imaging for diagnosing and treating liver diseases, such as tumors or metastases. This project uses a U-Net model with a ResNet18 backbone to segment liver lesions from CT scans. The notebook includes data preprocessing, model training, evaluation, and visualization of results, making it a comprehensive resource for medical imaging research.

### Key Features
- U-Net Model: Utilizes a pretrained U-Net with a ResNet18 backbone from the segmentation_models_pytorch library, fine-tuned for liver lesion segmentation.
- Data Preprocessing: Processes DICOM CT scans and masks, resizing them to 128x128 and normalizing pixel intensities for training.
- Data Augmentation: Applies random flips, rotations, affine transformations, and crops to improve model robustness.
- Custom Loss Functions: Combines BCE, Dice, and Tversky losses with weighted positive classes to handle class imbalance in lesion segmentation.
- Visualization: Includes functions to plot training loss (plot_loss), Dice coefficients (plot_dice), and segmentation predictions (plot_prediction) with raw probability heatmaps.
- Evaluation Metrics: Uses the Dice coefficient to evaluate segmentation performance, with a focus on improving overlap between predicted and ground truth masks.

## Results
- Dice Score: Achieved a Dice coefficient of 0.4244 after 3 cycles of training (5 epochs total), up from 0.34 in a single-cycle approach, indicating moderate performance with room for further improvement.
- Visualizations: The notebook includes plots of:
    - Training loss per cycle, with cycle boundaries for clarity.
    - Dice coefficients over epochs, showing performance trends.
    - Segmentation predictions with ground truth masks and raw probability heatmaps, highlighting areas of improvement.

## Dataset
This project uses the 3Dircadb1 dataset, a publicly available dataset for liver and lesion segmentation research. The dataset contains CT scans and corresponding lesion masks in DICOM format.
  
