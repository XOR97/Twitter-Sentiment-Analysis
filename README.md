# Social Sentiment Application using Dash
Real-time-streaming sentiment analysis application created with Python and Dash

## Contents:
- `dash.py` - This is currently the main front-end application code. Contains the dash application layouts, logic for graphs, interfaces with the database...etc. This code is setup to run on a flask instance. If you want to clone this and run it locally, you will be using the `dev_server.py`
- `dev_server.py` - If you wish to run this application locally, on the dev server, run via this instead.
- `twitter_stream.py` - This should run in the background of your application. This is what streams tweets from Twitter, storing them into the sqlite database, which is what the `dash.py` file interfaces with.
- `config.py` - Meant for many configurations, but right now it just contains stop words. Words we don't intend to ever count in the "trending"
- `cache.py` -  For caching purposes in effort to get things to run faster.
- `db-truncate.py` - A script to truncate the infinitely-growing sqlite database. You will get about 3.5 millionish tweets per day, depending on how fast you can process. You can keep these, but, as the database grows, search times will dramatically suffer.

## Credits

Credits for this code go to Sentdex. I've just taken inspiration from him and merely tweaked a few of the custom functions for run time performance improvements.
