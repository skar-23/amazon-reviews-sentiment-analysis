# Amazon Product Review Sentiment Analysis

## Overview

This project analyzes Amazon Fine Food Reviews using two sentiment analysis approaches: VADER, a lexicon-based sentiment analyzer, and a pretrained RoBERTa transformer model.

The analysis uses a sample of 10,000 reviews and compares predicted sentiment with customer star ratings.

## Features

- Exploratory data analysis of customer ratings and review lengths
- VADER sentiment scoring and classification
- Pretrained RoBERTa sentiment predictions
- Comparison of sentiment distributions and model agreement
- Evaluation against rating-derived sentiment labels
- Confusion matrices and visualizations

## Technologies

Python, Pandas, NumPy, Matplotlib, Seaborn, NLTK, Hugging Face Transformers, PyTorch, and scikit-learn.

## Dataset

Download the Amazon Fine Food Reviews dataset from [Kaggle](https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews).

Place `Reviews.csv` in the `data/` directory. The dataset is not included in this repository.

The notebook selects the first 10,000 rows for analysis.

## Setup

1. Clone this repository.
2. Create and activate a Python virtual environment.
3. Install the required dependencies.
4. Download the dataset and place it at `data/Reviews.csv`.
5. Open `sentiment_analysis.ipynb` in VS Code or Jupyter and run the cells in order.

Install dependencies using:

```bash
pip install -r requirements.txt
```

The first RoBERTa run requires an internet connection to download the pretrained model.

## Evaluation Notes

The project compares VADER and RoBERTa predictions and evaluates them against labels derived from customer ratings:

- 1–2 stars: Negative
- 3 stars: Neutral
- 4–5 stars: Positive

Rating-derived labels are an approximate reference, not definitive ground-truth sentiment. The RoBERTa model was pretrained for Twitter sentiment and is applied here to product reviews.

## Future Improvements

- Test on a larger or more representative sample
- Investigate disagreements between predicted sentiment and customer ratings
- Evaluate on manually labelled product reviews
- Explore additional sentiment models and preprocessing strategies
