# Sentiment Analysis (NLP) using LSTM and Naive BayesClassifier
Sentiment analysis on women e-commerce store dataset
Author: Claudia Słaboń

Data comes from:
https://www.kaggle.com/nicapotato/womens-ecommerce-clothing-reviews

Files:
- ML2_Project.ipynb - Python code
- Presentation_Sentiment_analysis_project.pdf - Short presentation describing problem and the results
- Project_report_Sentiment_analysis.pdf - short, detailed project report

Aim: The aim of this project is to predict customer satisfaction (negative, neutral, positive) based on the review.

Used methods: Long short-term memory (LSTM) networks Naive Bayes approach were used.

Final LSTM model is a combination of 2 pre-models:
- first LSTM embedding layer contained words’ weight obtained from GloVe (Global Vectors for Word Representation) which can be downloaded from the following link (https://nlp.stanford.edu/projects/glove/);
- second LSTM embedding layer contained words’ weight obtained from Word2Vec model which was trained on the dataset.

LSTM pre-models - optimization parameters:
- Number of hidden layers (model contains 1, 2 or 3 hidden layers)
- Dropout value (parameter was equal to: 0.2, 0.3, 0.4 or 0.5)
- Number of hidden neurons (depending on the layer parameter was equal to: 64, 32 or 16)
- Learning rate for Adam optimizer (parameter was equal to: 0.01, 0.001 or 0.0001)

Final 2 pre-models were chosen based on the highest validation accuracy.

Finally, the predictions of the best pre-models were combined together using average.

At the end results from LSTM model and Naive Bayes model were compared.
Accuracy of the models:
- LSTM (82,2%),
- Naive Bayes Classifier (80,6%).
