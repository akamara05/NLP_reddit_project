# Reddit NLP Project 


## Problem Statement 
XYZ consulting has been hired by the District of Columbia Courts to conduct research on the types of legal advice being sought after on social media forums such as Reddit. As not many people can afford the high lawyer fees, and pro- bono legal services aren’t as quickly available as most would like, they are seeing an uptick of people seeking legal advice on social media platforms in order to receive immediate responses to their legal issues. Our ultimate goal with this project is to create DC Court’s very own public platform, a repository where non-criminal legal information can be researched and obtained by interested citizens; a ‘one-stop shop’  for common legal questions.  

This part of the project (phase 1) is our discovery phase. We’d first want to see what language is being used and what sorts of topics are being discussed, all in the efforts of tailoring a product as best as we can, that reflects our citizens’ needs. As much as we want accessibility to information we also want factual information being provided. With this platform we aim to verify and ensure that the information being provided is accurate and reputable. 


## Background 
With increased connectivity and access to a plethora of information disseminated via numerous social media platforms, we are interested in knowing what users are searching/asking about, posting ,and ultimately absorbing. A lot of this information sharing is being done over various social media platforms, a popular one being Reddit, a ” social news aggregation, web content rating, and discussion website “(reddit.com). With a vast array of subbredits (sub-topics) people are able to discuss any topic of their choosing at length, in hopes of getting some sort of feedback, advice (solicited or otherwise), or any other form of interaction. No topic seems out of bounds within these forums. People are willing to seek all sorts of advice, such as where to find the best home décor, what to feed their pets, even advice on sensitive legal matters, from seemingly complete strangers. To assist by being a reputable source, DC Court’s would like to create their own platform geared towards citizens in need of immediate legal information. To achieve that, we’ll be approaching this project in phases. For phase 1, we’ll be using our data science skills to discover the types of legal matters being discussed, the popularity of said topics, and the language surrounding these.   


## Scope & Methodology
__Part 1. Data Collection:__ To begin with, we used API to scrap text data (3,000 observations each) from two subreddits, ‘Legal Advice’  and ‘Casual Conversations’.  We were interested in using the casual conversation subreddit alongside the legal advice  subreddit in order to see if the language used is similar between the two, do topics overlap, are conversations kept “casual” or do we see some legal jargon being used. We used the text classification approach looking to see if models we’ve constructed could first identify what constituted legal discussions compared to just casual conversations. Also, the casual conversations subreddit is text heavy , so used alongside the legal advice subreddit, another text heavy subreddit, we expected great results for our NLP models.

__Part 2. Data Cleaning:__ We cleaned the initial dataset being cognizant of missing data or features that may not be necessary for our analysis. As this is a NLP project we ensured to remove and replace any characters and punctuation, essentially stripping the text data to just words with the aim of increasing our model precision and accuracy. As a final step in this part, we merged the two subrreddit data frames into one for a much-streamlined analysis. 
Part 3. EDA: Here we begin to explore the clean data and get an idea of how these features alone and in combination with other complimentary features may affect our ultimate goal of proper text classification. Using a simple CountVectorizor , we sought to find common words within each subbredit as well as the corpus. Words such as just', 'know', 'time', and 'going', looked to be common words shared between both subreddits.

__Part 4a.__ Preprocessing: We took our cleaned data and tokenized, lemmatized, and stemmed the respective text data and created respective columns for each. From that we used a  TF-IDF transformer to reduce any influence common words, within each of the text data variations, may have on our model. This preprocessing step is performed in order to reduce bias in our models and achieve higher accuracy scores. 
Part 4b. Modeling: We used Logistic Regression and Random Forest Classification models. 

## Conclusion 

With a common set of constraints across “raw” posts, lemmatized posts, and stemmed posts we achieved the following results:
* Based on the accuracy scores, misclassification rate, specificity score, and sensitivity score our logistic regression model with stemmed text data, performed the best and increased our precision of proper classification of subreddit posts.

* Based on the accuracy scores, our RF model with stemmed text data, performed the best and increased our precision of properly classifying our subreddit posts.

* Out of the two models used, the Random Forest model yielded the best results.

* Our stemmed words resulted in a higher accuracy score compared to the lemmatized words, score of 0.96 compared to 0.74.

* For both models used it's evident the benefits of pre-processing the text data, either lemmatizing of stemming, in order to improve our model accuracy.


__Next steps__
We’d like to look not only at the posts but the related comments, what types of responses are these posts receiving , especially within the legal advice subreddit. Do  the responses contain legal terms, and also are these more factual or opinion based responses. 

