# Sentiment Analysis using NLP Pipeline & Machine Learning

A complete, beginner-friendly Machine Learning + NLP project that predicts sentiment from movie descriptions/reviews using **NLP preprocessing**, **feature engineering**, and **supervised classification models**. ??

## 1. Project Overview
This project builds an end-to-end sentiment analysis pipeline using Natural Language Processing (NLP) techniques and Machine Learning algorithms. The workflow includes:
- Data loading and preparation
- Text preprocessing
- Feature extraction using Bag of Words and TF-IDF
- Model training and evaluation
- Performance comparison and insights

## 2. Objective of the Project
The main objective is to classify text sentiment (for example, positive/negative) by:
- Cleaning and transforming raw text into machine-readable format
- Converting text into numerical vectors
- Training multiple ML models
- Comparing model performance using standard evaluation metrics

## 3. Dataset Information
The project uses IMDb-related datasets:
- `Dataset/IMDb movies.csv`
- `Dataset/IMDb ratings.csv`

Typical fields used in this notebook include:
- `description` (text data used for NLP)
- `avg_vote` or derived labels (used to create sentiment classes)

Note: Sentiment labels are created/derived in the notebook based on project logic.

## 4. NLP Preprocessing Steps
The text preprocessing pipeline includes:
- Lowercasing text
- Removing punctuation and special characters
- Removing numbers
- Tokenization
- Stopword removal
- (Optional) stemming/lemmatization depending on the final notebook flow

These steps reduce noise and improve model quality.

## 5. Feature Engineering Techniques
Two classical NLP feature extraction methods are used:

### Bag of Words (BoW)
- Creates a vocabulary from all words
- Represents each document based on word occurrence counts

### TF-IDF (Term Frequency–Inverse Document Frequency)
- Weighs important words higher
- Reduces the influence of very common words

Both feature sets are tested to compare impact on model performance.

## 6. Machine Learning Models Used
The following classification models are trained:

1. Logistic Regression
2. Naive Bayes
3. Decision Tree

## 7. Evaluation Metrics
Model performance is evaluated using:
- Accuracy
- Precision
- Recall
- F1 Score

These metrics provide a balanced understanding of overall and class-wise performance.

## 8. Key Insights and Model Comparison
General observations from this project workflow:
- **Logistic Regression** usually provides strong and stable baseline performance for text classification.
- **Naive Bayes** is fast and often performs competitively on sparse text features like BoW/TF-IDF.
- **Decision Tree** is interpretable but may overfit compared to linear probabilistic models.
- **TF-IDF** often improves quality over plain BoW by emphasizing informative words.

Recommendation: Use the notebook's final metric table as the source of truth for your exact best model.

## 9. Technologies and Libraries Used
- Python 3.x
- Jupyter Notebook
- pandas
- numpy
- nltk
- scikit-learn
- matplotlib (if used for visualization)

## 10. Installation Steps
Clone or download the project, then install dependencies.

```bash
# (Optional) create virtual environment
python -m venv .venv

# Activate environment (Windows PowerShell)
.venv\Scripts\Activate.ps1

# Install required libraries
pip install pandas numpy nltk scikit-learn matplotlib jupyter
```

## 11. How to Run the Notebook
```bash
# From project root
cd NLP-Task-2
jupyter notebook main.ipynb
```

Then run cells in order from top to bottom.

Important: If NLTK resources are missing, run:

```python
import nltk
nltk.download('punkt')
nltk.download('punkt_tab')
nltk.download('stopwords')
```

## 12. Project Folder Structure
```text
NLP-Task-2/
+-- Dataset/
¦   +-- IMDb movies.csv
¦   +-- IMDb ratings.csv
+-- main.ipynb
+-- README.md
```

## 13. Learning Outcomes
By completing this project, you will learn:
- How to design an NLP preprocessing pipeline
- How to apply BoW and TF-IDF feature engineering
- How to train and evaluate multiple ML classifiers
- How to compare models using Precision, Recall, and F1 Score
- How to build a practical sentiment analysis workflow for real-world text
