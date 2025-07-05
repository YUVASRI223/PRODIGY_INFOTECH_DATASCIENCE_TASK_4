

# PRODIGY_INFOTECH_DATASCIENCE: Task-04

 **Objective:**
The goal of this task is to perform sentiment analysis on Twitter training data. We aim to preprocess raw tweet text, analyze the distribution of sentiments, and visualize prominent words associated with each sentiment category using word clouds. This task focuses on fundamental Natural Language Processing (NLP) techniques, data cleaning, and data visualization.

**Dataset Used:**
* **Source:** Custom (Twitter Training Data)
* **Dataset:** `twitter_training.csv`
* **Format:** CSV (assumed no header, columns are `GameID`, `GameName`, `Sentiment`, `TweetText`)

 **Technologies Used:**
* Python 3.7+ (specifically Anaconda environment)
* Pandas for data manipulation
* `re` (Regular Expressions) for text cleaning
* Matplotlib and Seaborn for visualizations
* WordCloud for text visualization
* Pillow (dependency for WordCloud)
* Jupyter Notebook

 **Working:**

 **Data Loading:**
* Loaded the `twitter_training.csv` dataset, explicitly specifying no header (`header=None`).
* Renamed columns for clarity: `['GameID', 'GameName', 'Sentiment', 'TweetText']`.
* Performed basic checks (`.head()`, `.unique()`, `.value_counts()`) for initial data understanding.

 **Data Preprocessing:**
* Cleaned the `TweetText` column to create a `clean_sentence` column.
* Operations included removing punctuation (`re.sub(r'[^\w\s]', '', x)`) and converting text to lowercase (`.lower()`).
* Handled potential non-string entries by converting to `str(x)`.

 **Sentiment Distribution:**
* Identified unique sentiment labels (`'Positive'`, `'Neutral'`, `'Negative'`, `'Irrelevant'`) and their frequency counts within the dataset.

 **Word Cloud Generation:**
* Iterated through each identified sentiment category.
* Filtered `clean_sentence` data for each sentiment.
* Concatenated all clean sentences for a given sentiment into a single string.
* Generated and displayed a Word Cloud for each sentiment, highlighting the most frequent words. Robust checks were included to handle empty text segments.

 **Visualizations:**

 **Sentiment Distribution Plot:**
* A count plot (bar chart) visualizing the frequency of each sentiment label (`Positive`, `Neutral`, `Negative`, `Irrelevant`) in the dataset, providing an overview of sentiment prevalence.

 **Word Clouds:**
* Individual word cloud visualizations for each sentiment category, offering a quick visual summary of the most common terms associated with 'Positive', 'Neutral', 'Negative', and 'Irrelevant' tweets.

 **Learning Outcomes:**
* Gained practical experience in handling real-world text data for sentiment analysis.
* Mastered essential text preprocessing techniques (cleaning, lowercasing).
* Understood how to identify and analyze sentiment distributions.
* Developed skills in using the `wordcloud` library for effective text visualization.
* Practiced debugging common Python and library-specific errors (`KeyError`, `ModuleNotFoundError`, `ValueError`, `AttributeError`) related to data handling and package versions.

 **Author:**
Yuva Sri
Data Science Student, VIT Vellore
Year: 2025

---
