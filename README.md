
# Tweet Sentiment Analysis with PySpark

This project performs sentiment analysis on tweets using PySpark. It loads a dataset of tweets and uses Natural Language Processing (NLP) techniques to classify the sentiment of each tweet as positive, negative, or neutral.


## Table of Contents

 - [Project Overview](https://github.com/Roodzz/pyspark_tweet_sentiment)
- [Features](https://github.com/Roodzz/pyspark_tweet_sentiment)
- [Requirements](https://github.com/Roodzz/pyspark_tweet_sentiment)
- [Installation](https://github.com/Roodzz/pyspark_tweet_sentiment)
- [Usage](https://github.com/Roodzz/pyspark_tweet_sentiment)
- [Dataset](https://github.com/Roodzz/pyspark_tweet_sentiment)
- [License](https://github.com/Roodzz/pyspark_tweet_sentiment)



## Project Overview

The goal of this project is to demonstrate how to use PySpark for large-scale data processing and sentiment analysis. This analysis is based on a dataset of tweets where the sentiment has already been labeled. We use PySpark's MLlib for text processing and classification tasks.


## Features

- Load and process large datasets using PySpark.
- Text cleaning and preprocessing using PySpark functions.
- Sentiment classification (positive, neutral, negative).
- Ability to handle large-scale data for big data scenarios.

## Requirements

`Python 3.10`

`PySpark`

`Java 8 or 11 (required for Spark)`

`Numpy and Pandas (for additional data processing)`



## Installation

Install Python 3.10:

Download and install Python 3.10 from [here](https://www.python.org/downloads/).

#### Create a virtual environment:
```bash
  python3.10 -m venv venv
```

#### Activate the virtual environment:
```bash
  venv\Scripts\activate
```
#### Install the required libraries:
```bash
  pip install pyspark numpy pandas
```
## Usage

#### Start the Spark session: In the Python script, we initialize the Spark session:

```python
from pyspark.sql import SparkSession

spark = SparkSession.builder.appName("TweetSentiment").getOrCreate()
```
#### Load the tweet dataset: Replace the dataset path with your local dataset path:
```python
tweets_df = spark.read.csv('path/to/twitter_training.csv', header=True, inferSchema=True)
```
#### Run the sentiment analysis: The script will clean the tweet text, convert it into features, and classify the sentiment using machine learning models (e.g., Naive Bayes or Logistic Regression).

#### Stop the Spark session: Make sure to stop the session when done:
```python
spark.stop()

```


## Dataset

#### The dataset used for this project is a CSV file containing labeled tweets. Each tweet has an associated sentiment label (positive, negative, or neutral). The dataset should have the following format:

| Tweet   | Sentiment       | test                          |
| :---------- | :--------- | :---------------------------------- |
| `I love PySpark!` | `Positive` | OK |
| `I hate traffic` | `Negative` | OK |
| `It's an okay day` | `Neutral` | OK |

You can use any tweet dataset with similar structure.


## 🚀 About me

I am a full-stack developer and data engineer with experience in technologies like Java Spring, React, and cloud solutions. I have a passion for working with large-scale data and building automations for complex data workflows. With a strong background in backend development and robust data pipelines, I am always looking for new ways to apply technologies like PySpark to solve real-world problems in data analysis. This project demonstrates how I explore the power of Big Data for large-scale sentiment analysis.

Feel free to reach out if you're interested in learning more about my work or collaborating on future projects!
