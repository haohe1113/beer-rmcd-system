# We Got Your Beers!  
## Crowdsourced Beer Recommendation System  
![intro](https://user-images.githubusercontent.com/47257479/102526570-7b536380-4061-11eb-923e-9d017298c5ca.jpg)  

## Quick Links  
- [Introduction](https://github.com/haohe1113/beer-rmcd-system/blob/main/README.md#Introduction)  


## Introduction  
[Beeradvocate.com](https://www.beeradvocate.com/) is an online beer rating webstie. Alongside the ratings, people also post their reviews about the experience with various beers. In this project, we scraped beer reviews from Beeradvocate.com and used them to build a beer recommendation system with various text mining concepts. The recommendation system was required to accept user inputs about desired attributes of a product and come up with 3 recommendations.   

## Pakages Used  
* Selenium  
* NLTK  
* spaCy (Cosine Similarity)  
* VADER (Word Level Sentiment Analysis)  

## Approach  
1. Scraped Beeradvocate.com for ~6k reviews on thousands of beer products.  
2. Identified 3 beer attributes assuming that a user of this recommendation system would input in order to search for desired beers.  
3. Performed a similarity analysis between the 3 attributes and the reviews using [spaCy](https://github.com/explosion/spaCy); Extracted 300 reviews that have the highest similarity scores.  
4. Performed sentiment analysis using [VADER](https://github.com/cjhutto/vaderSentiment) on these 300 reviews and sort them by the sentiment scores.  
5. Recommended 3 beers to the user based on a general ranking system which combines similarity scores and attribute sentiment scores.  

## Analysis and Insights  
 
**1. Attributes chosen**  
*We picked the top 3 mostly mentioned beer attributes over all reviews scraped:  

**sweet:** Malty, grainy, caramel-like;  
**Fruity:** Flavors reminiscent of various fruits;                                                                   
**Robust:** Rich and full-bodied;    

**2. Top Reviews with highest similarity scores**  
![Alt Text](cos_similarity.png)  

