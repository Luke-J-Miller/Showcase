# Sentiment Analysis on Movie Reviews

This project is a Sentiment Analysis performed on a dataset of movie reviews. The aim of the project is to predict the sentiment of a movie review which can be either positive or negative. 

The dataset consists of reviews and sentiments associated with them from the IMDB Reviews Database.  https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews 

## Methods Used

The project uses Natural Language Processing (NLP) techniques for the sentiment analysis. The main steps followed in the analysis are:

1. **Data Preprocessing:** The text of the reviews is cleaned and preprocessed. This involves removing stop words (common words that are deemed irrelevant), and lemmatizing the words (reducing them to their base or root form).

2. **Vectorization:** The processed text is then converted into numerical form (vectors) using the CountVectorizer provided by the sklearn library.

3. **Model Training:** A Multinomial Naive Bayes model is trained on the vectorized text. 

4. **Evaluation:** The performance of the model is evaluated on a test set, which was not used during the training phase. The model achieved an accuracy of 84.5%.

## Visualizations

There are two main visualizations in this project. These include:

1. **Countplot of Sentiments:** This is a bar plot showing the number of positive and negative reviews in the dataset. It helps understand the distribution of sentiments in the dataset.
   ![image](https://github.com/Luke-J-Miller/Showcase/assets/111100132/8f237063-8819-4702-a7e0-3920f7f40b20)

2. **Wordcloud** This was basically playing with a new tool.  I would like to play with the arguments to get something nicer.
![image](https://github.com/Luke-J-Miller/Showcase/assets/111100132/9fa2d56f-1018-4956-ae53-4eae2f552917)

3. **Confusion Matrix:** The confusion matrix is a heatmap that shows the number of true positives, true negatives, false positives, and false negatives predicted by the model. This gives a good idea of the model's performance. 
![image](https://github.com/Luke-J-Miller/Showcase/assets/111100132/fd4a5515-c4c8-43ec-a9c7-0f246cc4d48d)

## Conclusion

The model performs reasonably well with an accuracy of 84.5%. Future work could involve trying different models or using other forms of vectorization like TF-IDF to possibly improve the performance. 

## Notes

The current project uses the nltk library. To ensure that the required nltk data is downloaded, a function is included that checks and downloads the necessary data. Therefore, it is important to have internet connection when running the code for the first time. 

To reproduce the results, you would need to have the same versions of the libraries used. Please refer to the requirements.txt file for the versions of libraries used.
