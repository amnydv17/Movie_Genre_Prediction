# Text Classification of Movie to Predict Movie Genres

### Author: [Aman Yadav](https://github.com/amnydv17)

## Business and Data Understanding

Movies are one of the most popular means of entertainment. There are large volumes of movie data being generated and shared on the internet every second.The genre of a movie can be deciphered from its synopsis much of the time. This project is a multiclass text classification problem which uses movie plot summaries to predict movie genres. NLP preprocessing techniques were implemented on the summaries to improve predictive capability. The dataset is from [Kaggle](https://www.kaggle.com/datasets/hijest/genre-classification-dataset-imdb) which contains about 54.2k  descriptions of movies. In this project, only movies that were assigned one genre were used.

Columns:
* ID - ID of column
* Title - title of the movies
* GENRE - Class of genre of the movies
* DESCRIPTION - DESCRIPTION of the movies


## Preprocessing

- The data was subset to include only the movies that have one genre. 
- I label-encoded the genres. 
- The 'Plot' column was then 'cleaned' using NLP preprocessing techniques (removed stopwords, punctuations, digits, changed text to lower case, lemmatization, tokenization)

## Exploratory Data Analysis

Frequency distribution of the genres showed the most prevalent genre was 'drama' with 'comedy' following close behind. The least common genre was 'romance'.




## Modeling and Results

The metric used in this project is the 'accuracy score'

The first simple model which predicted the most frequent class achieved an accuracy score of 24% which served as the baseline.

### Grid search on both tfidf and count_vectorizer transformed data:
#### Both Logistic regression performed the best, however logisitic regression performed better on the test set.
Best model was Multinomial Naive Bayes with tfidf transformed summaries with the following parameters:
* alpha': 0.2
* class_prior: None
* fit_prior: False


### Testing Result

I implemented the model on test data and achieved an acurracy score of 50% which is a significant increase from the baseline


## Conclusion
* Baseline accuracy was 41%
* The tfidf transformed plots performed better during modeling.
* GridSearchCV helped in narrowing down the best model hyperparameter values.
* Due to the fact that some of the genres had words in common with another genre, false predictions of those genres were mostly as the genres they had common words with.
* The decision tree models performed the least favorably.


## Navigation

```
├── data                                                <- folder containing data
│   ├── train, test data                                <- contains movie plot data scraped from Wikipedia
├── images                                              <- Visualizations used in README and pdf file
├── .gitignore                                          <- files to ignore
├── README.md                                           <- This README file
├── Movie_Genre_Classification.ipynb                    <- final notebook
└── predicted_genres.csv                                <- final presentation
```
## Contact Information

With questions or feedback on this repository, please reach out via:
- [GitHub](https://github.com/amnydv17)
- [LinkedIn](https://www.linkedin.com/in/amnyad05/)
 
 
