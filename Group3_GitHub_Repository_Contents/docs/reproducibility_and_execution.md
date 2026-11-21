# Reproducibility and execution

## Canonical notebook

Open the maintained Google Colab notebook: https://colab.research.google.com/drive/1GIpm0MRkKNwvzjOPV8fJvUNjoiQHNFib

Run the notebook from top to bottom. A Colab GPU is recommended for transformer fine-tuning. Download the source datasets directly from their official providers; do not use third-party copies that bypass their terms. Configure the output directory in the notebook to a persistent Google Drive folder.

## Environment

The notebook's setup cell installs the Colab-compatible dependencies. The recorded environment included Python 3.13.16, pandas 2.2.3, NumPy 2.4.6 and datasets 5.2.0 for the acquisition stage. Modelling dependencies used Transformers 5.x, tokenizers 0.23.x, accelerate, PyTorch, emoji, scikit-learn, sentencepiece, matplotlib and seaborn. Use the notebook's install cell as the authoritative dependency specification because it includes compatible version ranges.

## Main model settings

- Model: `xlm-roberta-base`; three-class weighted loss.
- Balanced training/validation: 5,430/1,359 examples.
- Batch size 8; learning rate 2e-5; max length 128.
- Up to 5 epochs; early-stopping patience 2; gradient accumulation 2; clipping norm 1.0.
- BiLSTM baseline: 27,898-token vocabulary, 128-dimensional embeddings, 96 units per direction, dropout 0.3, AdamW at 0.001, clipping norm 1.0.

The run summary, metrics, prediction export and figures supplied with the assignment are preserved in `results/` and `figures/`. The final notebook is kept as an editable `.ipynb`; saved cell outputs have been cleared from the public copy; figures and metrics are retained separately.
