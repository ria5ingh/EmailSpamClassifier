# Email Spam Classifier

This is a machine learning project that classifies text messages as either "ham" (non-spam) or "spam". It uses the SMSSpamCollection dataset and a Multinomial Naive Bayes classifier.

## Project Description

The goal of this project is to build a simple and efficient spam classifier using basic Natural Language Processing techniques. The process includes loading and preparing the data, converting text into numeric features, training a classifier, and evaluating its performance.

## Dataset

The dataset used is the SMSSpamCollection, a collection of labeled SMS messages. Each message is labeled as either "ham" or "spam". The file is tab-separated and contains two columns: one for the label and one for the message content.

## Steps

1. Load the dataset and convert labels to binary format (ham = 0, spam = 1).
2. Split the dataset into training and testing sets.
3. Use CountVectorizer to convert messages into numerical feature vectors.
4. Train a Multinomial Naive Bayes model using the training data.
5. Predict labels for the test set.
6. Evaluate the model using accuracy, precision, recall, and F1-score.

## Results

The classifier achieves high performance with an accuracy of approximately 99 percent. The model performs well in both identifying spam and correctly labeling ham messages.

## Requirements

This project uses Python and the following libraries:

- pandas
- numpy
- scikit-learn

## Future Work

- Test on additional datasets
- Try alternative vectorization methods such as TF-IDF
- Experiment with other classification algorithms

## Note

This project is intended for learning and experimentation. It is not optimized for deployment in production environments.
