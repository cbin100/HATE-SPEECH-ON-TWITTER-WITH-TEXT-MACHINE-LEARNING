# HATE SPEECH ON TWITTER WITH TEXT MACHINE LEARNING
 HATE SPEECH ON TWITTER WITH TEXT MACHINE LEARNING

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





