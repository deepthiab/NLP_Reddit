# NLP with Reddit


 ## Contents:
 
- [Problem Statement](#Problem-Statement)  
- [Data](#Data)
- [Data Dictionary](#Data-Dictionary)
- [Data Analysis](#Data-Analysis)
- [Interesting Observations](#Interesting Observations)


## Problem Statement:

This project aims to predict if a post is from 'movies' subreddit or 'books' subreddit. Applications include being able to sort customer complaints to appropriate teams within a company.


## Data

Use Pushshift API to download posts from Reddit:

1. Books
2. Movies
    

## Data Analysis:

**Data Cleaning**
- Only the post itself was used as our feature
- Null, [removed] and [deleted] values were dropped.
- Since we had nearly 24K documents  after dropping the invalid text posts.

**Modeling**

Multinomial Naive Bayes with Count vectorizor gave the best accuracy score of 94.4% on the testing data wiht low variablity. The other model  tried to fit, TFID with Random forest  was overfit. Hence the model was not used. Below is the confusion matrix for the NB with CV.

![Alt text](image/confusion_matrix.png)


    
## Interesting Observations:


- 'just', 'really', 'like','time' were the most common words across both boards
- 'know' was one of the top 10 words in Books
- 'think' was one of the top 10 words in Movies


