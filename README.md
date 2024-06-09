# Subtheme Sentiment Analysis

This repository contains a project for performing subtheme sentiment analysis on a dataset of customer reviews. The objective is to identify subthemes within the reviews and determine their respective sentiments.

## Table of Contents

- [Requirements](#requirements)
- [Dataset Format](#dataset-format)
- [Approach](#approach)
- [Output](#output)
- [License](#license)

## Requirements

To run this project, ensure you have the following Python packages installed:

- pandas
- spacy
- vaderSentiment

## Dataset Format

The input dataset should be a CSV file where each review is spread across multiple cells in a row.

## Approach

1. **Load the Dataset**: Import the CSV file into a Pandas DataFrame.
2. **Combine Review Parts**: Concatenate multiple cells containing parts of the same review into a single cell for each review.
3. **Preprocess Text Data**: Clean and preprocess the text data by converting it to lowercase, removing punctuation, tokenizing, removing stop words, and lemmatizing.
4. **Define Possible Subthemes**: Create a list of possible subthemes (e.g., "tyre", "garage", "service", "booking", etc.).
5. **Extract Subthemes**: Identify subthemes present in the processed text using spaCy's lemmatization.
6. **Perform Sentiment Analysis**: Analyze the sentiment of each review using the VADER sentiment analysis tool and classify the sentiment as "positive", "negative", or "neutral".
7. **Generate Results**: For each review, associate identified subthemes with their respective sentiments and store the results in a new DataFrame.
8. **Save Results**: Export the results to a new CSV file.

## Output

The output will be a CSV file (`subtheme_sentiments.csv`) containing the following columns:

- `review_id`: Unique identifier for each review
- `review`: The combined review text
- `subtheme`: The identified subtheme
- `sentiment`: The sentiment associated with the subtheme
