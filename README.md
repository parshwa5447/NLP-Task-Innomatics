# NLP Assignment 4: BERT Fine-Tuning (IMDb Sentiment Classification)

This task fine-tunes `bert-base-uncased` for binary sentiment classification and evaluates performance using multiple metrics.

## Files
- `BERT_Fine_Tuning.ipynb` : end-to-end notebook (preprocessing -> training -> evaluation -> experiments)
- `Dataset/` : dataset CSVs used by the notebook

## Dataset Setup
Place the dataset files here:
- `NLP-Task-4/Dataset/IMDb movies.csv`
- `NLP-Task-4/Dataset/IMDb ratings.csv`

The notebook reads them using relative paths:
- `Dataset/IMDb movies.csv`
- `Dataset/IMDb ratings.csv`

Note: These CSVs are large. It is recommended to keep them locally and not push them to GitHub (to keep the repo small).

## Environment / Install
Recommended (Windows PowerShell):

```bash
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -U transformers datasets torch accelerate scikit-learn pandas numpy matplotlib jupyter
```

## Run
From the repo root:

```bash
jupyter notebook NLP-Task-4/BERT_Fine_Tuning.ipynb
```

Run cells top-to-bottom.

## Model
- Tokenizer: `bert-base-uncased`
- Model: `AutoModelForSequenceClassification`
- Optimizer: AdamW (via HF Trainer, `learning_rate=2e-5`)

## Evaluation Metrics (Required)
The notebook prints:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- Classification report

## Experiments (Required)
The notebook runs and compares:
- Full fine-tuning (baseline)
- Freeze encoder and train classifier only
- Fine-tune last 2 encoder layers + classifier

At the end it produces a comparison table (sorted by F1).

## FAST_MODE (For Slow PCs)
If training takes too long on your computer, keep:
- `FAST_MODE = True`

This reduces:
- number of samples used
- maximum token length
- training steps

Set `FAST_MODE = False` for a final higher-quality run before submission.

## Expected Workflow
Raw Data -> Preprocessing -> Tokenization -> Model Training -> Evaluation -> Comparison

