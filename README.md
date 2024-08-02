<h1 id= "top doc"> Description </h1>

---




1. General info

In this project, we aim to use an NLP model that can predict the stock market of a certain stock by analyzing Twitter sentiment using a transformer based neural network and show that it makes stock predictions with reasonable accuracy. Previous implementations of news-based stock market predictors have usually only focused statistical methods instead of Machine Learning and Natural Language Processing techniques. 

Link for sentiment analysis model:
[website](https://huggingface.co/cardiffnlp/twitter-roberta-base-sentiment-latest) 




2. Used methods

After taking the latest information about ***Nvidia*** we used ***snscrape*** for extracting the latest tweets about Nvidia from **tweeter.com** and used a welknown model for sentiment analysis:

- [roBERTa-base model](https://huggingface.co/cardiffnlp/twitter-roberta-base-sentiment-latest)

- Sentiment Analysis



# Highlights



 ```python

sent_results = {}
count = 0
for i, d in tqdm(tweet_df.iterrows(), total=len(tweet_df)):
    sent = sentiment_task(d["Text"])
    sent_results[d["Tweet Id"]] = sent
    count += 1
    if count == 60000:
        break

 ```





- link to some where <a href= "#top doc"> go to up </a>
