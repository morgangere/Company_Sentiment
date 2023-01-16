# Company_Sentiment
Group Project worked on by myself (Morgan Gere) along with Suihin Wong, and Niranjan Juvekar.  The project was attempting to take a data set obtained from kaggle and create a process of using text mining techniques and form the best process of predicting sentiment on a tweet.  This size of the data set and the number of models and options tested required that it be broken up into different notebooks each focused on a particular portion of the project.  Each notebook has a specified readme section below.  The data set itself was prelabeled as either Postive, Negative, or Neutral.
##### Base line
The data is simply imported, and the raw agreement and baseline comparison accuracies were determined.  Raw agreement is simply if all predictions went into one category.  IE the sentiment for all was said to be neutral the model would achieve around 40 % accuracy.  We then needed a baseline comparison which we selected NLTK’s Sentiment Analyzer Vader.  Out of the box system was found to be around 64% accurate.  This was the accuracy to beat.
##### Word Cloud / EDA
The tweets were separated into different data frames and word clouds were created.  The purpose of this is to examine the differences words used in positive vs negative vs all tweets. The word clouds were shaped like twitter’s bird logo just because it could be done, and it looks nice.
![image](https://user-images.githubusercontent.com/118774600/212759566-a5536f3e-80f9-48ca-9ecd-8fd52f523378.png)
![image](https://user-images.githubusercontent.com/118774600/212759576-a5613a2b-853a-46ae-a1c7-c6a4caa5cbbc.png)
![image](https://user-images.githubusercontent.com/118774600/212759588-4b9ff59d-4d00-408a-9c2f-b2cf4044d027.png)


##### Vectorization options
##### New Feature generation
##### Gridsearchsv tuning
##### Final Models
##### Clustering
