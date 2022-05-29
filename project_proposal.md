
## Question/Need:

What is the question behind your analysis or model and what practical impact will your work have?

1. Sentiment towards films from Cannes film festival 2022 held from May 17 to May 28 2022.
2. Topic modelling to try to assess what people are saying about each film

Who is your client and how will that client benefits from exploring this question or building this model/system?

- Film distributors will be able to assess sentiment and conversation around new films in real time and assist in picking which movies to release.

## Data Description:

- Twitter data with movie hashtags: 
    - Use hashtag of #Cannes2022 
    - Also try hashtags for top N list of movies

What is an individual sample/unit of analysis in this project? In other words, what does one row or observation of the data represent?
- A document or bag of words

What characteristics/features do you expect to work with? In other words, what are your columns of interest?
- Document terms

If modeling, what will you predict as your target?
- Sentiment (positive, neutral, negative) toward the film
- Identify topics being discussed around the films 


## Tools:

How do you intend to meet the tools requirement of the project?
- Twint for acquiring Tweets
- VADER for sentiment tagging
- NLTK, scikit learn for topic modelling
- Seaborn and matplotlib for vizualisations

## MVP Goal:

Have data gathered, cleaned and transformed into a document-term matrix
Start testing topic modelling methodology