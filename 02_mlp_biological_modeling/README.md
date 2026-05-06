# 🧠 MLP for Biological Modeling

Implementation of **Multi-Layer Perceptrons (MLPs) from scratch (NumPy)** applied to:

- 📈 Non-linear regression
- 🎯 Multi-class classification

This project focuses on understanding **core deep learning mechanics**, including:
forward propagation, backpropagation, optimization, and the impact of key design choices such as **learning rate, architecture, activation functions, and training strategies**.

---

## 📁 Project Structure
02_mlp_biological_modeling/
│
├── notebooks/
│ ├── mlp_regression_non_linear_modeling.ipynb
│ └── mlp_multiclass_classification_from_scratch.ipynb
│
├── results/
│ ├── trained_prediction.png
│ ├── epochs_comparison.png
│ ├── lr_comparison.png
│ ├── architecture_comparison.png
│ ├── loss_epochs.png
│ ├── loss_lr.png
│ ├── loss_architecture.png
│ ├── dataset_tp3.png
│ ├── prediction_map_tp3.png
│ ├── confusion_matrix_tp3.png
│ ├── loss_tp3.png
│ ├── loss_minibatch.png
│ └── loss_relu.png
│
├── environment.yml
└── README.md


---

## ⚙️ Setup

```bash
conda env create -f environment.yml
conda activate mlp-biological-modeling

📊 Results

All results are generated from the final optimized implementations and reflect trained models only.

📈 Regression — Non-linear Function Approximation

A custom MLP is used to approximate a piecewise non-linear function.

🔍 Key Insights
The model successfully captures non-linear behavior
Performance depends strongly on:
number of epochs
learning rate
network architecture
📊 Outputs
Final prediction vs target → trained_prediction.png
Hyperparameter analysis:
Epochs → epochs_comparison.png
Learning rate → lr_comparison.png
Architecture → architecture_comparison.png
Loss evolution:
loss_epochs.png
loss_lr.png
loss_architecture.png
🎯 Classification — Multi-Class Angular Regions

The MLP is trained to classify 2D points into three angular regions.

⚠️ Baseline Model (Full Batch + Sigmoid)
Slow convergence
Limited performance (~63% accuracy)
Difficulty modeling decision boundaries

Outputs:

Loss curve → loss_tp3.png
Confusion matrix → confusion_matrix_tp3.png
🚀 Optimized Model (Mini-batch + ReLU)

A major improvement is achieved by introducing:

✔ Mini-batch gradient descent
✔ ReLU activation
✔ Better optimization dynamics
📊 Results
Accuracy: ~99.8%
Fast and stable convergence
Clear and sharp decision boundaries
📊 Outputs
Dataset visualization → dataset_tp3.png
Prediction map → prediction_map_tp3.png
Confusion matrix → confusion_matrix_tp3.png
Loss curves:
loss_minibatch.png
loss_relu.png
🧠 Key Learnings
✔ Backpropagation implemented from scratch
✔ Softmax + Cross-Entropy correctly derived
✔ Hyperparameter tuning is critical
✔ Activation functions drastically impact performance
✔ Mini-batch training improves convergence and stability
🚀 Takeaway

This project demonstrates how careful design choices transform a model from:

⚠️ Moderate performance (~63%)
→
🚀 Near-perfect classification (~99.8%)

It highlights the importance of:

model architecture
optimization strategy
activation functions

in real-world deep learning workflows.

👩‍💻 Author

Salomé Gastaldi, PhD
Computational Biophysics | AI for Drug Discovery
