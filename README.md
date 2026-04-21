# SignLanguage-project  
## Explainable Transformer Architecture for Word-Level Sign Language Classification  

### Project Overview  
This project explores a **transformer-based model** for **word-level sign language classification**, with a strong emphasis on **model explainability**. The approach utilizes **saliency maps** to analyze and interpret model decisions, improving transparency in predictions.  

### Key Highlights  
- ** Datasets**  
This project uses publicly available sign language datasets:

  - **[AUTSL Dataset](https://cvml.ankara.edu.tr/datasets/)**  
    - Sincan, O. M., & Keles, H. Y. (2020). AUTSL: A Large Multi-Variability Dataset for Turkish Sign Language Recognition. *IEEE Transactions on Biometrics, Behavior, and Identity Science*.

  - **[LSA-64 Dataset](https://facundoq.github.io/datasets/lsa64/)**  
    - Ronchetti, F., Quiroga, F., Estrebou, C., Lanzarini, L., & Rosete, A. (2016). LSA64: A Dataset for Argentinian Sign Language Recognition. *IEEE Latin America Transactions*.

 If you use this work, please also **cite these datasets** accordingly.  

- ** Feature Extraction**:  
  - Used **pose estimation** and data preprocessing to extract skeletal motion features.  
  - Reduced videos to **30 frames with 258 features per frame** for efficiency.  
- ** Model Performance**:  
  - **AUTSL dataset**: Achieved **86.26% accuracy** using a **2-layer transformer with sinusoidal positional encoding**.  
  - **LSA-64 dataset**: Accuracy ranged between **90-94%** with optimized transformer configurations.  
- ** Comparisons**:  
  - Outperformed **LSTM models** in both **accuracy and training speed**.  
- ** Explainability**:  
  - **Saliency analysis** revealed the model’s focus on **active hand movements** and **mid-frame segments**.  
  - Misclassifications were linked to **overlapping hand trajectories**.  

## Technologies Used  
- **Deep Learning Frameworks**: PyTorch  
- **Preprocessing**: MediaPipe for pose detection  
- **Evaluation**: Loss, Accuracy, confusion matrices, Captum's saliency maps  

---

### Data Analysis & Preprocessing  
The following visualizations illustrate **average movement trajectories** in sign language datasets and the **MediaPipe-based preprocessing pipeline** used to extract skeletal motion features.

#### **1. Mediapipe Keypoints**
<p align="center">
    <img src="images/mediapipe.png">
</p>

### **2. Movement Trajectories (GIFs)**
<p align="center" style="display: flex; justify-content: center; align-items: center; gap: 10px;">
    <img src="images/movements-ezgif.com-video-to-gif-converter.gif" width="40%">
    <img src="images/movements1-ezgif.com-video-to-gif-converter.gif" width="40%">
</p>
<p align="center"><b>Figure 1: GIFs showing average movement trajectories for different sign language sequences.</b></p>

### **3. Average Movement Trajectories in Datasets**
<p align="center" style="display: flex; justify-content: center; align-items: center; gap: 10px;">
    <img src="images/movements_autsl.png" width="45%">
    <img src="images/movements_lsa64.png" width="45%">
</p>
<p align="center"><b>Figure 2: Average movement trajectories in the AUTSL subset and LSA-64 dataset.</b></p>

---

## Experimental Results  

#### **4. Performance vs Hyperparameters**
<p align="center" style="display: flex; justify-content: center; align-items: center; gap: 10px;">
    <img src="images/performancevslayers.png" width="30%">
    <img src="images/performancevsnumheads.png" width="30%">
    <img src="images/performancevsdff.png" width="30%">
</p>
<p align="center"><b>Figure 3: Performance vs Number of Layers, Number of Attention-Heads, and DFF.</b></p>

#### **5. Average Saliency Maps**
<p align="center" style="display: flex; justify-content: center; align-items: center; gap: 10px;">
    <img src="images/saliencyautsl.png" width="45%">
    <img src="images/saliencylsa64.png" width="45%">
</p>
<p align="center"><b>Figure 4: Average saliency maps for the AUTSL subset and LSA-64 dataset.</b></p>

#### **5. Model Architecture**
<p align="center">
    <img src="images/transformerarchitecture.png" width="60%">
</p>
<p align="center"><b>Figure 5: Transformer-based model architecture for sign language classification.</b></p>

---
###  Contact  
For any questions or research collaborations, feel free to reach out:  
📧 **Email:** sadegh.allahverdi@stud.uni-duisburg-essen.de

