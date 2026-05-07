# Neural Network Foundations for Biological Prediction 🧠🧬

This module introduces the core principles of neural networks through a **from-scratch implementation of a single neuron**, with applications to **biological data modeling**.

It builds the conceptual and practical foundation required to understand and develop more advanced models such as **Multilayer Perceptrons (MLPs)** and deep learning systems used in biotech and drug discovery.

---

## 🎯 Objectives

- Understand how neural networks learn from data  
- Implement forward pass and gradient-based optimization from scratch  
- Analyze model behavior across different input dimensions (1D, 2D, 3D)  
- Explore the limitations of linear models  

---

## 🔬 Biological Context

The problems addressed in this module are simplified representations of real-world scenarios:

- Biological classification tasks  
- Prediction of experimental or molecular outcomes  
- Modeling relationships between biological variables  

💡 These concepts scale directly to:

- Drug discovery pipelines  
- Bioinformatics workflows  
- AI-driven biological prediction systems  

---

## ⚙️ Technical Approach

- Pure NumPy implementation (no high-level frameworks)  
- Forward propagation and activation functions  
- Binary cross-entropy loss  
- Manual gradient computation  
- Batch gradient descent training  

---

## 🧪 Experiments & Results

### 1. Neuron Behavior Analysis
- Response visualization in 1D, 2D and 3D  
- Comparison of activation functions (Sigmoid, ReLU, Tanh, Step)  
- Decision boundary interpretation  

### 2. Logical Functions Modeling
- AND, OR → successfully learned (linearly separable)  
- XOR → failure case demonstrating model limitations  

### 3. Training Dynamics
- Loss convergence over epochs  
- Gradient behavior analysis  
- Parameter updates and optimization  

---

## 🚨 Key Insight

A single neuron can only learn **linear decision boundaries**.

This limitation prevents it from solving problems like XOR, which require **non-linear modeling**.

---

## 🚀 Industry Relevance

This module demonstrates core competencies required in applied machine learning roles:

- Understanding of optimization and gradient-based learning  
- Ability to implement models from first principles  
- Interpretation of model behavior and limitations  
- Clear connection between theory and real-world applications  

💡 These skills are directly applicable to:

- AI in drug discovery  
- Computational biology  
- Data-driven modeling in biotech  

---

## 📊 Outputs

All generated artifacts are stored in `/results`:

- Training curves (`loss_*.png`)  
- Decision boundaries (`frontera_*.png`)  
- Model outputs (`resultados_*.txt`)  
- Neuron behavior visualizations  

---

## 📂 Project Structure
## 📂 Project Structure

```text
01_mlp_biological_prediction/
├── notebooks/
│   └── mlp_binary_classification_basics.ipynb
├── results/
├── environment.yml
├── README.md
```

---

## 🛠️ Tech Stack

- Python 3.11  
- NumPy  
- Matplotlib  
- Jupyter  

---

## 👩‍🔬 Author

**Salomé Gastaldi, PhD**  
Computational Biophysics | AI for Drug Discovery
