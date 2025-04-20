# Multi-Label Emotion Recognition using BERT

This project performs multi-label emotion classification on textual data using the GoEmotions dataset and a fine-tuned BERT model. It addresses class imbalance with weighted loss and supports inference on real-world user inputs.

## • Features

- Fine-tuning `bert-base-uncased` for multi-label classification
- Preprocessing with custom cleaning functions
- Class imbalance handling with `BCEWithLogitsLoss` and `pos_weight`
- Evaluation with `micro-F1`, `macro-F1`, and Hamming Loss
- Real-time inference via command-line interface

## • Dataset

- Source: [GoEmotions Dataset by Google](by Kaggle.com)
- Format: CSV with binary columns for 28 emotion labels + `neutral`
- Unclear examples are filtered before training

## • Labels

- `admiration`, `amusement`, `anger`, `annoyance`, `approval`, `caring`, `confusion`, `curiosity`, `desire`, `disappointment`, `disapproval`, `disgust`, `embarrassment`, `excitement`, `fear`, `gratitude`, `grief`, `joy`, `love`, `nervousness`, `optimism`, `pride`, `realization`, `relief`, `remorse`, `sadness`, `surprise`, `neutral`

## • Model Details

- Base model: `bert-base-uncased`
- Max sequence length: 128
- Epochs: 50 (selectable)
- Frozen BERT encoder for stability
- Trainer class customized for weighted loss

## • Evaluation Metrics

- Micro F1 Score
- Macro F1 Score
- Hamming Loss

## • Inference

Run the script and input text to receive predicted emotions:

```bash
python main.py
```

**Example:**

``Text: I just got the job!
Predicted emotions: ['joy', 'excitement', 'pride']``

## • Installation

```bash
pip install -r requirements.txt
```

### • Requirements

- Python ≥ 3.7
- PyTorch ≥ 1.12
- transformers ≥ 4.0
- datasets
- scikit-learn
- numpy
- scipy

### • Usage
```bash
python main.py
```

#### • License<br>
This project is licensed for educational and research purposes.

