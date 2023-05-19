# Twitter tweets' sentiment scores
## Overview
The idea of this research is to calculate the sentimental score of tweets related to a trending topic on Twitter to see if this topic is discussed negatively or positively among users. The data is about the trending topics in specific areas, crawled directly from Twitter platform using twitter-api, with the WOE ID of the expected region. In this assignment, the trending topics of the world and in the US are taken. 

## The result
The common topics both trending around the world and in the US are chosen and saved in a list.

<img width="276" alt="image" src="https://github.com/MinhThanh2404/Twitter-tweets-sentiment-scores/assets/126949248/fc709f5c-e2b5-4bdd-a1ac-c68f0f72a8f3">

*(the data was crawled at around 10p.m UTC+7, 19/05/2023)*


Then, a random topic in this list is assigned, the system crawls popular tweets including that topic and having less than 100 words. Some NLP techniques were apply to process the tweet content, such as: tokenization, lemmatization, tagged. Then the sentiment score of each word is calculated by the average sentiment score of all possible sentiments given by the sentiwordnet library. The sentiment score of each sentence in the tweet is the average sentiment score of the words in it.

<img width="500" alt="image" src="https://github.com/MinhThanh2404/Twitter-tweets-sentiment-scores/assets/126949248/6c76e7cd-af97-4e66-8c2d-a4967ec9a2d1"><img width="100" alt="image" src="https://github.com/MinhThanh2404/Twitter-tweets-sentiment-scores/assets/126949248/487e2577-24db-4b6e-925c-308a6e4eed87">

*(choose random topic)*

<img width="335" alt="image" src="https://github.com/MinhThanh2404/Twitter-tweets-sentiment-scores/assets/126949248/49a7d7ab-8723-48b2-83ad-765da2972826">

*(the sentiment scores of sentence in each tweet stored in a list)*

The sentiment score of the whole tweet is estimated by the average score of all the sentences. Sub-zero scores indicate the tweet tends to be negative. Otherwise, the tweet is likely to give positive message.

<img width="308" alt="image" src="https://github.com/MinhThanh2404/Twitter-tweets-sentiment-scores/assets/126949248/9d20211b-69d8-4a2a-9e32-0b07e4506020">
<img width="629" alt="image" src="https://github.com/MinhThanh2404/Twitter-tweets-sentiment-scores/assets/126949248/8f152d11-3056-4e9f-9671-bfdfd922a5b3">

Visualize the sentiment score to understand the topic more.

![newplot (5)](https://github.com/MinhThanh2404/Twitter-tweets-sentiment-scores/assets/126949248/ae440898-c5e9-43a2-8074-6b01c7e6b150)

It can be seen from the skewed right plot that the amount of negative tweets is larger than the positive  ones. So, what was the topic about? It can be figured out by using WordCLoud to find most frequent words.

![image](https://github.com/MinhThanh2404/Twitter-tweets-sentiment-scores/assets/126949248/5d69587b-b363-4605-beae-5ae383609fce)

Most common words are: Andy Rourke (the topic), pancreatic, cancer, RIP, sadness, passing, illness. It can be concluded that a celebrity named Andy Rourke has passed away due to an illness called pancreatic cancer, and the users are expressing their sympathy, sorry to his/her loss.
