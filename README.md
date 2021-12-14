# HATE SPEECH ON TWITTER WITH TEXT MACHINE LEARNING
 Hi,
 This is one of my Data Science research, so I decided to share with you all.

This project considered HatEval dataset. This dataset came from SemEval 2019 (Task 5) for a competition on multilingual (English and Spanish) detection of hate tweets targeting women and immigrants. It is made up of sets of three labels. The first label denotes whether the tweet shows hatred towards women or immigrants, the second, whether the tweet is aggressive, and the third, whether the tweet is directed against an individual or the entire group.

During the steps of the project, this dataset was explored, analysed and then evaluated using a wide range of machine learning and deep learning techniques.
A clear discussion on the performance of different models will be covered using standard evaluation metrics including accuracy, F1-score, Precision and Recall, and also using the alternative evaluation measurements, the Partial Match Ratio and the Exact Match Ratio.

## Aim and Objectives

The aim of this project was to conceive and deploy a machine learning model that automatically detects the use of hate speech on the Twitter social network.
In order to successfully complete the goal, the objectives below were set:
•	To Provide a documentation of the different stages of the project
•	To set up the case study focused on automatic detection of hate speech
•	To perform a certain number of experiments
•	To evaluate the results of each of the experiments.

## Description of the task
The task surrounding the project case study is articulated into two sub-tasks:
- Subtask 1 - Detecting Hate Speech against women and immigrants:
In the subtask 1, a series of machine learning algorithms will be going to predict whether a tweet in English or in Spanish, targeting an individual (woman or an immigrant) or a group of people (women or immigrants), has hate speech (HS) or not.

- Sub-task 2 - Aggressiveness and target classification

In Subtask B, the ML algorithm, after identifying the hateful tweet, will going to classify these hateful tweets in two ways: aggressiveness and Target Range (TR). Aggressiveness (AG) means whether the identified HS is aggressive or not. And TR means whether the identified HS targets a specific individual or a generic group of individual.

## Evaluation Measures

The evaluation of the results considers different strategies and metrics for Subtasks 1 and 2 in order to allow more fine-grained scores.
About subtask 1, systems will be evaluated using standard evaluation metrics, including Accuracy, Precision, Recall and macro-averaged F1-score.
Regarding the evaluation of the subtask 2, two principles are to be considered including partial match and exact match. Concerning the partial match, the labels to be predicted (HS, TR and AG) will be evaluated separately by using the standard evaluation metrics mentioned above where the macro-averaged F1-score will be computed.
However, about the exact match, all the labels to be predicted will be combined to compute the Exact Match Ratio (EMR)

## Corpus Collection and Data Understanding

As mentioned in chapter 4, this dataset was provided by SemEval 2019 (Task 5) for a competition on multilingual detection of hate tweets targeting women and immigrants. The following gathering strategies have been used to collect the data, between July and September 2018, from Twitter.
Firstly, observing and keeping track on individuals which are likely to be targeted by hate accounts. When the hate account has been identified, then download its history.
Finally, filtering news feed and streams using the words, hashtags and stems. In the collected data, the following keywords occurred more often: 
"migrant, refugee, #buildthatwall, bitch, hoe, women for English, and inmigra-, arabe, sudaca, puta, callate, perra for Spanish".
The HatEval dataset consists of 19,600 tweets, of which 13,000 are in English and 6,600 are in Spanish.

## Results Analysis

## Evaluation with standard metrics: Subtask 1
Five traditional ML models, including MNB, KNN, LogR, Linear SVM and DT, were grouped into two types of vectorization including Count Vectorizer and TFIDF Vectorizer.

Considering the English Data, it has been observed that by using the Count Vectorization approach, MNB achieves 74% of accuracy in detecting HS, followed by LogR which performs 73%. When applying the TFIDF Vectorization approach, once again MNB comes first by achieving 73% of accuracy on the main category, HS, followed by LogR with 72% of both accuracy and F1-score. However, RoBERTa performs the best with the accuracy of 87% followed by DistilBERT with 83% of accuracy.
Note that the four transformer-based pre-trained models, including BERT, DistilBERT, RoBERTa and XLNet, achieve high accuracies than traditional ML models where the least performing model, XLNet, reaches 79% of accuracy, which is 5% more than the high performing among traditional ML models.

Given the Spanish Data, when applying the Count Vectorization approach, LogR achieves respectively 78% of accuracy and 78% of F1-score in detecting HS, followed by MNB which performs respectively 73% of accuracy and 76% of F1-score. The others, SVM, DT and KNN achieve respectively 76%, 71% and 59% of accuracy each.
When using TFIDF Vectorization approach, SVM performs 78% of both accuracy and F1-score, followed by LogR with 77% of accuracy.
But again, RoBERTa achieves the top and best scores with 87% of accuracy and 80% of F1-score, followed by BERT with 82% of accuracy and 77% of F1-score.

According to the results all the four transformer-based pre-trained models perform better than traditional ML models on English data, while on Spanish Data, 3 out of 4 transformer-based pre-trained models achieve the highest performance compared to traditional ML models.

## Evaluation with Partial Matches and Exact match Ratio: Subtask 2

When applying Count Vectorization approach on English Data, SVM performs the higher partial match ratio with the value of 0.72 or 72% of F1-score, followed by LR with 68%, followed by DT with 65% then 60% for both MNB and KNN each. For this approach, LR performs higher EMR by 80% followed by SVM with 79%, followed by MNB with 78% then KNN and DT with 77% each.
By using TFIDF Vectorization approach, SVM performs the higher partial match ratio with 70% of F1-score, followed by LR with 68% and which achieves the higher EMR with 79%, followed by DT with 62%. However, KNN and SVM come after LogR with both 78% of EMR.
However, the outperforming scores for the partial match and the EMR were achieved using RoBERTa with 78% and 90% respectively.

By implementing Count Vectorizer on Spanish Data, LogR performs the higher scores for the partial match ratio and EMR, with 80% and 82% respectively. Followed by SVM with 78% of partial ration and 80% of EMR.
By using TFIDF Vectorizer, SVM achieves the higher scores for both partial match ratio and EMR, with 79% of F1-score and 81% of EMR, followed by LogR with 77% of partial match ration and 80% of EMR.
However, the outperforming scores for the partial match and the EMR were again achieved using RoBERTa with 78% and 90% respectively.

## In brief,
Accuracy was used as the main evaluation metric. In addition, other measurements were used such the macro average F1-score, Precision and Recall and finally Partial match ratio and EMR. However, these measurements did not seem to be enough perfect. Therefore, the use of ROC and AUC could help confirm the experiment results.











