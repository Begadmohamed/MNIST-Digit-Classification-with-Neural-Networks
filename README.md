# 🖊️ MNIST Digit Classification with Neural Networks  

This project implements and experiments with different deep learning techniques to classify handwritten digits from the **MNIST dataset**.  

---

## 🚀 Features & Techniques Used  

### 🔹 Data Preprocessing  
- Normalized pixel values (0–255 → 0–1)  
- Train/Validation/Test split  

### 🔹 Model Architecture  
- Feedforward Neural Network (Dense layers)  
- Experiments with different:  
  - Numbers of hidden layers and neurons  
  - Activation functions (`relu`, `softmax`, etc.)  

### 🔹 Training Strategies  
- **Callbacks**: EarlyStopping (to avoid overfitting & restore best weights)  
- Optimizer experiments: `adam`, `sgd`  
- Different **batch sizes** tested  
- Regularization: **Dropout** & **Batch Normalization**  

### 🔹 Hyperparameter Tuning  
- Used **RandomizedSearchCV** with `scikeras.wrappers.KerasClassifier`  
- Tuned hyperparameters:  
  - Number of layers (`nl`)  
  - Number of neurons per layer (`nn`)  
  - Optimizer (`adam`, `sgd`)  
  - Dropout rates  
  - Batch size & epochs  

---

## 📊 Results & Metrics  

- **Best Validation Accuracy**: `98.18%` (at Epoch 15)  
- **Test Accuracy**: `97.93%`  
- **Test Loss**: `0.0740`  

### 🔹 Classification Report  

| Digit | Precision | Recall | F1-score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.98      | 0.99   | 0.99     | 980     |
| 1     | 0.99      | 0.99   | 0.99     | 1135    |
| 2     | 0.97      | 0.98   | 0.98     | 1032    |
| 3     | 0.96      | 0.98   | 0.97     | 1010    |
| 4     | 0.98      | 0.98   | 0.98     | 982     |
| 5     | 0.98      | 0.97   | 0.98     | 892     |
| 6     | 0.99      | 0.98   | 0.98     | 958     |
| 7     | 0.98      | 0.98   | 0.98     | 1028    |
| 8     | 0.96      | 0.97   | 0.97     | 974     |
| 9     | 0.99      | 0.97   | 0.98     | 1009    |

**Overall Accuracy**: `98%`  
- **Macro Avg** → Precision: `0.98` | Recall: `0.98` | F1-score: `0.98`  
- **Weighted Avg** → Precision: `0.98` | Recall: `0.98` | F1-score: `0.98`  

---

## 🔥 Confusion Matrix  

- A **heatmap** was plotted to visualize model predictions vs. true labels.  

---

## 📌 Summary  

This project demonstrates:  
- How different deep learning strategies affect MNIST digit classification.  
- The effectiveness of regularization (Dropout & Batch Normalization).  
- The power of hyperparameter tuning with **RandomizedSearchCV**.  

Final performance shows the model achieving **~98% accuracy** on unseen test data.  
