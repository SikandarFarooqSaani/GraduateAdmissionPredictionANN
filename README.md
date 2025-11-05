# 🎓 Graduate Admission Prediction using ANN  
**🧠 AI-Generated README (Custom Prompt for Clarity & Learning)**  

---

## 📌 Overview  
This project demonstrates how to build a simple **Artificial Neural Network (ANN)** to predict graduate admission chances using regression.  
Dataset is taken from **Kaggle’s Graduate Admission Prediction** dataset.  

The goal is to predict the **“Chance of Admit”** based on several applicant features such as GRE score, TOEFL score, CGPA, etc.  

---

## 🧰 Libraries Used  
- pandas  
- numpy  
- matplotlib  
- scikit-learn  
- tensorflow / keras  

---

## 📂 Dataset Information  
- Dataset obtained from **Kaggle**.  
- Contains **8 features** and **1 target (label)**.  
- Features include: GRE Score, TOEFL Score, University Rating, SOP, LOR, CGPA, Research, etc.  
- One serial column was dropped as it carried no predictive value.  
- No duplicate values found.  

---

## ⚙️ Preprocessing Steps  

1. **Feature-Label Split:**  
   - `X` → 8 input features.  
   - `y` → Target column “Chance of Admit”.  

2. **Train-Test Split:**  
   - Divided data into training and testing sets.  

3. **Scaling:**  
   - Used `MinMaxScaler` to scale all feature values between **0 and 1**.  
   - Chosen because feature bounds are known and it helps neural network convergence.  

---

## 🧩 Model Architecture  

- **Framework:** TensorFlow / Keras  
- **Type:** Regression ANN  

### Model Layers  
| Layer Type | Units | Activation | Notes |
|-------------|--------|-------------|--------|
| Input Layer | 7 | ReLU | Takes scaled feature input |
| Hidden Layer | 7 | ReLU | Single hidden dense layer |
| Output Layer | 1 | Linear | Since it’s a regression problem |

**Total Parameters:** 120  

---

## ⚙️ Compilation & Training  

- **Loss Function:** Mean Squared Error (MSE)  
- **Optimizer:** Adam  
- **Metric:** Mean Absolute Error (MAE)  

Trained for **100 epochs** with a **validation split of 0.2**.  
Training results were stored in the `history` object to visualize loss over epochs.  

---

## 📊 Model Performance  

- **R² Score:** 0.778  
  (Indicates a decent predictive strength but can be improved with deeper networks or tuning.)  
- **Observation:** Adding more hidden layers or increasing neurons may enhance performance.  

---

## 📈 Visualization  

**Image 1:** Loss curve showing training and validation error decreasing and stabilizing over epochs.  
This indicates proper learning and convergence of the ANN model.  

---

## 🧠 Key Insights  

- ANN performed reasonably well on a small dataset.  
- **MinMax scaling** was crucial for faster convergence.  
- Overfitting was avoided using validation split.  
- Further improvement possible via:
  - Adding dropout layers  
  - Increasing neurons/layers  
  - Using early stopping  

---

## 🖼️ <img width="556" height="415" alt="ANN1" src="https://github.com/user-attachments/assets/64a73760-0613-4642-b19e-3590fc00156a" />

1. Loss vs Epochs plot — shows decreasing and stabilizing training & validation loss  

---

📄 *Note: This README was AI-generated using a custom prompt for educational and documentation purposes.*
