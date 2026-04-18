# digital-nationalism-cwg
Test for research paper
/data
/scripts
/results
/notebooks
README.md
requirements.txt
import tweepy

client = tweepy.Client(bearer_token="YOUR_TOKEN")

query = "#CWG OR #CommonwealthGames OR #TeamIndia lang:en"

tweets = client.search_recent_tweets(query=query, max_results=100)

for tweet in tweets.data:
    print(tweet.text)
