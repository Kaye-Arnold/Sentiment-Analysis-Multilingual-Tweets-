# Group 3 — Multilingual Tweet Sentiment Analysis

**Course:** CSC 63106: Artificial Intelligence  
**Institution:** Uganda Martyrs University  
**Group members:** SSENDIWALA ARNOLD (2024-B291-13533), JJEMBA RONALD (2024-B291-12210), NAKABUGO MARGRET (2024-B291-11431)

## Start here

- **Google Colab notebook:** https://colab.research.google.com/drive/1GIpm0MRkKNwvzjOPV8fJvUNjoiQHNFib
- **Local notebook copy:** [`notebooks/Group3_Sentiment_Analysis.ipynb`](notebooks/Group3_Sentiment_Analysis.ipynb)
- **Short report:** [`reports/Group3_Sentiment_Analysis_Report.docx`](reports/Group3_Sentiment_Analysis_Report.docx)
- **Assignment artifact map:** [`docs/assignment_artifact_matrix.md`](docs/assignment_artifact_matrix.md)
- **Reproducibility guide:** [`docs/reproducibility_and_execution.md`](docs/reproducibility_and_execution.md)
- **Dataset provenance and terms:** [`data/README.md`](data/README.md)

## Project summary

This work evaluates three-class sentiment classification (negative, neutral, positive) across Amharic, Swahili and English tweets. Amharic and Swahili come from AfriSenti; English comes from TweetEval's sentiment configuration. XLM-RoBERTa is the main transformer and a bidirectional LSTM is the baseline. The supplied handover retains EDA, token length comparisons, preprocessing evidence, language-specific and combined metrics, confusion matrices, ROC curves, attention visualisation, ablation results, cross-lingual transfer diagnostics and model run metadata.

## Repository structure

```text
.
├── README.md
├── notebooks/                 # Editable Colab/Jupyter notebook
├── reports/                   # Final short report
├── data/                      # Provenance, label mapping, split counts (no raw tweet text)
├── results/
│   ├── metrics/                # Main, baseline, ablation and transfer metrics
│   ├── predictions/            # Row-level predictions with tweet text redacted
│   └── training/               # Experiment summary and training history
├── figures/                   # EDA, evaluation, ablation, attention, transfer evidence
└── docs/                      # Assignment coverage and reproducibility notes
```

## Dataset redistribution note

Raw and preprocessed tweet-text data are intentionally not included. The AfriSenti terms prohibit redistribution of the dataset, and TweetEval directs users to comply with individual subset licences and Twitter terms. See [`data/README.md`](data/README.md) and upstream notices before obtaining or using the data.

## Important experiment disclosures

- AfriBERTa was not run; no AfriBERTa scores are claimed.
- The cross-lingual Swahili-trained model predicted neutral for all test examples, so this is a negative transfer result, not evidence of successful cross-lingual generalisation.
- Three unique Swahili text records crossed the train/validation boundary; no exact-text overlap with the test set was found.
- The combined test score is dominated by English because English contributes most test examples. Per-language results should be read alongside the aggregate.
- No fine-tuned checkpoint weights were present in the supplied files; this repository does not pretend to include model weights.
