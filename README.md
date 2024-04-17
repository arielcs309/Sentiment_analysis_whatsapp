# Sentiment Analysis Whatsapp: in Portuguese
Using the package Regex and NLTK.

# About the project

The project uses the package NLTK to read the sentiment analysis and they also have it for portuguese language. 
The first challenge for me was to transform the whatsapp txt file into a dataframe. 
So I used the Re package to find a pattern and separate the time, date, author and message.
``` bash
# finding the whatsapp pattern:
# [12:32, 27/03/2024] Mariane: Isso mesmo!

pattern = re.compile(r'\[(\d{2}:\d{2}), (\d{2}/\d{2}/\d{4})\] (.+?): (.*)')
raw = pattern.findall(chat)
```

## Stopwords
Stopwords are commonly occurring words (such as "the", "is", "at", "which", and "on")
that are often filtered out from text data because they usually do not carry significant meaning in the context of 
natural language processing tasks like text analysis, information retrieval, and sentiment analysis

It's important to erase them from the text.
``` bash
import nltk
nltk.download('vader_lexicon')
from nltk.sentiment import SentimentIntensityAnalyzer 
from nltk.corpus import stopwords
nltk.download('stopwords')
```
![counts](https://github.com/arielcs309/Sentiment_analysis_whatsapp/blob/master/Sentiment_counts.png)
## Wordcloud 
``` bash
from wordcloud import WordCloud
from wordcloud import STOPWORDS
```
![wordcloud](https://github.com/arielcs309/Sentiment_analysis_whatsapp/blob/master/Wordcloud.png)
# Language
![python](https://github.com/arielcs309/ML-Sklearn/blob/main/python.jpg)

# Author
Ariel Sousa. 
See my [Linkedin](https://www.linkedin.com/in/ariel-candido-22684578/) and my [Kaggle](https://www.kaggle.com/arielsousa)


