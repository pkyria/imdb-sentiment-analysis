# Sentiment Analysis

For this project, we will be analyzing an [IMDB Review Dataset](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews), found on Kaggle.

The steps taken will be briefly described below:

## Importing Libraries

First, we import the necessary libraries required for our analysis. Libraries like sklearn, pandas, nltk, matplot, seaborn and wordcloud are among the many used for this assignment.

## The IMDB dataset
This simple dataset consists of two attributes:
- ### Review attribute
  Contains a user submitted review of a random movie
- ### Sentiment
  Characterizes the review as ‘positive’ or ‘negative’.

## Data Cleaning
This dataset has low dimensionality and contains 50,000 entries, making it an ideal dataset for testing Machine Learning techniques, such as Sentiment Analysis.
There are no empty rows to remove. For better processing of the data, we have assigned numbered labels to each review value: 1 is assigned to “positive” and 0 is assigned to “negative”.

## Data Visualization
Visualizing data aids in understanding the distribution of our problem and the underlying structure of our dataset. It will enhance the process of analysis.

Data Preprocessing
A very crucial part of sentiment analysis. The text that will be used for our sentiment models must be preprocessed and converted into a proper form, devoid of any noise and transformed into a form readable to the machine.
The steps taken are as follows:

- ### Unicode to ascii
  Converting any Unicode characters to ascii for machine readability.
- ### Contractions handling
  Contractions are words or combinations of words that are shortened by dropping letters and replacing them by an apostrophe, such as "you are" -> "you're" .
- ### Removing HTML tags
- ### Removing noise such as br tags.
- ### Converting text to lowercase
- ### Removing URLs and Special Characters
- ### Deleting Numbers
- ### Punctuation Handling
- ### Removing Stopwords
  Stopwords are frequent words that contain little to no meaning for a sentence. They can be removed.
- ### Lemmatization-stemming
  This is the process of converting any word into their root form, simplifying text analysis.

## Sentiment Analysis with TextBlob
TextBlob is a Python library for processing textual data. It provides a simple API for diving into common natural language processing (NLP) tasks such as part-of-speech tagging, noun phrase extraction, sentiment analysis, classification, and more.
By extracting the polarity score for each separate review, we assign a label to each one:

- Positive if polarity >0
- Negative if polarity < 0
- Neutral if polarity = 0

## Vader Sentiment Analysis
Polarity scores give a dictionary containing pos, neg and neu values, as well as compound scores. The compound scores will be used similarly to the previous analysis.
By extracting the compound score for each separate review, we assign a label to each one:

- Positive if score >= 0.05
- Negative if score < 0.05
- Neutral if score = 0
