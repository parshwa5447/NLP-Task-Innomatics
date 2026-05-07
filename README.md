# BERT Fine-Tuning for Sentiment Analysis

## 📌 Project Overview

This project demonstrates how to fine-tune a pre-trained BERT (Bidirectional Encoder Representations from Transformers) model for Sentiment Analysis using the Hugging Face Transformers library and PyTorch.

The project covers the complete NLP pipeline including:
- Text preprocessing
- Tokenization
- BERT fine-tuning
- Model training
- Evaluation
- Experimental comparison

The main goal is to understand how transformer-based models work for text classification tasks.

---

# 🎯 Objective

Build a text classification model using a pre-trained BERT model and evaluate its performance using multiple classification metrics.

---

# 📂 Dataset Used

Dataset: **IMDb Movie Reviews Dataset**

The dataset contains:
- Movie reviews
- Sentiment labels:
  - Positive
  - Negative

Dataset Source:
Kaggle IMDb Reviews Dataset

---

# 🚀 Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- Scikit-learn
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

---

# 🧠 Concepts Covered

- Natural Language Processing (NLP)
- Transformer Architecture
- BERT Tokenization
- Fine-Tuning Pre-trained Models
- Text Classification
- Transfer Learning
- Model Evaluation

---

# 🔄 Project Pipeline

```text
Raw Data
   ↓
Text Preprocessing
   ↓
Train / Validation / Test Split
   ↓
BERT Tokenization
   ↓
Fine-Tuning BERT
   ↓
Model Evaluation
   ↓
Performance Comparison
```

---

# 🛠️ NLP Preprocessing Steps

The following preprocessing techniques were applied:
- Lowercasing
- Removing HTML tags
- Removing URLs
- Removing special characters
- Handling missing values

---

# 🔤 Tokenization

The project uses:

```python
bert-base-uncased
```

tokenizer from Hugging Face Transformers.

The tokenizer converts raw text into:
- Input IDs
- Attention Masks

which are suitable inputs for BERT.

---

# 🤖 Model Used

Pre-trained Model:

```python
AutoModelForSequenceClassification
```

Base Model:

```python
bert-base-uncased
```

Optimizer Used:
- AdamW

Learning Rate:
```python
2e-5
```

---

# 🧪 Experiments Performed

## Experiment 1: Freeze BERT Layers
- Faster training
- Lower computational cost
- Slightly lower accuracy

## Experiment 2: Fine-Tune Last 2 Layers
- Better contextual understanding
- Improved performance
- Higher training time

---

# 📈 Evaluation Metrics

The model was evaluated using:
- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

Classification reports were also generated for detailed analysis.

---

# 📊 Key Insights

- Fine-tuning the last two BERT layers improved performance.
- BERT captured contextual meaning better than traditional ML models.
- Transformer-based embeddings significantly improved text understanding.
- Fine-tuning achieved better accuracy than frozen layers.

---

# ▶️ How to Run the Project

## Step 1: Install Required Libraries

```bash
pip install transformers
pip install datasets
pip install torch
pip install scikit-learn
pip install pandas
pip install matplotlib
```

---

## Step 2: Open Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
BERT_Fine_Tuning.ipynb
```

Run all cells sequentially.

---

# 📂 Project Structure

```text
NLP-Task-Innomatics
└── NLP-Task-4
    ├── BERT_Fine_Tuning.ipynb
    └── README.md
```

---

# ⚠️ Important Note

Large model files, cache files, and datasets were excluded from GitHub to avoid storage issues.

Files ignored:
- hf_cache/
- model weights
- checkpoints
- .safetensors files

---

# 🎯 Learning Outcomes

After completing this project, you will understand:
- How BERT works for NLP tasks
- Tokenization using transformers
- Fine-tuning transformer models
- Evaluation of NLP classification systems
- Experimental comparison in deep learning models

---
# 📜 License

This project is created for academic and educational purposes.
