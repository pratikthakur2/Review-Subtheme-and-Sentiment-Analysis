Subtheme Sentiment Analysis
This repository contains a project for performing subtheme sentiment analysis on a dataset of customer reviews. The objective is to identify subthemes within the reviews and determine their respective sentiments.

Table of Contents:
Requirements
Dataset Format
Approach
Usage
Output
License
Requirements
To run this project, ensure you have the following Python packages installed:

pandas
spacy
vaderSentiment

Dataset Format
The input dataset should be a CSV file where each review is spread across multiple cells in a row.

Approach:
Load the Dataset: Import the CSV file into a Pandas DataFrame.
Combine Review Parts: Concatenate multiple cells containing parts of the same review into a single cell for each review.
Preprocess Text Data: Clean and preprocess the text data by converting it to lowercase, removing punctuation, tokenizing, removing stop words, and lemmatizing.
Define Possible Subthemes: Create a list of possible subthemes (e.g., "tyre", "garage", "service", "booking", etc.).
Extract Subthemes: Identify subthemes present in the processed text using spaCy's lemmatization.
Perform Sentiment Analysis: Analyze the sentiment of each review using the VADER sentiment analysis tool and classify the sentiment as "positive", "negative", or "neutral".
Generate Results: For each review, associate identified subthemes with their respective sentiments and store the results in a new DataFrame.
Save Results: Export the results to a new CSV file.

Output
The output will be a CSV file (subtheme_sentiments.csv) containing the following columns:
review_id: Unique identifier for each review
review: The combined review text
subtheme: The identified subtheme
sentiment: The sentiment associated with the subtheme

