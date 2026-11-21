# Assignment artifact coverage matrix

| Assignment area / evidence | Handover location | Status / note |
|---|---|---|
| Dataset overview, sources, split counts and labels | `data/` | Included; tweet-text datasets not redistributed due source terms. |
| EDA: language/split distribution | `figures/eda/language_distribution_by_split.png` | Included. |
| EDA: training label proportions | `figures/eda/training_label_proportions.png` | Included. |
| EDA: raw tweet-length distributions | `figures/eda/raw_tweet_lengths.png` | Included. |
| Tokenizer length comparison | `results/metrics/tokenizer_length_summary.csv` | Included (mBERT and XLM-R). |
| Preprocessing method and replacement counts | Notebook and `results/training/experiment_summary.json` | Included. |
| XLM-RoBERTa main model and BiLSTM baseline | Notebook and `results/metrics/` | Included. |
| AfriBERTa comparison | Notebook/report discussion | Not run in supplied experiment; explicitly disclosed, no results fabricated. |
| Model training history | `results/training/lstm_training_history.csv` | Included. Transformer run summary/config is in `experiment_summary.json`. |
| Test metrics: accuracy, macro precision/recall/F1 and ROC-AUC | `results/metrics/` | Included, per-language and combined where supplied. |
| Confusion matrices | `figures/evaluation/confusion_matrices/` | Included for XLM-R and BiLSTM. |
| ROC curves | `figures/evaluation/roc_curves/` | Included for XLM-R and BiLSTM. |
| Sample prediction evidence | `results/predictions/xlmr_test_predictions_text_redacted.csv` and report table | Included with tweet text withheld. |
| Attention visualisation | `figures/interpretability/xlmr_attention_heatmap.png` | Included. |
| Ablation metrics and figure | `results/metrics/ablation_results.csv`, `figures/ablation/` | Included. |
| Cross-lingual transfer metrics, confusion matrices and ROC curves | `results/metrics/crosslingual_sw_train_metrics.csv`, `figures/cross_lingual/` | Included. |
| Discussion of robustness, generalisation and limitations | `reports/` and `docs/` | Included; includes source/domain shift, validation overlap and language-specific limitations. |
| Executable end-to-end notebook | `notebooks/Group3_Sentiment_Analysis.ipynb` and Colab link in root README | Included. Saved notebook cell outputs were cleared in the public copy; standalone evidence is retained in figures/ and results/. |
| Short assignment report | `reports/Group3_Sentiment_Analysis_Report.docx` | Included; source tweet text redacted in example table for dataset-term compliance. |

## Explicit scope notes

- AfriBERTa was not run in the supplied experiment. The executed transformer was XLM-RoBERTa; the baseline was BiLSTM.
- The notebook contains executable ablation and cross-lingual sections. The report's numeric results are based on the supplied output archive.
- The fine-tuned model checkpoint weights were not present in the supplied archives, so no checkpoint files are claimed as included.
- The source datasets are not mirrored in this public repository.
