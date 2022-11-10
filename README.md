# Get Tweets (getTweets.py)

I am interested in searching, retrieving, and analyzing tweets from Twitter on topics of interest. getTweets.py is a Python script that searches for 100 tweets per specified query item, retrieves relevant information and writes it to a newly created comma-separated values (.csv) file. config.py is used to store the Twitter application’s API and Access Token keys.

For this exercise, I am interested in retrieving tweets regarding NBA’s Toronto Raptor players to explore the sentiment regarding the team’s player on NBA Twitter.

# Tweepy

This exercise will leverage the Tweepy Python Library using the Twitter API v2 Client.

Reference: https://docs.tweepy.org/en/stable/client.html#search-tweets

# Output

This script will produce a .csv file containing all Tweets retrieved per topic of interest. Each record in the .csv file corresponds to single Tweet.

| Field  | Field Description |
| :---: | --- |
| tweet_id| This is the ID of the Tweet. |
| user_id  | This is the ID of the user that created the Tweet.  |
| username | This is the username of the user that created the Tweet. |
| tweet_text | This is the Tweet itself. |
| created_at | The date and time the Tweet was created. The script will convert this time from UTC to the time zone of the machine it was executed on. |
| location | If available, the location where the Tweet was created. |
| source | The application or client the Tweet was created at. |
| reply_count | The number of replies on the Tweet. |
| retweet_count | The number of retweets on the Tweet. |
| like_count | The number of likes on the Tweet. |
| quote_count | The number of times the Tweet was quoted. |
| hashtags | If available, the list of hashtags used in the Tweet. |
| urls | If available, the URLs included in the Tweet. |
| mentions | If available, any mentions in the Tweet. |
| referenced_tweet_type | The type of Tweet. Whether is an original Tweet, a Tweet replying to another Tweet, Retweeted or a quoted Tweet. |
| reference_reply_count | If available, the number of replies on the Tweet it is referencing. |
| reference_retweet_count | If available, the number of retweets on the Tweet it is referencing. |
| reference_like_count | If available, the number of likes on the Tweet it is referencing. |
| reference_quote_count | If available, the number of quotes on the Tweet it is referencing. |
| user_profile_url | The URL to the user’s profile that created the Tweet. |
| tweet_url | The URL to the Tweet. |
| reference_user_profile_url | The URL to the user profile that created the referenced Tweet. |
| reference_tweet_url | The URL to the referenced Tweet. |

# Limitations
There were some limitations I ran into during the creation of this project:

1)	The search recent Tweets function allows users to search tweets made within the last seven days. Thus, your search results are limited to only very recent Tweets.
2)	Only a maximum of 100 Tweets can be retrieved for search recent Tweets call. This means only 100 Tweets can be retrieved for every topic of interest (query). You may see quite a few of duplicate Tweets as a result of it being Retweeted.
3)	With the Twitter API v2 Client, another get Tweet call is required to retrieve the full Tweet text of reference Tweets as such Retweets. This can limit how many queries can be searched before hitting the call request cap within a 15-minute timeframe.

# Conclusions
Tweepy is a great Python library for searching and retrieving Tweets based on a query. The data retrieved can be used for simple data analysis. However, a larger sample size of Tweets would be required for a deeper analysis. This would require a higher level of developer access.
