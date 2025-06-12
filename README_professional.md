# SignLanguage Project

**Explainable Transformer Architecture for Word-Level Sign Language Classification**

This project investigates a transformer-based approach to sign language recognition with a focus on interpretability through saliency visualization. The following document proposes a more polished version of the original README while retaining all image references.

## Project Overview
- Implements a transformer model for word-level sign language classification.
- Emphasizes explainability via saliency maps.
- Demonstrates improved accuracy and training speed compared with traditional recurrent models.

## Datasets
- **[AUTSL](https://cvml.ankara.edu.tr/datasets/)** &mdash; Sincan and Keles (2020).
- **[LSA-64](https://facundoq.github.io/datasets/lsa64/)** &mdash; Ronchetti et al. (2016).

Please cite these datasets if you use this work.

## Feature Extraction
- Utilizes pose estimation for skeleton-based motion features.
- Processes videos to 30 frames with 258 features per frame.

## Model Performance
- **AUTSL:** 86.26% accuracy with a 2-layer transformer and sinusoidal positional encoding.
- **LSA-64:** 90&ndash;94% accuracy after hyperparameter optimization.
- Outperforms LSTM baselines in accuracy and training speed.

## Explainability
- Saliency analysis highlights active hand movements and mid-frame regions.
- Misclassifications stem from overlapping trajectories.

## Technologies
- PyTorch for model implementation.
- MediaPipe for pose detection.
- Captum for saliency visualization.

## Data Analysis & Preprocessing

### 1. Mediapipe Keypoints
<p align="center">
    <img src="images/mediapipe.png">
</p>

### 2. Movement Trajectories (GIFs)
<p align="center" style="display: flex; justify-content: center; align-items: center; gap: 10px;">
    <img src="images/movements-ezgif.com-video-to-gif-converter.gif" width="40%">
    <img src="images/movements1-ezgif.com-video-to-gif-converter.gif" width="40%">
</p>
<p align="center"><b>Figure 1: GIFs showing average movement trajectories for different sign language sequences.</b></p>

### 3. Average Movement Trajectories
<p align="center" style="display: flex; justify-content: center; align-items: center; gap: 10px;">
    <img src="images/movements_autsl.png" width="45%">
    <img src="images/movements_lsa64.png" width="45%">
</p>
<p align="center"><b>Figure 2: Average movement trajectories in the AUTSL subset and LSA-64 dataset.</b></p>

## Experimental Results

### 4. Performance vs. Hyperparameters
<p align="center" style="display: flex; justify-content: center; align-items: center; gap: 10px;">
    <img src="images/performancevslayers.png" width="30%">
    <img src="images/performancevsnumheads.png" width="30%">
    <img src="images/performancevsdff.png" width="30%">
</p>
<p align="center"><b>Figure 3: Performance vs. number of layers, attention heads, and DFF size.</b></p>

### 5. Average Saliency Maps
<p align="center" style="display: flex; justify-content: center; align-items: center; gap: 10px;">
    <img src="images/saliencyautsl.png" width="45%">
    <img src="images/saliencylsa64.png" width="45%">
</p>
<p align="center"><b>Figure 4: Average saliency maps for AUTSL and LSA-64.</b></p>

### 6. Model Architecture
<p align="center">
    <img src="images/transformerarchitecture.png" width="60%">
</p>
<p align="center"><b>Figure 5: Transformer architecture for sign language classification.</b></p>

## Download Preprocessed Data
- **LSA-64**: [Google Drive](https://drive.google.com/drive/folders/1AjV780y033Cy9k9PV9Y2RBOndS1sG4Fd?usp=drive_link)
  - Path: `SignLanguageProject/data/landmarks_lsa64`
- **AUTSL**: [Google Drive](https://drive.google.com/drive/folders/1vupDY3DaFvmBdt_beXWIMqShPkHrcVeU?usp=drive_link)
  - Path: `SignLanguageProject/data/landmarks_autsl40`

After downloading, copy the files to the indicated directories.

## Contact
For questions or collaborations, please reach out at **Sadegh7644@gmail.com**.

