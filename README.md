# Project: NLP on Wine Reviews

## Description

This project implements a natural language processing (NLP) pipeline on a dataset of wine reviews (`winemag-data-130k-v2.csv`). The goal is to clean, tokenize, and analyze word frequency (unigrams and bigrams) to extract insights into the language used in the descriptions.

## Features

- Initial data loading and exploration with **pandas**.
- Removal of English **stopwords**.
- **Punctuation cleaning** using regular expressions (`re`).
- **Text tokenization** with **NLTK** (`word_tokenize`).
- **Stemming** using NLTK’s `PorterStemmer`.
- **Lemmatization** using NLTK’s `WordNetLemmatizer`.
- Flattening token lists to create a unified corpus.
- Calculation of **unigram** and **bigram** frequencies with `nltk.ngrams` and `pandas.Series.value_counts()`.

## Technologies

- **Python 3.10+**
- **pandas**
- **NLTK** (tokenization, stopwords, stemming, lemmatization)
- **re** (regular expressions)
- **Jupyter Notebook**

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/your_repository.git
   cd your_repository
   ```
2. Create a virtual environment and install dependencies:
   ```bash
   python -m venv venv
   # On macOS/Linux
   source venv/bin/activate
   # On Windows
   venv\Scripts\activate
   pip install -r requirements.txt
   ```
3. Download the dataset `winemag-data-130k-v2.csv` and place it in the project root.

## Usage

1. Open the Jupyter Notebook (`wine.ipynb`):
   ```bash
   jupyter notebook wine.ipynb
   ```
2. Run all cells to process the data and generate n-gram statistics.

## Project Structure

```
├── wine.ipynb                 # Jupyter Notebook with the NLP pipeline
├── winemag-data-130k-v2.csv   # Dataset of wine reviews
├── requirements.txt           # Project dependencies
└── README.md                  # Project documentation (this file)
```

## License

This project is licensed under the MIT License. Feel free to use and adapt it.

