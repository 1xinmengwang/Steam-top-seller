The data we used is scraping from Steam's World Best Selling Game (SWBG) page
(https://store.steampowered.com/search/?filter=globaltopsellers&os=win), recorded on Apirl 5th, 2024. 

The features we are using are all collected from the Steam game details page:

‘Current Price $’: This field represents the normal price of each game in dollars.
As opposed to its sale price, focusing only on the regular pricing of the games.

‘Day_now’: We collect the released dates for each game and convert these dates,
which are hard to utilize in machine learning tools, into numerical data representing the
totals days since the game was released to the date we collect the data, which is April 5,
2024.

‘pct_positive_views’: This information is directly collected from Steam, and
indicates the percentage of positive views a game has received

‘num_pop_tag’: Steam shows up to 20 user-defined tags for each game, around
80% of the games in our dataset have exactly 20 tags. However, due to the highly skewed
distribution, we decided to focus on the top 10% of the most frequent tags and count their
occurrences across each game.

‘total _reviews’: this is our dependent variable. It’s commonly known among
Steam users that the total number of sales is confidential. However, to some extent the
total number of reviews can serve as a proxy for sales. Clearly, using the total number of
reviews as a substitute for actual sales data is not ideal, but it is the only feasible option
given the absence of accessible sales data.

*Noticed: both ‘pct_positive_views’ and ‘total _reviews’ are based on the past 30 days.
