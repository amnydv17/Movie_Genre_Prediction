# Movie Genre Classification Using Movie Plot Summaries

## Author: Aman Yadav

### Business Understanding

Movies, a prevalent form of entertainment, generate vast amounts of data on the internet. Predicting a movie's genre from its synopsis holds significant value. This project focuses on multiclass text classification, utilizing movie plot summaries to predict genres. The dataset, obtained from Kaggle, consists of 54.2k movie descriptions. For analysis, only movies with a single assigned genre were considered.

#### Columns:
- **ID:** Unique identifier
- **Title:** Movie title
- **GENRE:** Movie genre
- **DESCRIPTION:** Movie plot summary

### Data Preprocessing

Preprocessing steps involved:
- Subsetting data to include movies with a single genre.
- Encoding genre labels.
- Applying NLP techniques (stopwords removal, punctuation/digit removal, lowercase conversion, lemmatization, tokenization) to clean the 'DESCRIPTION' column.

### Exploratory Data Analysis

Analysis of genre frequency distribution revealed:
- 'Drama' as the most prevalent genre, closely followed by 'Comedy'.
- 'Romance' as the least common genre.

### Modeling and Results

Evaluation Metric: 'Accuracy score'

Key Results:
- Baseline model predicting the most frequent class achieved 24% accuracy.
- Grid search conducted on tfidf and count_vectorizer transformed data.
- Top-performing models: Logistic Regression and Multinomial Naive Bayes.
- Multinomial Naive Bayes with tfidf-transformed summaries achieved 50% accuracy on the test set using an alpha value of 0.2.

### Conclusion

Key Findings:
- Baseline accuracy: 24%, improved to 50% with the final model.
- Tf-idf transformed plots outperformed other techniques.
- GridSearchCV aided in selecting optimal hyperparameters.
- Misclassifications often occurred due to shared words among genres.
- Decision tree models displayed the least favorable performance.

### Project Structure

├── data <- Folder containing data
│ ├── train, test data <- Movie plot data scraped from Wikipedia
├── images <- Visualizations used in README and PDF files
├── .gitignore <- Files to ignore
├── README.md <- This README file
├── Movie_Genre_Classification.ipynb <- Final notebook
└── predicted_genres.csv <- Final presentation


### Contact Information

For questions or feedback, please reach out via:

- [GitHub](https://github.com/amnydv17)
- [LinkedIn](https://www.linkedin.com/in/amnyad05/)
