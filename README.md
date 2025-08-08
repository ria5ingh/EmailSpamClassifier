# Email Spam Classifier

This is a machine learning project that classifies text messages as either "ham" (non-spam) or "spam". It uses the UCI SMSSpamCollection dataset and a Multinomial Naive Bayes classifier. The goal of this project is to build a simple and efficient spam classifier using basic Natural Language Processing techniques. The process includes loading and preparing the data, converting text into numeric features, training a classifier, and evaluating its performance.

## Dataset

The dataset used is the UCI SMSSpamCollection, a collection of 5574 labeled SMS messages. Each message is labeled as either "ham" or "spam". The file is tab-separated and contains two columns: one for the label and one for the message content.

## Steps

1. (Preprocessing): Load the UCI dataset and convert labels to binary format (ham = 0, spam = 1).
2. Split the dataset into training and testing sets.
4. Use CountVectorizer to convert messages into numerical feature vectors.
6. Train a Multinomial Naive Bayes model using the training data.
7. Predict labels for the test set.
8. Evaluate the model using accuracy, precision, recall, and F1-score.

## Results

The classifier achieves high performance with an accuracy of approximately 99 percent. The model performs well in both identifying spam and correctly labeling ham messages. However, this is also because the model was trained on 80% of the dataset, and tested on the remaining 20%, so it is not surprising that it has high accuracy. 

## Testing on Other Datasets

We also tested the trained NB model (trained on the UCI dataset), on a separate dataset from https://github.com/AbayomiAlli/SMS-Spam-Dataset (ExAIS_SMS Spam Dataset, shown under the newspam folder). The data collected was conducted at the Federal University of Agriculture, Abeokuta, Nigeria with the aim of building an indigenous SMS Spam corpus with African-English context. Before testing, we had to preprocess the data by conjoining multiple CSV files, and dropping NaN (null) values, and loading only the 'label' and 'message' columns into the new dataframe.

The testing size was much larger, as we testing on the entire dataset (5238 messages) instead of 20% of it. The UCI-Dataset-Trained NB model had an accuracy score of 0.61 when testing on the ExAIS_SMS spam dataset, meaning it accurately classified 61% of the messages as 'ham' or 'spam.'

## Future Recommendations

To make the model more accurate, training on more datasets and using hyperparametrizing techniques could optimize model performance. 

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
