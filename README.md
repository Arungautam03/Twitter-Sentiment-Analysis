# Twitter-Sentiment-Analysis
- This project aims to build a machine learning model that analyzes a large volume of tweets directed at an airline and classifies them into positive, negative, or neutral sentiments.
- Such models are commonly used by platforms like Twitter and Facebook to filter out unwanted content, such as hate speech or inappropriate comments.
  
![image](https://github.com/user-attachments/assets/e54b24b6-58cc-4372-a634-ce00ccd210de)


## Problem Definition
-	Aim of project: analyze loads of twitter tweets, and be able to judge the sentiments behind the tweets : positive, negative or neutral sentiments

## Data Collection
-	Dataset used: https://www.kaggle.com/datasets/crowdflower/twitter-airline-sentiment
-	We Import the Dataset into our workspace Using PANDAS  which makes data manipulation easy.

## Data Cleaning & Preprocessing
-	We are concerned about 2 parameters: the actual text of the tweet(input of the NLP model) and the airline sentiment(output of the NLP model).
-	To improve model quality, drop all tweets with an 'airline_sentiment_confidence' below 0.5 (less than 50% confidence in sentiment classification).
-	Machine learning models only work with numbers but we do not have to convert all the words to number
- We just have to remove the unnecessary words by using the techniques:
1.	Removing Stop Words: Basically words like this, an, a, the, etc that do not affect the meaning of the tweet
2.	Removing Punctuation: ‘,.*!’ and other punctuation marks that are not really needed by the model
3.	Stemming: Basically reducing words like ‘jumping, jumped, jump’ into its root word(also called stem), which is jump in this case. Since all variations of the root word convey the same meaning, we don’t need each of the word to be converted into different numbers.
   
   ![image](https://github.com/user-attachments/assets/073d59d0-70e6-46be-aece-0ea739c18c1e)
   

## Feature Extraction
- As input is clean and ready, we convert it into numbers using ‘Bag of Words’
- 
  ![image](https://github.com/user-attachments/assets/68d02189-e4cb-4273-8612-2535cfa4eca8)

## Model Selection
-	Multinomial Naive Bayes model is used to figure out the relationship between the input and the output.
-	Multinomial NB is a supervised learning algorithm that works really well for text based data using sklearn library. 

 ## Model Training
-	We split the dataset into a training and testing section(testing size=30% of the actual data).

## Result
- Accuracy achieved: 0.77
- The **classification_report** function from sklearn.metrics provides a detailed summary of the model's performance by breaking it down into key evaluation metrics for each class (positive, negative, neutral in your case).




