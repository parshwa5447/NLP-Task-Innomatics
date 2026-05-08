# Fine-Tuning BERT for POS Tagging and Chunking

## Overview

This project demonstrates how to fine-tune a BERT-based transformer model for two important Natural Language Processing (NLP) tasks:

* Part-of-Speech (POS) Tagging
* Chunking (Phrase Detection)

The implementation uses the CoNLL-2003 dataset and Hugging Face Transformers to perform token classification. The notebook covers dataset loading, preprocessing, tokenization, model training, evaluation, and prediction.

---

# Objectives

The main objectives of this project are:

* Understand token classification using transformers
* Learn how BERT processes sequential text data
* Perform POS tagging using contextual embeddings
* Implement chunking for phrase detection
* Train and evaluate transformer models using Hugging Face

---

# Technologies Used

| Technology       | Purpose                           |
| ---------------- | --------------------------------- |
| Python           | Programming Language              |
| Transformers     | Pretrained BERT model             |
| Datasets         | Dataset loading and preprocessing |
| PyTorch          | Deep learning backend             |
| SeqEval          | Evaluation metrics                |
| Evaluate         | Model evaluation                  |
| Jupyter Notebook | Development environment           |

---

# Dataset

The project uses the CoNLL-2003 dataset.

The dataset contains:

* Tokens (words)
* POS tags
* Chunk tags
* Named Entity tags

Example:

| Token   | POS Tag | Chunk Tag |
| ------- | ------- | --------- |
| EU      | NNP     | B-NP      |
| rejects | VBZ     | B-VP      |
| German  | JJ      | B-NP      |
| call    | NN      | I-NP      |

---

# Project Workflow

## 1. Install Required Libraries

The notebook first installs compatible versions of required libraries:

```python
!pip install transformers==4.40.2 datasets==2.18.0 huggingface_hub==0.22.2 torch seqeval evaluate
```

---

## 2. Load Dataset

The CoNLL-2003 dataset is loaded using Hugging Face Datasets.

```python
from datasets import load_dataset

dataset = load_dataset("eriktks/conll2003")
```

---

## 3. Data Exploration

The dataset structure is explored by viewing:

* Tokens
* POS Tags
* Chunk Tags

Example:

```python
example = dataset['train'][0]
print(example['tokens'])
```

---

## 4. Tokenization

The BERT tokenizer converts words into subword tokens.

```python
from transformers import AutoTokenizer

tokenizer = AutoTokenizer.from_pretrained("bert-base-uncased")
```

---

## 5. Label Alignment

Since BERT splits words into subwords, labels must be aligned properly.

Example:

| Original Word | Tokenized Form |
| ------------- | -------------- |
| playing       | play, ##ing    |

The correct POS and chunk labels are assigned to corresponding subword tokens.

---

## 6. Model Selection

The project uses:

```python
bert-base-uncased
```

for token classification.

---

## 7. Training

The Trainer API is used for training.

Training includes:

* Forward propagation
* Backpropagation
* Loss calculation
* Optimization

---

## 8. Evaluation

Evaluation metrics include:

* Accuracy
* Precision
* Recall
* F1 Score

The SeqEval library is used for token classification evaluation.

---

## 9. Prediction

The trained model predicts POS and chunk tags for unseen sentences.

---

# Model Architecture

The architecture used in this project:

```text
Input Sentence
       ↓
BERT Tokenizer
       ↓
BERT Encoder
       ↓
Token Classification Layer
       ↓
POS / Chunk Predictions
```

---

# Features

* Fine-tuning BERT for token classification
* POS tagging implementation
* Chunking implementation
* Hugging Face Trainer API integration
* Evaluation using SeqEval
* Compatible with Jupyter Notebook and VS Code

---

# How to Run the Project

## Step 1: Clone Repository

```bash
git clone <repository-url>
```

---

## Step 2: Create Virtual Environment

```bash
python -m venv NLPenv
```

Activate environment:

### Windows

```bash
NLPenv\Scripts\activate
```

### Linux/Mac

```bash
source NLPenv/bin/activate
```

---

## Step 3: Install Dependencies

```bash
pip install transformers==4.40.2 datasets==2.18.0 huggingface_hub==0.22.2 torch seqeval evaluate
```

---

## Step 4: Run Notebook

Open:

```text
Fine_Tuning_BERT_POS_Chunking.ipynb
```

Run all cells sequentially.

---

# Expected Output

The model will:

* Load the dataset successfully
* Train on token classification tasks
* Predict POS tags
* Predict chunk tags
* Display evaluation metrics

---

# Challenges Faced

During implementation, a compatibility issue occurred with newer versions of the Hugging Face datasets library.

Error:

```text
RuntimeError: Dataset scripts are no longer supported
```

Solution:

Compatible package versions were installed:

```text
transformers==4.40.2
datasets==2.18.0
huggingface_hub==0.22.2
```

---

# Learning Outcomes

After completing this project, the following concepts were understood:

* Transformer-based NLP
* Token Classification
* BERT Fine-Tuning
* POS Tagging
* Chunking
* Hugging Face Ecosystem
* Sequence Labeling
* NLP preprocessing techniques

---

# Future Improvements

Possible future enhancements:

* Add Named Entity Recognition (NER)
* Use DistilBERT for faster training
* Deploy model using Streamlit
* Add custom dataset support
* Hyperparameter tuning
* Model comparison with BiLSTM

---

# Conclusion

This project provides practical experience in transformer-based NLP using BERT for token classification tasks. It demonstrates how pretrained language models can effectively perform POS tagging and chunking with high contextual understanding.

The implementation also helps in understanding the Hugging Face workflow for modern NLP development.

---
