# python_tweet_analysis
Analyzing tweets from republican and democrat representatives - obtained from a kaggle database.

Uses Python 3.7 and Jupyter Notebooks

Requires:
  - sqlite3 (version 2.6.0)
  - matplotlib (version 3.0.1)
  - matplotlib-venn (version 0.11.5)
  
BUG NOTES: THE YML FILE DOES NOT SEEM TO WORK VERY WELL

THE LATEST VERSION OF ANACONDA HAS EVERYTHING YOU NEED TO RUN THE JUPYTER NOTEBOOK ASIDE FROM 'matplotlib-venn', WHICH CAN BE INSTALLED USING 'pip install matplotlib-venn' FROM THE ANACONDA PROMPT.

THIS NOTEBOOK HAS ONLY BEEN TESTED ON WINDOWS 10 OPERATING SYSTEMS

---

<h1>Summary</h1>

This project is intended to compare and contrast the words found in a database of 85,000 tweets from US congresspeople separated into two categories based on their political party - Democrat or Republican.


<h1>First Inquiry</h1>

The first question I wanted to answer regarding the information I found was:  "How often does each party mention the other in this collection of tweets?"  I achieved this goal by parsing the text of all of the tweets from each party in search of different keywords intended to represent an occurance where the opposing party is mentioned.

I used regular expressions to search for the following character sets

**Democrat**:
  - Words beginning with 'repub' (the word 'republic' is filtered out)
  - 'gop'
  - 'conservative'
  - Words beginning with 'right' and ending with 'wing'
    
**Republican**:
  - Words beginning with 'dem' (the words 'demarest' and 'democracy' are filtered out)
  - 'dnc'
  - 'liberal'
  - 'libs'
  - Words beginning with 'left' and ending with 'wing'
  
The visualization for this inquiry is a bar graph comparing instances of these words found for each party.

**Notes regarding the results of this first inquiry**:

The results of this first inquiry may not represent a true pattern in either party overall.  The amount of terms in the regular expressions are limited, and all the tweets are from around the same time in 2018.  On a larger timeline of tweets there could certainly be fluctuations in the results of analyzing using the same regular expressions.  The results could also be affected by instances of mentioning the opposing party that can only be inferred from context rather than a direct mentioning of a keyword.  The results of this program's analysis may simply reflect which party is more direct when mentioning the other rather than which party truly mentions the other more often.

<h1>Second Inquiry</h1>

The second question I wanted to answer regarding the information I found was:  "What are the most common words in each party's tweets, and how many words are shared between the parties?"  I achieved this goal by gathering the text from each and every tweet, splitting the strings into individual words based on spacing, filtering out common stop-words, and counting instances of each word used.

The visualization for this inquiry is two bar graphs comparing instances of these words found for each party, as well as a venn diagram to show the words found in common.

**Notes regarding the results of this second inquiry**

The results of this second inquiry are once again not necessarily representative of the parties as a whole.  These results are limited by the fact that they are based solely upon tweets from 2018.  The large amount of top words in common when viewing the top 100 most-used words between the parties may serve as evidence for the parties being more similar than they are often given credit for.  This could be due to the fact that both parties are the undoubtedly the most powerful political parties in the USA, it is unsurprising that the same form of language and structure of speech might appeal to a wide enough audience to allow that rise to power.  Not to mention they both discuss the same topics fairly often.  The difference between the two parties may be found moreso in how these common words are used to structure posts rather than the words themselves.  There also may be words in addition to the common stop words I filtered out that could be filtered out to see a more unique set of top words from each party.
