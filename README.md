
# Sentiment Analysis of Booking Reviews

## Project Overview

This project aims to perform sentiment analysis on customer reviews from Booking.com. Using Natural Language Processing (NLP) techniques, the sentiment of each review is classified into Positive, Neutral, or Negative. The core of the project involves fine-tuning pre-trained models to effectively categorize sentiments based on the text content of the reviews.

## Objectives

The primary goal of this project is to detect the sentiment (positive, neutral, or negative) of customer reviews using the Hugging Face transformer models, specifically Roberta-based models.

## Dataset

The dataset used consists of customer reviews extracted from Booking.com, focusing on the **"review_text"** column, which contains the textual review of each customer.

## Key Steps

### 1. Data Preprocessing

To ensure the text is properly formatted and prepared for analysis, the following preprocessing steps were applied:
- **Lowercasing**: Convert all text to lowercase.
- **HTML tag removal**: Remove any HTML tags from the reviews.
- **URL removal**: Eliminate any links from the text.
- **Punctuation removal**: Remove any special characters or punctuation.
- **Stopword handling**: Process and remove unnecessary stopwords from the text.
- **Emoji handling**: Properly handle any emojis in the review text.

### 2. Sentiment Analysis

The sentiment analysis was conducted by fine-tuning pre-trained Roberta models from Hugging Face. Two specific models were utilized:
- **`cardiffnlp/twitter-roberta-base-sentiment-latest`**:
  - Trained on Twitter data, this model predicts the following sentiments:
    - **0** -> Negative
    - **1** -> Neutral
    - **2** -> Positive
- **`siebert/sentiment-roberta-large-english`**:
  - Trained on multiple datasets, this model predicts:
    - **1** -> Positive
    - **0** -> Negative

For each review, a sentiment score was generated and added as a new column in the dataset.

### 3. Conclusion

The project provides insights into the overall customer sentiment for different aspects of Booking.com reviews, allowing better understanding of customer satisfaction and concerns.

## Requirements

To run the project, you need to install the following dependencies:
- `pandas`
- `numpy`
- `transformers`
- `torch`
- `sklearn`

## File Structure

- `Project.ipynb`: Jupyter notebook containing the code for data processing and sentiment analysis.
- `dataset/booking_reviews.csv`: Dataset containing the reviews.


