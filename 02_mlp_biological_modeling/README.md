# 🧠 MLP for Biological Modeling

## 🎯 Objective

This project explores how neural networks learn by implementing **Multi-Layer Perceptrons (MLPs) from scratch using NumPy**.

The goal is not just to train models, but to deeply understand:
- Forward & backward propagation
- Optimization dynamics
- Impact of architecture and hyperparameters
- Role of activation functions in learning behavior

Applications:
- 📈 Non-linear regression
- 🎯 Multi-class classification

---

## 📁 Project Structure

```text
02_mlp_biological_modeling/
├── notebooks/
│   ├── mlp_regression_non_linear_modeling.ipynb
│   └── mlp_multiclass_classification_from_scratch.ipynb
├── results/
│   ├── trained_prediction.png
│   ├── epochs_comparison.png
│   ├── lr_comparison.png
│   ├── architecture_comparison.png
│   ├── loss_epochs.png
│   ├── loss_lr.png
│   ├── loss_architecture.png
│   ├── dataset_tp3.png
│   ├── prediction_map_tp3.png
│   ├── confusion_matrix_tp3.png
│   ├── loss_tp3.png
│   ├── loss_minibatch.png
│   └── loss_relu.png
├── environment.yml
└── README.md
```

---

## ⚙️ Setup

```bash
conda env create -f environment.yml
conda activate mlp-biological-modeling
```

---

## 📊 Results Overview

### 📈 Non-linear Regression

A custom MLP learns a piecewise non-linear function.

**Key insights:**
- Captures complex non-linear patterns
- Strong dependency on:
  - learning rate
  - number of epochs
  - network architecture

**Results:**
- `trained_prediction.png` → model fit
- `epochs_comparison.png` → training duration effect
- `lr_comparison.png` → learning rate sensitivity
- `architecture_comparison.png` → model capacity impact
- `loss_*` plots → training dynamics

---

### 🎯 Multi-class Classification

The model classifies 2D points into angular regions.

#### ⚠️ Baseline Model (Full Batch + Sigmoid)
- Slow convergence  
- Limited decision boundary quality  
- ~63% accuracy  

**Outputs:**
- `loss_tp3.png`
- `confusion_matrix_tp3.png`

---

#### 🚀 Optimized Model (Mini-batch + ReLU)

Key improvements:
- ✔ Mini-batch gradient descent  
- ✔ ReLU activation  
- ✔ Improved optimization stability  

**Results:**
- ~99.8% accuracy  
- Fast convergence  
- Well-defined decision boundaries  

**Outputs:**
- `dataset_tp3.png`
- `prediction_map_tp3.png`
- `confusion_matrix_tp3.png`
- `loss_minibatch.png`
- `loss_relu.png`

---

## 🧠 Key Learnings

- Backpropagation works as a modular computational graph
- Activation functions drastically affect learning dynamics
- Optimization strategy (batch vs mini-batch) is critical
- Hyperparameter tuning is often as important as architecture
- Small implementation details strongly impact performance

---

## 🚀 Takeaway

A simple MLP goes from:

⚠️ ~63% accuracy (unstable training)  
→  
🚀 ~99.8% accuracy (stable + optimized training)

This highlights how **architecture + optimization choices define model success**, even in simple neural networks.

---

## 👩‍💻 Author

**Salomé Gastaldi, PhD**  
Computational Biophysics | AI for Drug Discovery
