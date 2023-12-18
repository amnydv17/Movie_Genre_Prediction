Movie Genre Classification Using Movie Plot Summaries
Author: Aman Yadav
Business Understanding
Movies are a popular form of entertainment generating vast amounts of data on the internet. Understanding a movie's genre from its synopsis is crucial. This project focuses on multiclass text classification, utilizing movie plot summaries to predict genres. The dataset sourced from Kaggle comprises 54.2k movie descriptions. For this analysis, only movies with a single assigned genre were used.

Columns:

ID: Unique identifier
Title: Movie title
GENRE: Movie genre
DESCRIPTION: Movie plot summary
Data Preprocessing
Subsetting involved selecting movies with a single genre.
Genre labels were encoded.
NLP preprocessing techniques (stopwords removal, punctuation/digit removal, lowercase conversion, lemmatization, tokenization) were applied to clean the 'DESCRIPTION' column.
Exploratory Data Analysis
Genre frequency distribution revealed 'drama' as the most prevalent genre, closely followed by 'comedy'. 'Romance' appeared as the least common genre.

Modeling and Results
The chosen evaluation metric is the 'accuracy score'.

A simple baseline model predicting the most frequent class achieved 24% accuracy.
Grid search was performed on both tfidf and count_vectorizer transformed data.
Logistic regression and Multinomial Naive Bayes emerged as the top-performing models.
Multinomial Naive Bayes with tfidf-transformed summaries, utilizing an alpha value of 0.2, achieved the best accuracy of 50% on the test set.
Conclusion
Key Findings:

Baseline accuracy stood at 24%, improving to 50% with the final model.
Tf-idf transformed plots outperformed other techniques.
GridSearchCV aided in selecting optimal hyperparameters.
Misclassifications often occurred due to shared words among genres.
Decision tree models displayed the least favorable performance.
Project Structure
r
Copy code
├── data                                                <- Folder containing data
│   ├── train, test data                                <- Movie plot data scraped from Wikipedia
├── images                                              <- Visualizations used in README and PDF files
├── .gitignore                                          <- Files to ignore
├── README.md                                           <- This README file
├── Movie_Genre_Classification.ipynb                    <- Final notebook
└── predicted_genres.csv                                <- Final presentation
Contact Information
For questions or feedback, please reach out via:

GitHub
LinkedIn
