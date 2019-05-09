# RateMe Project
Jesse Fredrickson

## Motivation
The purpose of this project is to scrape and analyze posts and comments from the reddit.com/r/rateme subreddit, with the end goal of training a neural network on the faces paired with their crowdsourced ratings. The idea is to develop a model which can recognize attractiveness in humans, and rate faces on its own. This could be turned into a phone or web app in future development.

## Files
**Scrape.ipynb:** this is the main python file I use to scrape and analyze the data. 

**raw_scrape.csv:** this is the raw output of the scraping operation, containing each post id, date created, image url, title, and a list of top level comment bodies.

## Results / Instructions
In this project I utilize praw along with the pushshift api to query reddit for post and comment data, which I store as a json object, import to pandas, and clean with the numpy, regex, and statistics packages. As a test I gathered ~1200 data points and did some quick analysis on them after parsing ratings. Unfortunately, I found that the distribution was poor, with a massive percentage of posters getting rated a 7/10 with a small standard deviation. Without data at the high and low ends of the scale, I will be unable to train a neural net on this dataset, and have shelved the project... for now.