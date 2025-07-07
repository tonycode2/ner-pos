# Project: POS and NER Analysis on News Articles

## Description

This project implements a natural language processing (NLP) pipeline focused on Part-of-Speech (POS) tagging and Named Entity Recognition (NER) using a news dataset (`true_news.csv`). The goal is to extract grammatical and semantic insights from news headlines and articles to better understand their structure and mentioned entities.

## Key Features

- **Data Loading**: Read the news dataset with **pandas**.
- **Text Normalization**:
  - Lowercasing all text.
  - Removing English stopwords using NLTK.
  - Cleaning punctuation and special characters via regular expressions (`re`).
- **Tokenization**:
  - Raw tokens (`tokens_raw`) from the original text.
  - Clean tokens (`tokens_clean`) after stopword and punctuation removal.
- **Lemmatization**:
  - Reducing tokens to their base form using NLTK’s `WordNetLemmatizer`.
- **POS Tagging**:
  - Tagging raw tokens with **spaCy** (`en_core_web_sm`).
  - Creating a DataFrame of each token and its POS tag.
  - Calculating frequency distributions of POS tags and filtering by categories (nouns, verbs, etc.).
- **Named Entity Recognition (NER)**:
  - Extracting entities (PERSON, ORG, GPE, DATE, etc.) with **spaCy**.
  - Aggregating entity counts into a DataFrame.
  - Filtering and analyzing entities by type.

## Basic Concepts Covered

1. **Tokenization**: Splitting text into individual tokens or words.
2. **Stopwords**: Removing common words with little semantic value.
3. **Regular Expressions**: Pattern matching for cleaning text.
4. **Lemmatization**: Converting words to their canonical base forms.
5. **POS Tagging**: Assigning grammatical categories (noun, verb, adjective) to tokens.
6. **Named Entity Recognition (NER)**: Identifying and classifying named entities in text.

## Technologies Used

- **Python 3.10+**
- **pandas**
- **NLTK** (tokenization, stopwords removal, lemmatization)
- **spaCy** (`en_core_web_sm` for POS and NER)
- **re** (regular expressions)
- **Jupyter Notebook**

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/your_repository.git
   cd your_repository
   ```
2. Set up a virtual environment and install dependencies:
   ```bash
   python -m venv venv
   # macOS/Linux
   source venv/bin/activate
   # Windows
   venv\Scripts\activate
   pip install -r requirements.txt
   ```
3. Place the `true_news.csv` dataset in the project root.

## Usage

1. Launch the Jupyter Notebook (`news_nlp.ipynb`):
   ```bash
   jupyter notebook news_nlp.ipynb
   ```
2. Execute all cells to perform POS tagging and NER, and to view frequency analyses.

## Project Structure

```
├── news_nlp.ipynb     # Notebook demonstrating the POS & NER pipeline
├── true_news.csv      # Dataset of news articles and headlines
├── requirements.txt   # Python dependencies
└── README.md          # Project documentation (this file)
```
