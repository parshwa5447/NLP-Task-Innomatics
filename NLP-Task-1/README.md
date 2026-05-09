# NLP Preprocessing Assignment

## 📌 Project Overview

This project demonstrates an advanced Natural Language Processing (NLP) text preprocessing pipeline implemented in Python. The notebook includes conceptual explanations, preprocessing techniques, stress testing, token analytics, frequency analysis, and a complete reusable NLP pipeline.

The assignment is designed to showcase practical preprocessing skills used in real-world NLP applications such as sentiment analysis, chatbots, search engines, and text classification systems.

---

# 📂 File Structure

```bash
.
├── main.ipynb          # Complete NLP preprocessing notebook
├── README.md           # Project documentation
```

---

# 🚀 Features Implemented

## ✅ Task 1: Conceptual Understanding

The notebook explains:

* Difference between "Love" and "love" in NLP
* Importance of stopword removal
* Situations where stopword removal can be harmful
* Difference between stemming and lemmatization

---

## ✅ Task 2: Advanced Text Preprocessing Function

Implemented function:

```python
preprocess_text(text)
```

### Features Included

* Remove numbers
* Remove URLs
* Remove email patterns
* Convert text to lowercase
* Handle repeated characters
* Remove extra spaces
* Remove special characters
* Remove short tokens
* Preserve meaningful words like `no` and `not`

---

## ✅ Task 3: Stress Testing

The preprocessing function is tested on multiple noisy sentences containing:

* Emojis
* Numbers
* Slang
* Repeated characters
* URLs
* Mixed-case text
* Promotional spam text

---

## ✅ Task 4: Token Analytics

For every processed sentence, the notebook calculates:

* Total number of tokens
* Number of unique tokens
* Average token length

The notebook also includes analytical observations.

---

## ✅ Task 5: Frequency Analysis

Using Python’s `Counter` class:

```python
from collections import Counter
```

The notebook identifies:

* Top 10 most frequent words
* Top 5 least frequent words

---

## ✅ Task 6: Full NLP Pipeline

Implemented function:

```python
full_pipeline(text_list)
```

### Output Format

```python
{
    "tokens": [...],
    "clean_sentences": [...]
}
```

---

## ✅ Task 7: Error Handling

The preprocessing pipeline safely handles:

* Empty strings
* Emoji-only inputs
* Number-only inputs
* Invalid or `None` values

---

# 🛠️ Technologies Used

* Python 3
* Jupyter Notebook
* Regular Expressions (`re`)
* Collections (`Counter`)
* NumPy

---

# ▶️ How to Run the Project

## Step 1: Install Required Libraries

```bash
pip install numpy
```

## Step 2: Open Jupyter Notebook

```bash
jupyter notebook
```

## Step 3: Run the Notebook

Open:

```bash
main.ipynb
```

Run all cells sequentially.

---

# 📊 Sample Input

```python
"I absolutely looooved this product 😍😍"
```

# 📊 Sample Output

```python
Tokens: ['absolutely', 'loved', 'this', 'product']
Cleaned Sentence: absolutely loved this product
```

---

# 🎯 Learning Outcomes

After completing this project, you will understand:

* Basic NLP preprocessing techniques
* Tokenization and text cleaning
* Noise reduction in textual data
* Token analytics and frequency analysis
* Building reusable NLP preprocessing pipelines
* Error handling in NLP systems

---
