# Key Distinction of Narratives

This repository contains notebook-based NLP-pipeline for Identifying Key Distinctions in Literary Narratives (German) Using static Word Embeddings.

## Repository Structure

```
Key-Distinction-of-Narratives-main/
├── Code/
│   ├── 1_scatter_Plot.ipynb
│   ├── 2_Violin_plot.ipynb
│   ├── 3_Training_FastText.ipynb
│   ├── 4_Training_spaCy.ipynb
│   └── 5_Adj_syn_Nouns_(AVG)_Viz.ipynb
├── Data/
├── Result/
├── README.md
└── requirements.txt
```

## Setup

### 1) Clone the repository

```bash
git clone <your-repo-url>
cd Key-Distinction-of-Narratives-main
```

### 2) Create and activate a virtual environment

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3) Install dependencies

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 4) Download required NLP resources

The notebooks use German spaCy models, NLTK stopwords, and a FastText German model.

Download the FastText word embedding model (German) following this link: https://fasttext.cc/docs/en/crawl-vectors.html

```bash
python -m spacy download de_core_news_md
python -m spacy download de_core_news_lg
python -c "import nltk; nltk.download('stopwords')"
python -c "import fasttext.util; fasttext.util.download_model('de', if_exists='ignore')"
```

The FastText command downloads the German vectors file (for example, `cc.de.300.bin`) to your current working directory.

## Data and Outputs

- Put input data files in `Data/` (the notebooks reference Excel-based inputs in places).
- Save generated outputs/figures/tables in `Result/`.

## Reproducibility Notes

- Run notebooks in numeric order to preserve the intended pipeline flow.
- If using Jupyter Lab:

```bash
jupyter lab
```
