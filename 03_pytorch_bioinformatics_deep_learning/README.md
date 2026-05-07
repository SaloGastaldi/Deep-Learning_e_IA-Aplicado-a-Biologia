# 🧬 Deep Learning for Bioinformatics (PyTorch)

This project applies PyTorch-based neural networks to DNA sequence classification problems, extending previous work on neural networks and MLPs into a real bioinformatics context.

It focuses on understanding how model design, data representation, and biological realism affect performance and interpretability.

---

## 🎯 Objectives

- Apply deep learning to DNA sequence classification
- Study impact of biological realism on model performance
- Analyze effect of dataset size and sequence length
- Explore interpretability of learned representations

---

## 🧬 Biological Context

This project models simplified genomic classification tasks:

- Promoter vs non-promoter DNA sequences
- Random and mutated negative samples
- Sequence-based classification problems

These tasks are representative of real-world bioinformatics applications such as:

- Gene regulation analysis
- Genomic sequence modeling
- AI-assisted biological prediction

---

## ⚙️ Technical Approach

- PyTorch fully connected neural networks (MLPs)
- One-hot encoding of DNA sequences (A, T, C, G)
- Binary classification using BCEWithLogitsLoss
- Adam / SGD optimization
- Mini-batch training using DataLoader

---

## 🧪 Experiments

### 1. Baseline classification
- Simple promoter classification task
- High performance in synthetic settings

---

### 2. Negative sampling strategies

- Random sequences → easy classification
- Mutated sequences → more realistic and difficult task

👉 Biological realism significantly reduces performance.

---

### 3. Dataset size impact

- Small datasets → unstable learning
- Larger datasets → no consistent improvement

---

### 4. Sequence length impact

- Short sequences → better performance
- Long sequences → degraded accuracy

👉 High-dimensional inputs introduce noise and optimization challenges.

---

### 5. Interpretability

- Feature importance extracted from first layer weights
- No clear positional motifs detected
- Importance distributed across sequence positions

---

## 📊 Key Results

- Good performance in simplified tasks
- Strong degradation under realistic biological conditions
- High sensitivity to data design
- Limited interpretability of MLP models for sequence data

---

## 🧠 Key Insights

- Data design is critical in bioinformatics ML
- Biological realism significantly affects performance
- MLPs lack inductive bias for sequence structure
- One-hot encoding leads to high-dimensional sparse inputs
- Deep learning performance depends heavily on representation

---

## 🚀 Conclusions

This project shows that:

> Fully connected neural networks can solve simplified DNA classification tasks but fail to generalize under realistic biological conditions.

---

## 🔭 Future Work

- Convolutional Neural Networks (CNNs) for motif detection
- k-mer embeddings for compact representations
- Transformer models for sequence learning
- Improved negative sampling strategies

---

## 📂 Project Structure
```text
03_pytorch_bioinformatics_deep_learning/

├── notebooks/
│   └── TP4_PyTorch_bioinformatics.ipynb
│
├── results/
│   ├── dataset_size_4_4.png
│   ├── sequence_length_4_5.png
│   ├── feature_importance_4_6.png
│   ├── loss_train_val_4_2.png
│   ├── roc_curves_4_2.png
│   ├── hist_train_4_3.png
│   └── hist_val_4_3.png
│
├── environment.yml
└── README.md
```
## 👩‍🔬 Author

**Salomé Gastaldi, PhD**  
Computational Biophysics | AI for Drug Discovery
