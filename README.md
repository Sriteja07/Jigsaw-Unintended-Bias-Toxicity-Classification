# Jigsaw-Unintended-Bias-Toxicity-Classification

## Project Summary

1. Jigsaw is a technology incubator which was child comapny of google. It mainly focuses on providing remedies to Internet attacks, online attacks on free speech etc;
2. The objective is to reduce the unintended bias towards certain religion groups, communities, genders and also to predict toxicity of comments on them.
3. AUROC is the metric used.
4. The dataset can be found at kaggle ":https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification/data". It has around 1.8 Million data points and 45 features. Among those features, identity features are present and in almost all the cases they are Null values. Also, a test set is also provided with 2 features namely, comment text and Target.
5. One of the features 'comment_text' represents the text comment and another one is 'target' which determines the toxicity of the comment.So, the problem is to measure the toxicity of the comment by analysing the text.
6. This problem can be posed as a classification problem by classifying the comments as toxic and non-toxic.So, the comments which are over 0.5 toxicity are considered as toxic comments and rest of them are taken as Non-toxic and are also labeled accordingly.
7. The train dataset is highly imbalanced with 92% non toxic comments and 8% toxic comments. So a dumb model can achieve 92 % accuracy by predicting all of them as non-toxic.
8.Initially, new features such as comment length, number of words in the comment are created. After this, text preprocessing is done by removing unnecessary punctuations, stopwards etc;
9. In addition to these 2 features, another four features namely Compound ,Positive ,Negative , Neutral are created by using NLTK's Vadar Sentiment Intensity Analyser.
10. These four features were stacked to the train and test datasets and some EDA is performed on these features.
11. Then the Train dataset is divided into Train and cv datasets. The text of all the datasets is vectorised using Tfidf Vectoriser.
12. Several ML and DL models such as Naive Bayes, Logistic Regression , Linear SVM , Gradient Boosting, LSTM are trained on this new set of features, and had their hyperparameters tuned.
13. Among all the models SGD classifier (Logistic regression with balanced class weight) performed better with 96.5 train AUC and 94.8 CV AUC.
