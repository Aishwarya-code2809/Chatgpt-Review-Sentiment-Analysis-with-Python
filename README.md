# ChatGPT Review Sentiment Analysis

A Python and Google Colab project that analyzes user reviews of the ChatGPT app to understand overall sentiment, review subjectivity, star-rating patterns, and recurring feedback themes.

## Project objectives

- Measure review polarity and subjectivity.
- Classify review text as positive, neutral, or negative.
- Compare text sentiment with star ratings.
- Identify frequently mentioned words and phrases in positive and negative reviews.
- Explore review volume and sentiment over time.
- Summarize common feedback areas, such as answer quality, usefulness, usability, reliability, and app features.

## Dataset

The notebook downloads `chatgpt_reviews.csv` automatically from the public [ChatGPT_Reviews_Analysis repository](https://github.com/Ayush-k-Das/ChatGPT_Reviews_Analysis). The mentor's notebook reports 196,727 source rows with fields for review ID, review text, rating, and review date. The notebook displays the actual row count when run because the hosted data may change.

If the automatic download is unavailable, the notebook offers a Google Colab file-upload fallback. No Google Drive mount is required.

## Files

- `ChatGPT_Review_Sentiment_Analysis.ipynb` — Colab notebook with the full analysis workflow.

## Analysis workflow

1. Load and inspect the review dataset.
2. Standardize column names, remove exact duplicate rows, fill missing review text, and convert ratings and dates to appropriate types.
3. Calculate TextBlob polarity and subjectivity for non-empty reviews.
4. Group polarity scores into positive, neutral, and negative sentiment.
5. Visualize ratings, sentiment distribution, subjectivity, sentiment by rating, and monthly trends.
6. Extract frequent unigrams and bigrams from positive and negative reviews.
7. Use transparent keyword rules to explore feedback aspects and their sentiment.

## Run in Google Colab

1. Download `ChatGPT_Review_Sentiment_Analysis.ipynb` from this repository.
2. Open [Google Colab](https://colab.research.google.com/).
3. Choose **File → Upload notebook** and select the downloaded `.ipynb` file.
4. Choose **Runtime → Run all**.

The notebook installs TextBlob and fetches the dataset when run. Sentiment scoring processes all non-empty reviews and may take a few minutes.

## Tools

- Python
- pandas and NumPy
- Matplotlib and Seaborn
- TextBlob
- scikit-learn `CountVectorizer`
- Google Colab

## Interpretation notes

TextBlob is a lexicon-based method; it can miss sarcasm, context, and domain-specific meanings. Keyword-based feedback aspects are exploratory indicators rather than a trained classifier. Phrase counts show frequency, not importance, and findings should be checked against example reviews. The analysis is descriptive and does not establish why users feel a certain way.

## Data attribution

The CSV is retrieved from the public [ChatGPT_Reviews_Analysis GitHub repository](https://github.com/Ayush-k-Das/ChatGPT_Reviews_Analysis). Please review the source repository and dataset terms before redistributing the data itself.
