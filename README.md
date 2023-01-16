# Company_Sentiment
Group Project worked on by myself (Morgan Gere) along with Suihin Wong, and Niranjan Juvekar.  The project was attempting to take a data set obtained from kaggle and create a process of using text mining techniques and form the best process of predicting sentiment on a tweet.  This size of the data set and the number of models and options tested required that it be broken up into different notebooks each focused on a particular portion of the project.  Each notebook has a specified readme section below.  The data set itself was prelabeled as either Postive, Negative, or Neutral.
### Base line
The data is simply imported, and the raw agreement and baseline comparison accuracies were determined.  Raw agreement is simply if all predictions went into one category.  IE the sentiment for all was said to be neutral the model would achieve around 40 % accuracy.  We then needed a baseline comparison which we selected NLTK’s Sentiment Analyzer Vader.  Out of the box system was found to be around 64% accurate.  This was the accuracy to beat.
### Word Cloud / EDA
The tweets were separated into different data frames and word clouds were created.  The purpose of this is to examine the differences words used in positive vs negative vs all tweets. The word clouds were shaped like twitter’s bird logo just because it could be done, and it looks nice.
![image](https://user-images.githubusercontent.com/118774600/212759650-fa7fde4b-40cd-4f0b-a947-5cecb4a394dd.png)
![image](https://user-images.githubusercontent.com/118774600/212759714-0720a275-0d6e-48d2-902a-8f5171f3d890.png)
![image](https://user-images.githubusercontent.com/118774600/212759740-e68eb326-0431-4f6e-a9ec-60d75958d2b7.png)
### Vectorization options
The first steps were to do some preprocessing and replacing tweet slang that is common in the data set to its regular vocabulary.  An example would be 2day replaced with today.  NLTK Tokenizer was tested against NLTK tweet tokenizer.  8 different vectors were created using combinations of the two tokenizers using stop words or not, using stemming or not and adding in bigrams.
All 8 different vectorization options were run on SVM and Multinomial Naive Bayes models.  Overall accuracy was found along with F! scores for each category examples are shown below.
![image](https://user-images.githubusercontent.com/118774600/212761628-d2f1e284-d1dd-4a0b-9c01-bb131f121b2f.png)
![image](https://user-images.githubusercontent.com/118774600/212761656-7db877ff-a313-4ac5-b8ce-d73ff90f7b2a.png)
### New Feature generation
Using text mining techniques, new features were added based on the tweets.  These included a link count which simply counted the number of links a tweet contained, a count for each Emoticon used in the tweet, a count of the number of sentences, a word count, a column which tracks if the tweet uses negation.  Each was added separately to the best preforming SVM and Multinomial Naïve Bayes models and a combination of the best two preforming features was tested as well. Accuracy was used to find the best model and a graph off the SVM accuracy is below as an example.
![image](https://user-images.githubusercontent.com/118774600/212761756-9fb651ca-1c4e-4cae-8748-0650b49604e8.png)
### Gridsearchsv tuning
The best preforming SVM model was turned using Gridsearchcv the results are below.
![image](https://user-images.githubusercontent.com/118774600/212762576-c77a1157-4779-472e-9d30-1e9082b535ca.png)
### Final Models
The best preforming model between SVM and Multinomial Naive Bayes was SVM and with the vectorization options, new features added and the tuning set, the accuracy and F1 scores for each category was graphed along with the list of the most important features names which is the words that show the most relevance to determining sentiment.
![image](https://user-images.githubusercontent.com/118774600/212763122-64ba2891-830e-4a79-ae79-cb20bba6585c.png)
![image](https://user-images.githubusercontent.com/118774600/212763156-8c73b9d6-e459-434e-85bf-a6035deb2b89.png)

### Clustering
Clustering was preformed on the model after to deteremine if it could be used to find different tweets by sentiment.  Yet upon inspection the best clustering showed tweets taht are focused on the individual who is writing the tweets while the other clusters is twees that mention another person or entity. The clustering is shown below along with some eample tweets of the different clusterings. 
![image](https://user-images.githubusercontent.com/118774600/212763803-657e0461-15df-43e6-9209-b5541df66cbe.png)

### An examples of tweets in the first cluster is as shown below:

as much as i love to be hopeful, i reckon the chances are minimal =P

i`m never gonna get my cake and stuff

I really really like the song Love Story by Taylor Swift

My Sharpie is running DANGERously low on ink

i want to go to music tonight but i lost my voice.

### Some examples of tweets in the second cluster are:

'you can ride one, you can catch one, but its not summer til you pop open one'  ?

Hey, you change your twitter account, and you didn`t even tell me...

i miss you bby      wish you were going tomorrow to make me do good.

Hi  how are you doing ???  *just joined twitter...*

Happy Mothers day to all you Mums out there

### Paper
A Reporrt was created explaining in detail beyond this readme the project and that is also included above.
