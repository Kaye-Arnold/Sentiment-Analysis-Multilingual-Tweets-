# Dataset provenance and access

The experiment used 72,390 labelled records across three languages. Amharic (9,480) and Swahili (3,011) came from AfriSenti; English (59,899) came from the TweetEval `sentiment` configuration. The split counts and canonical label mapping are recorded in this folder.

## Source repositories

- AfriSenti SemEval 2023: https://github.com/afrisenti-semeval/afrisent-semeval-2023
- AfriSenti terms: https://afrisenti-semeval.github.io/Terms/
- TweetEval: https://github.com/cardiffnlp/tweeteval
- Hugging Face dataset/config: https://huggingface.co/datasets/cardiffnlp/tweet_eval (configuration: `sentiment`)

## Why source CSVs are not included

The AfriSenti organiser terms state that the datasets are for scientific/research use and must not be redistributed or shared in part or full with third parties. TweetEval also directs users to check individual task licences and Twitter terms. For that reason this public repository deliberately does **not** contain original tweet-text CSVs, preprocessed tweet-text CSVs, raw train/validation/test splits, or prediction text excerpts. Obtain the data from the upstream providers and comply with their terms.

The original data packages supplied for this analysis included source-specific train/validation/test CSVs and a combined preprocessed file; they were reviewed locally but excluded from this public handover for the above reason. A redacted row-level prediction table is provided under `results/predictions/`, retaining language, true label, predicted label and confidence without tweet text.

## Dataset sizes

See [`split_summary.csv`](split_summary.csv). The balanced modelling subset used 1,810 training records and 453 validation records per language (5,430 train; 1,359 validation); the original test sets were retained (15,031 total).
