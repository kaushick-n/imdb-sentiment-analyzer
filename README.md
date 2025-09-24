# IMDb Sentiment Analysis – Naive Bayes Model
## Project Overview
This project implements a sentiment analysis model for IMDb movie reviews using Naive Bayes model. It classifies the reviews as either positive or negative.

The dataset (IMDB Dataset.csv) contains 50000 reviews with 2 columns:
- review - text of the movie review
- sentiment - label (positive or negative)

## Tech Stack
- pandas 
- scikit-learn

## Procedure:
1. **Data Loading**: I loaded the dataset using pandas dataframe and put the columns as review(input) and sentiment(output)
2. **Text Vectorization**: Raw test cannot be put directly into a ML model so i used CountVectorizer from scikit-learn module to convert the raw data into numerical values using bag of words algorithm. I coded it to remove the common English stop words (like the, is, and etc) as they dont add any value and interfere with the output. It also keeps only the top 5000 most frequent words to reduce dimensionality.
3. **Train-Test Split**: The dataset was split into 80% training and 20% testing sets using train_test_split.
4. **Model selection and training data**: Naive Bayes model is used here as it is fast and efficient and works well with word freq features. I then trained the model using fit()
5. **Evaluation**: Then the model is passed into the testing phase where i made test set using predict() function. I found the accuracy using accuracy_score.

## Results
The accuracy of the model was found to be **84.47%**
