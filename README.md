# Sentiment-analysis-using-LSTM-BiLSTM-and-DistilBERT
This project aims to find a solution for the homonyms of words
## Contextual words and phrases and homonyms
<img src="https://i.pinimg.com/736x/b4/5b/ce/b45bce61ac5eea49a1deb6d339dc5164.jpg">

The same words and phrases can have **different** meanings according to the context of a sentence and many words – especially in English – have the exact same pronunciation but totally **different meanings**.

For example:

1. `I ran to the store because we ran out of milk.`

2. `Can I run something past you real quick?`

3. `The house is looking really run down.`

These are easy for humans to understand because we read the context of the sentence and we understand all of the different definitions. And, while **NLP language models** may have learned all of the definitions, **differentiating** between them in context can present problems.


# Dataset
<img src="https://storage.googleapis.com/kaggle-datasets-images/1417162/2347441/33d9f5bf223243529075f4566365f1c8/dataset-card.jpg?t=2021-06-18-09-43-24"
     width=600
     hight=600>
<br>
**IMDB dataset** having 50K movie reviews for natural language processing or Text analytics.
This is a dataset for binary sentiment classification containing substantially more data than previous benchmark datasets. We provide a set of 25,000 highly polar movie reviews for training and 25,000 for testing. So, predict the number of positive and negative reviews using either classification or deep learning algorithms.

# How can we avoid this problem
This problem occurs because **fixed word embeddings**.word embeddings can suffer from semantic drift, where the meaning of a word can change over time. This can lead to inaccurate results when using the embeddings for prediction tasks.
## In this  Notebook I will try some models to avoid this problem
    
1. RNNs have feedback connections that allow the output of a one-time step to be fed back as input to the next time step. is the baseline to be compared with other techniques
2. Bidirectional LSTM layers
> Bi-LSTM (Bidirectional Long Short-Term Memory) is a type of recurrent neural network (RNN) that **processes sequential data in both forward and backward directions**. It combines the power of LSTM with bidirectional processing, allowing the model to *capture both the past and future context of the input sequence*
> `Bi-LSTM could solve this problem `
3. Contextualized embeddings that were introduced by transformer architecture and LLMs models
>**contextualized** embeddings from such models as BERT or GPT, we will get two different representations based on the context around the word. That's the main difference between contextualized and non-contextualized embeddings

|Contextualized|	Non-contextualized|
|:----|:---|
|Many embeddings for one token depend on the context.|	One embedding for one word, no matter the context.|
|Embeddings are formed based on the context as you pass the whole sentence or text.|	Embeddings are saved as key-value pairs for word embedding. So, you do not need to pass the whole sentence to get the embedding.|
