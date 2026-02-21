# Alzheimer’s Disease Stage Classification Using Inception-ResNet-V2

This repository presents a deep learning–based framework for **multi-class classification of Alzheimer’s disease stages from brain MRI images** using the **Inception-ResNet-V2** architecture. The proposed model achieves **98.08% validation accuracy** and demonstrates strong generalization across all disease stages.

---

## 📌 Problem Definition

Alzheimer’s disease (AD) is a progressive neurodegenerative disorder that requires early and accurate diagnosis for effective clinical intervention.

This project formulates AD diagnosis as a **supervised multi-class image classification problem**, where each MRI image is classified into one of four disease stages:

- **NonDemented**
- **VeryMildDemented**
- **MildDemented**
- **ModerateDemented**

---

## 🧠 Model Architecture

- **Backbone:** Inception-ResNet-V2  
- **Pretraining:** ImageNet  
- **Input Size:** 299 × 299 × 3  

### Classifier Head
- Global Average Pooling  
- Batch Normalization  
- Fully Connected Layers (512 → 256)  
- Dropout Regularization  
- Softmax Output (4 classes)

### Training Strategy
1. **Transfer Learning:** Backbone frozen, classifier head trained  
2. **Fine-Tuning:** Upper backbone layers unfrozen for performance refinement  

---


## Dataset Directory Structure

The dataset is organized into training and validation sets.  
Each set contains four classes representing different dementia stages.

data/
- train/
  - NonDemented/
  - VeryMildDemented/
  - MildDemented/
  - ModerateDemented/
- val/
  - NonDemented/
  - VeryMildDemented/
  - MildDemented/
  - ModerateDemented/



---

## 📊 Evaluation Metrics

- Accuracy  
- Precision, Recall, F1-score (per class)  
- Confusion Matrix  
- ROC-AUC (One-vs-Rest)  
- Prediction Confidence Distribution  
- Qualitative Visual Analysis (MRI → Prediction)

---

## 🏆 Results (Validation Set)

| Class | Precision | Recall | F1-Score |
|------|-----------|--------|----------|
| MildDemented | 1.00 | 0.99 | 0.99 |
| ModerateDemented | 1.00 | 1.00 | 1.00 |
| NonDemented | 0.98 | 0.99 | 0.98 |
| VeryMildDemented | 0.98 | 0.97 | 0.97 |

- **Overall Accuracy:** **98.08%**  
- **Macro F1-Score:** **0.99**  
- **ROC-AUC:** **> 0.99**

---

## 🖼️ Qualitative Results

The repository includes visual outputs showing:
- Original MRI images  
- Ground-truth labels  
- Predicted labels with confidence scores  

These results provide visual interpretability critical for medical AI research.

---

## 🛠️ Technologies Used

- Python  
- TensorFlow / Keras  
- NumPy  
- Scikit-learn  
- Matplotlib  
- Seaborn  

---

## 🚀 How to Run

### Clone the repository
```bash
git clone https://github.com/ihsafy/alzheimers-inception-resnet-v2.git
cd alzheimers-inception-resnet-v2

Install dependencies
pip install -r requirements.txt

Train or evaluate

Use the provided notebooks or scripts.

📄 Research & Academic Use

Suitable for:

Medical image analysis research

Alzheimer’s disease diagnosis studies

Deep learning coursework

Conference or journal extensions

Please cite appropriately if used in academic research.

📬 Contact

Author: IH Safy
Email: ihsafy2k21@gmail.com
