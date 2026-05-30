# Text Mining for AI 
Group 59 

## Project Structure

```
TextMining/
├── final_assignment.ipynb   ← MAIN NOTEBOOK (submit this)
├── analysis_original.py     ← original spaCy + LDA script (reference)
├── draft_reference.ipynb    ← original draft (reference)
├── NER-test.tsv             ← ⚠ place here (download from Canvas)
├── Sentiment-topic-test.tsv ← ⚠ place here (download from Canvas)
└── README.md
```

## Setup

```bash
pip install spacy transformers[torch] vaderSentiment pandas scikit-learn matplotlib
python -m spacy download en_core_web_trf   # GPU recommended
python -m spacy download en_core_web_sm    # CPU fallback
```

## Tasks Covered

| Task | System | File |
|------|--------|------|
| NERC (comparison) | spaCy `en_core_web_trf` + BERT `dslim/bert-base-NER` | NER-test.tsv |
| Sentiment analysis | VADER | Sentiment-topic-test.tsv |
| Topic classification | Zero-shot `facebook/bart-large-mnli` (labels: movies, restaurants, books) | Sentiment-topic-test.tsv |

## Running

1. Drop `NER-test.tsv` and `Sentiment-topic-test.tsv` in this folder
2. Open `final_assignment.ipynb` in Jupyter
3. Run all cells top to bottom

> **Note on en_core_web_trf:** the transformer model is slow on CPU (~1 min for small sets).  
> Colab with GPU is recommended. The notebook auto-falls back to `en_core_web_sm` if trf is not installed.
# TextMiningG59
