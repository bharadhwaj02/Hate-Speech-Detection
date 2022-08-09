# Hate-Speech-Detection || TWITTER DATA ANALYSIS 
Detecting the hate tweets using various ML algorithms and generaing accuracies of the ML algorithms


 
 
 
# ADVANCED DATA ANALYTICS 
 


# Abstract:  
Hate speech is an unfortunately common occurrence on the Internet and in some cases culminates in severe threats to individuals. Therefore, social media sites face the problem of identifying and censoring problematic posts while weighing the right to freedom of speech. The importance of detecting and moderating hate speech is evident from the strong connection between hate speech and actual hate crimes. Hate speech in the form of racist and sexist remarks is a common occurrence on social media. For that reason, many social media services address the problem of identifying hate speech, but the definition of hate speech varies markedly and is largely a manual effort. We analyze the features that improve the detection of hate speech. While it is easy to identify racist and sexist slurs, hate speech is often expressed without any such terms. Furthermore, it is not trivial for humans to identify hate speech due to differences in exposure to and knowledge of hate speech. To reliably identify hate speech, we need a clear decision list to ensure that problematic tweets are identified. so to identify the hate speech (racist or sexist tweets) on Twitter we build a model. Early identification of users promoting hate speech could enable outreach programs that attempt to prevent an escalation from speech to action. Sites such as Twitter have been seeking to actively combat hate speech. Our contribution We provide a data set of almost 32k tweets annotated for hate speech. We also investigate which of the features we use to provide the best identification performance. 
 
 
# Introduction : 
Social Media are sensors in the real world that can be used to measure the pulse of societies. However, the massive and unfiltered feed of messages posted on social media is a phenomenon that nowadays raises social alarms, especially when these messages contain hate speech targeted at a specific individual or group. 
Among the many existing social networks, Twitter currently ranks as one of the leading platforms. Twitter is an American microblogging and social networking service on which users post and interact with messages known as "tweets" and it is a well-known real-time public microblogging network where, frequently, the news appears before official news media. Characterized by its short message limit (now 280 characters) and unfiltered feed, its usage has quickly escalated, especially amid events, with an average of 500 million tweets posted per day. And toxic content has become a major issue in today’s world due to an exponential increase in the use of the internet by people of different cultures and educational backgrounds. Differentiating hate speech and offensive language is a key challenge in the automatic detection of toxic text content. This report proposes an approach to automatically classify tweets on Twitter into two classes: hate speech and non-hate speech.  
 
# Objectives: 
1.	To detect hate speech in tweets, as tweets contain hate speech if it has a racist or sexist sentiment associated with it. 
2.	we aim to classify the toxic tweets from other tweets. 
   
Our project analyzed a dataset CSV file from Kaggle containing 31,935 tweets. The dataset was heavily skewed with 93% of tweets or 29,695 tweets containing non-hate labelled Twitter data and 7% or 2,240 tweets containing hate-labelled Twitter data. 
1.	The first step of building our model was to balance the number of hate and non-hate tweets. 
2.	We clean the specific parts of tweets data by using regular expressions to remove URLs and user handles that begin with ‘@ 
3.	Using TweetTokenizer from NLTK, we tokenize the tweets into individual terms. 
4.	And then stop words, # symbols and redundant terms like ‘amp’, ‘rt’, etc are also removed. 
5.	Then for the pre-processing step, we use Term Frequency Inverse Document Frequency (TFIDF). 
6.	Then we create a classification model by using Logistic 
Regression 
7.	Then we use regularization, hyperparameter tuning, stratified k-fold and cross-validation to get the best model 
 
TFIDF is a numerical statistic that is intended to reflect how important a word is to a document in a collection. It is used as 
a weighting factor in searches for information retrieval, text mining, and user modelling.

# Results and Discussions : 
 
Firstly, we have considered the data which classifies the tweets based on their characteristic attributes matching against their original tweets. Next, we cleaned the data through various data pre-processing techniques such as normalizing the data, removing user handle names, URL links and other forms of data which may cause disruptions to the process. Now we tokenize the tweet and again remove the words of length as they are very less significant. 
  
Now we segment the top terms and put them in a new list. We will divide the resultant data into the testing and training data with a split ratio of 0.7:0.3 additionally by using the 
Tfidvectorizer we Transform text to feature vectors that can be used as input to estimator for logistic regression classification 
We prepare the Logistic Regression model and classify the training data and generate the classification report which shows the resultant data accuracy as a 0.95 f1 score. Now doing the grid search by setting the class weight to balanced, stratifiedfold to 4 and estimating the best attribute to classify the data. Now we perform the prediction for the test data set and calculate the accuracy for the f1-score, which is 0.92 
 
By observing the classification report of the training data we can say that the precision of both the labels is equal and there is a huge difference in the recall score resulting in an f1 score of 0.98 and 0.55 respectively. The attributes macro average and weighted average also share the same disparity as the labels. Finally the accuracy of the resultant f1 sore and support are 0.96 and 22373. 
  
Again after further process of the data, we get the classification report of the training data whose results are not equal in precision and recall, giving the f1 score of 0.96 and 0.58 respectively and the attributes macro average and weighted average have the precision of 0.72 and 0.92 and recall of 0.85 and 0.92 resulting in the f1 score of 0.77 and 0.93 respectively. the accuracy of the resultant f1 score is 0.92 and its support is 9589.  	  

# Conclusions:  
 
As hate speech continues to be a societal problem, the need for automatic hate speech detection systems becomes more apparent. In this report, we proposed a solution to the detection of hate speech and offensive language on Twitter through machine learning using TF IDF values. We performed a comparative analysis of Logistic Regression and Instantiate the grid search model with StratifiedKFold value 4. The results showed that Logistic Regression performs comparatively better with the TF IDF approach. 
 
We presented the current problems for this task and our system that achieves reasonable accuracy (96%) as well as recall (77%). Given all the challenges that remain, there is a need for more research on this problem, including both technical and practical matters. 
  
# References : 
Capozzi, Arthur T. E., et al. ““Contro L’Odio”: A Platform for Detecting, Monitoring and Visualizing Hate Speech against Immigrants in Italian Social Media.” Italian Journal of Computational Linguistics, vol. 6, no. 1, 1 June 2020, pp. 77–97, 10.4000/ijcol.659. 
Accessed 27 Apr. 2021. 
https://www.researchgate.net/publication/336987923_HATECHECKER_a_ Tool_to_Automatically_Detect_Hater_Users_in_Online_Social_Networks ---. ““Contro L’Odio”: A Platform for Detecting, Monitoring and Visualizing Hate Speech against Immigrants in Italian Social Media.” Italian Journal of Computational Linguistics, vol. 6, no. 1, 1 June 2020, pp. 77–97, 10.4000/ijcol.659. Accessed 27 
Apr. 2021. 
 https://iris.unito.it/retrieve/handle/2318/1659197/387293/paper024.pdf 
