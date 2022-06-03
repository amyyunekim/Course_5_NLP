
## MVP Overview

### Goal:
- To find topics of discussion and assess sentiment towards films from Cannes film festival 2022.

### Process:

- Imported Tweets with Cannes hashtags from May 17 to May 28 2022 into python using the Twint library.
- Created a clean tweet function involving regex and removing stop words.
- Stemmed words using SnowballStemmer however it didn't improve results so original cleaned tweets were used.
- Tried both Count Vectorizer and TFIDF to create document-term matrices. Count Vectorizer did not work well as celebrity fans were flooding certain terms so TFIDF was selected.
- Tried LSA, NMF, LDA for topic modelling. NMF was chosen as the topics made more sense from visual inspection and were more clearly grouped.

### Findings:

- For the NMF model, n_components = 10, 15, 50 were attempted so far. Higher n_components (50) topics did not work well as the topics were were not as clear and terms were bleeding across different topics. 
- Top 6 movies appearing in the topics were:
1. Broker <br>
broker, iu, leejieun, lee, brokercannes2022, team, bonvoyagebrokerteam, brokeratcannes2022, ji, eun
2. Armageddon Time<br>
anne, hathaway, annehathaway, armageddon, time, jeremy, armageddontime, strong, photocall, greg
3. Crimes of the Future<br>
kristen, stewart, crimes, future, crimesofthefuture, kristenstewart, photocall, david, premiere, cronenberg
4. Elvis<br>
elvis, austin, butler, elvismovie, premiere, baz, party, hanks, tom, shakira
5. Decision to Leave<br>
park, leave, decision, chanwook, director, tang, wei, premiere, decisiontoleave, chanwooks
6. Triangle of Sadness<br>
triangle, sadness, palme, dor, ruben, amp, close, stlund, won, prize


### Further work:
- Continue to tune the number of topics to include smaller films, which is proving challenging.
- Assign sentiment to each movie through VADER and further deconstructing tweets by extracting adjectives through POS tagging.
- Compare results to actual Cannes awards won by movies.