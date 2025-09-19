# IDC Breast Cancer Classification (Custom CNN)

This project implements a **Convolutional Neural Network (CNN)** from scratch to classify histopathology images of **Invasive Ductal Carcinoma (IDC)** vs **Non-IDC** using the [Breast Histopathology Images Dataset](https://www.kaggle.com/datasets/paultimothymooney/breast-histopathology-images).

---

## Dataset
- **Source:** Kaggle ([Breast Histopathology Images](https://www.kaggle.com/datasets/paultimothymooney/breast-histopathology-images))  
- **Structure:**
  - `0/` → Non-IDC patches  
  - `1/` → IDC patches  
- Each image is a **50x50 px patch** extracted from breast tissue slides.

---

## Workflow
1. **Download dataset** from Kaggle.  
2. **Split patients** into:
   - 70% Training  
   - 20% Validation  
   - 10% Test  
3. **Data cleaning** – remove non-image files.  
4. **Oversampling** – balance minority class (IDC).  
5. **Data Augmentation** using `ImageDataGenerator`.  
6. **Custom CNN** with:
   - Conv2D + BatchNorm + MaxPooling  
   - Global Average Pooling  
   - Dense + Dropout layers  
   - L2 Regularization  
7. **Training with callbacks**:
   - EarlyStopping  
   - ReduceLROnPlateau  
8. **Evaluation**:
   - Accuracy & Loss curves  
   - Classification report (Precision, Recall, F1)  
   - Confusion matrix  

---

## Model Performance
- **Accuracy:** ~88% on test set  
- **Confusion Matrix & Classification Report** included.  
- Saved model: `IDC_Breast_Cancer_CNN.h5`  

---

## Results Visualization
- Training vs Validation **accuracy/loss curves**  
- **Sample images** from each class  
- **Confusion matrix**  

---

## How to Run
1. Upload your `kaggle.json` (API key).  
2. Run the notebook on **Google Colab** (GPU recommended).  
3. The model will train and save as `IDC_Breast_Cancer_CNN.h5`.

---

## Notes
- This project uses a **custom CNN**, not transfer learning.  
- Balancing and augmentation help improve generalization.  
- Further improvement possible with deeper networks or pre-trained models.  

---

👩‍💻 **Author:** Nada Emad  
