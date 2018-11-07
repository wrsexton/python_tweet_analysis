# python_tweet_analysis
Analyzing tweets from republican and democrat representatives - obtained from a kaggle database.

Uses Python 3

Requires:
  - sqlite3
  - matplotlib


This project is intended to compare and contrast the words found in a database of 85,000 tweets from US congresspeople separated into two categories based on their political party - Democrat or Republican.

The first question I wanted to answer regarding the information I found was:  "How often does each party mention the other in this collection of tweets?"  I achieved this goal by parsing the text of all of the tweets from each party in search of different keywords intended to represent an occurance where the opposing party is mentioned.

I used regular expressions to search for the following character sets

*Democrat*:
  - words beginning with 'repub' (the word 'republic' is filtered out)
  - 'gop'
  - 'conservative'
  - words beginning with 'right' and ending with 'wing'
    
*Republican*:
  - words beginning with 'dem' (the words 'demarest' and 'democracy' are filtered out)
  - 'dnc'
  - 'liberal'
  - 'libs'
  - words beginning with 'left' and ending with 'wing'

*Notes regarding the results of this first inquiry*:

The results of this first inquiry may not represent a true pattern in either party overall.  The amount of terms in the regular expressions are limited, and all the tweets are from around the same time in 2018.  On a larger timeline of tweets there could certainly be fluctuations in the results of analyzing using the same regular expressions.  The results could also be affected by instances of mentioning the opposing party that can only be inferred from context rather than a direct mentioning of a keyword.  The results of this program's analysis may simply reflect which party is more direct when mentioning the other rather than which party truly mentions the other more often.
