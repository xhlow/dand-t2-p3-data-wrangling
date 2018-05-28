# Data Wrangling Project: WeRateDogs Twitter Page

## Project Overview

This project is created for Project 3 (Term 2) of Udacity's Data Analyst
Nanodegree (DAND). In this project, I gathered three data sets about the
[WeRateDogs Twitter page](https://twitter.com/dog_rates), assessed them for
tidiness and quality issues, and cleaned them accordingly. After that, I
conducted some analysis on the cleaned data and reported about the analysis.

## Datasets

- `twitter-archive-enhanced.csv`: Contains basic tweet data (tweet
ID, timestamp, text etc.), provided by the WeRateDogs Twitter page. This
dataset was downloaded manually.
- `image_predictions.tsv`: Contains predictions of the dog's breed in each
tweet according to a neural network. This dataset is hosted on Udacity's
servers and was downloaded programmatically using the
[Requests](http://docs.python-requests.org/en/master/) library.
- `fav_ret_count.csv`: Contains the favorite and retweet counts of each tweet.
The data is available in Twitter's API. Using the tweet IDs in
`twitter-archive-enhanced.csv`, I queried Twitter's API to obtain each
tweet's JSON data using the [Tweepy](http://www.tweepy.org/) library and stored
the data in the text file named `tweet_json.txt`. Afterwards, I read the text
file to obtain each tweet's favorite and retweet counts and saved it into this
csv file.
- `twitter_archive_master.csv`: The clean dataset that was created by combining
and cleaning the above three datasets. This dataset is not completely cleaned
as doing so will require substantial time, but it is sufficiently cleaned for
the purpose of this analysis.
- `query_errors.csv`: This file was generated when querying Twitter's API to
record the IDs of tweets which the API queries were unsuccessful. Not used in
the analysis.

## Other Files

- `wrangle_act.ipynb`: Jupyter notebook that contains details and codes for the
data wrangling and analysis process.
- `wrangle_report.pdf`: A report that summarizes the wrangling process.
- `act_report.pdf`: A report that summarizes the findings of the analysis.

## Future Scope

As mentioned in the Datasets section, the dataset was not completely cleaned.
Therefore, future work will involve further cleaning of the dataset. In
addition, I will also conduct more analysis on the dataset.

## Libraries Used in the Project

- numpy 1.13.3
- pandas 0.22.0
- matplotlib 2.1.0
- seaborn 0.8.0
- requests 2.18.4
- tweepy 3.5.0
