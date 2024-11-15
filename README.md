Hate Speech Detection: Preprocessing Tweets

Overview

This project processes a dataset of tweets to clean, analyze, and visualize the text data using Python's Natural Language Toolkit (NLTK) and other libraries. The preprocessing includes tokenization, removing stopwords, stemming, lemmatization, and generating word clouds for insights into the text content.

Dataset

The dataset is a CSV file containing tweets and metadata. The preprocessing focuses on the text content of the tweets.

Key Features

Data Cleaning and Tokenization

Tokenize tweets while removing punctuation.

Stopword Removal

Filter out common stopwords to retain meaningful words.

Stemming and Lemmatization

Perform stemming and lemmatization for word standardization.

Word Cloud Visualization

Generate word clouds to visualize text data before and after preprocessing.

POS Tagging and Named Entity Recognition

Part-of-Speech (POS) tagging and Named Entity Recognition (NER) for linguistic insights.

Libraries Used

pandas: For data manipulation.
nltk: For natural language processing tasks.
string: To handle text data and punctuation.
wordcloud: To generate word clouds.
matplotlib: For data visualization.
Setup Instructions
Install Required Libraries

bash

Copy code
pip install pandas nltk wordcloud matplotlib
Download NLTK Data The following datasets need to be downloaded:

python
Copy code
import nltk
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('averaged_perceptron_tagger')
nltk.download('wordnet')
nltk.download('maxent_ne_chunker')
nltk.download('words')
Load the Dataset Ensure your dataset (e.g., HatespeechKenya.csv) is accessible in your project directory.

Usage

Load the dataset using pandas:

python
Copy code
df = pd.read_csv("/content/HatespeechKenya.csv", sep=";", header=None, on_bad_lines='skip')
Follow the preprocessing steps in the script to clean and analyze the text.

Generate word clouds for visual insights:

python
Copy code
generate_wordcloud(all_tokens_before)  # Before preprocessing
generate_wordcloud(all_tokens_after)   # After preprocessing
Analyze POS tags and named entities:

python
Copy code
pos_tags = tokens_after_lemmatization.apply(pos_tagging)
Troubleshooting
If you encounter the error:

plaintext
Copy code
LookupError: Resource maxent_ne_chunker_tab not found
Download the missing resource:

python
Copy code
nltk.download('maxent_ne_chunker_tab')

Output

Tokenized, clean text data.
Word clouds to visualize frequent terms.
POS tags and named entities for linguistic analysis.
