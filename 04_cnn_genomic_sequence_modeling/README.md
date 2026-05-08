# 🧬 CNN-Based Genomic Sequence Modeling & ChIP-seq Signal Prediction (Chr22)

This project implements a full deep learning pipeline for genomic sequence analysis using convolutional neural networks (CNNs), with application to transcription factor binding prediction and genome-wide signal reconstruction.

The workflow spans from synthetic sequence classification to **real genome-scale inference on chromosome 22**, integrating biological validation using ChIP-seq (BED) data.

---

## 🎯 Objectives

- Train CNN models for DNA sequence classification
- Optimize model architecture and regularization strategies
- Address severe class imbalance in genomic datasets
- Perform genome-wide sliding window inference
- Predict transcription factor binding regions (JunD)
- Validate predictions using experimental ChIP-seq data (BED format)

---

## 🧬 Biological Context

The project focuses on **transcription factor JunD binding sites**, which are:

- sparse across the genome
- context-dependent regulatory elements
- experimentally validated via ChIP-seq assays

The computational task is:

> Predict functional DNA regulatory regions directly from raw nucleotide sequence.

---

## ⚙️ Technical Approach

### Deep Learning Model
- 1D Convolutional Neural Network (CNN)
- One-hot encoding of DNA (A, C, G, T)
- Binary classification (binding vs non-binding)

### Training Strategy
- BCEWithLogitsLoss
- Class imbalance correction via `pos_weight`
- Adam optimizer

### Regularization Techniques
- Dropout
- Batch Normalization
- L2 weight decay (regularization tuning)

---

## 🧪 Experiments Summary

### 1. Hyperparameter Optimization
- Filters: 2 to 24
- Kernel sizes: 3 to 20
- Evaluated using ROC-AUC, PR-AUC, Accuracy

👉 Best performance achieved with intermediate model complexity (e.g. 16 filters, kernel size ~10)

---

### 2. Regularization Analysis

| Method | Behavior |
|--------|----------|
| BatchNorm | Faster convergence, mild overfitting |
| Dropout | Best generalization stability |
| L2 Regularization | Smooth training dynamics |

---

### 3. Class Imbalance Experiments

Best configuration:
- `pos_weight = 50`

Results:
- Strong improvement in ROC-AUC
- Significant gain in PR-AUC
- Optimal trade-off between sensitivity and stability

---

## 📊 Key Genomic Results (Chr22 Scanning)

Genome-wide inference was performed using sliding window prediction:

- Window size: 100 bp
- Step size: 20 bp
- Region: 20M–22M bp (Chr22)

### Final Results:

- Total peaks (BED): 561  
- Peaks in region: 143  
- Detected peaks: 122 / 143  
- False positive candidates: 579  

---

## 🧠 Biological Interpretation

The trained CNN behaves as a:

> **functional genomic signal detector**

Key findings:

- Learned convolutional filters capture motif-like DNA patterns
- Model generalizes from synthetic training data to real genomic regions
- High sensitivity to regulatory signal regions
- False positives may correspond to:
  - weak or unannotated regulatory elements
  - noisy genomic background
  - overlapping sliding window redundancy

---

## 📈 Key Insights

- CNNs effectively model DNA regulatory patterns
- Class imbalance is critical in genomic prediction tasks
- Optimal performance requires balanced regularization (Dropout + L2 + pos_weight tuning)
- Genome-wide inference is feasible using sliding window approaches
- Deep learning models can recover ChIP-seq-like signal structure

---

## 🔬 Scientific Contribution

This project demonstrates that:

> Deep convolutional models can reconstruct functional genomic landscapes from raw DNA sequence alone.

It bridges:
- machine learning sequence modeling
- and experimental genomics signal detection

---

## 🚀 Future Work

- Multi-chromosome generalization
- Multi-transcription factor prediction
- Transformer-based genomic architectures
- Integration with epigenomic datasets (ATAC-seq, histone marks)
- Model interpretability (motif extraction from CNN filters)

---

## 📂 Project Structure

```text
04_cnn_genomic_sequence_modeling/

├── notebooks/
│   ├── cnn_regularization_and_model_optimization.ipynb
│   ├── cnn_chip_seq_prediction.ipynb
│
├── results/
│   ├── model_final.pth
│   ├── chr22_signal_vs_bed.png
│   ├── hyperparameter_experiments.csv
│   ├── regularization_comparison.csv
│   ├── l2_experiments.csv
│   ├── metrics_comparison.csv
│   ├── roc_curve.png
│   ├── pr_curve.png
│   ├── roc_vs_complexity.png
│   ├── filters_comparison.png
│   ├── kernel_comparison.png
│   ├── loss curves (*.png)
│
├── chr22.fa
├── jun_np_chr22_GRCh38.bed  
├── sequences_upper.fasta
│
├── environment.yml
└── README.md
```

## 👩‍🔬 Author

**Salomé Gastaldi, PhD**  
Computational Biophysics | AI for Drug Discovery
