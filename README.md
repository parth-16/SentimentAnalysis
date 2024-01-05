## Sentiment Analysis
### Motivation
Embarking on the journey of creating a Sentiment analyser holds the promise of unveiling valuable insights into the collective emotions and opinions coursing through the vast social media landscape. In a world where information is disseminated at an unprecedented pace, understanding the sentiment behind the tweets allows us to decipher the pulse of the online community. By delving into the nuances of sentiment expressed in tweets, we not only gain a deeper understanding of public perception but also open doors to real-time market insights, political trends, and societal shifts. Harnessing the power of sentiment analysis on Twitter provides a unique opportunity to navigate the ever-evolving digital discourse, enabling businesses, policymakers, and individuals to make informed decisions, cultivate meaningful engagements, and stay attuned to the dynamic currents of public sentiment.
### Goal
In order to create a real-time sentiment analyser, I decided to test some models using the above dataset. This will help me understand which model works the best along with the required pre-processing and feature engineering techniques. 
### Dataset
The dataset is present on Kaggle called Sentiment140 dataset with 1.6 million tweets. The dataset consists of 1,600,000 tweets and have been extracted using the twitter api.
It consists of the following fields:
1. **target**: the polarity of the tweet (0 = negative, 4 = positive)
2. **ids**: The id of the tweet
3. **date**: The date of the tweet (format- "Sat May 16 23:58:44 UTC 2009")
4. **flag**: The query (lyx). If there is no query, then this value is NO_QUERY.
5. **user**: The user that tweeted
6. **text**: The text of the tweet 
### Exploratory Data Analysis
1. The dataset consists of 1600000 rows and 6 columns.
2. The only columns useful for this project are tweet and target.
3. The number of positive and negative tweets are equal(800000 each) 
### Data pre-processing
**Reducing the sample size**
The sample size that I will be using for the project is 100000 rows where I have taken 50000 tweets marked "Positive" and 50000 tweets marked "Negative" for simplicity.
**Stop word removal**
Stop word removal involves eliminating common words (e.g., "the," "and," "is") from any text to focus on meaningful words and reduce noise in NLP tasks.
**Removing punctuations, repeating characters, URLs, and Numbers**
Removing punctuations, repeating characters, URLs, and numbers in text preprocessing is essential to enhance the quality of NLP models by reducing noise, ensuring uniformity, and mitigating the impact of irrelevant or variable data patterns.
**Performing Stemming and Lemmetization**
Performing stemming and lemmatization is crucial for reducing words to their base or root form, promoting consistency in textual representation and improving the efficiency of language understanding and analysis by reducing variations of words.
**Performing vectorization**
Vectorization is essential to represent text data numerically, assigning weights to words based on their importance in a document relative to the entire text, enabling meaningful feature representation for machine learning models.
**Performing train-test split**
I have divided the dataset and assigned 80% to training and 20% to testing. 
### Model implementation
The models that I have implemented are:
Logistic Regression
KNN
Naive Bayes
Random Forest
Support Vector Machine
### Model evaluation
### Inferences and Takeaways
1.  In terms of accuracy, SVM performs the best. Next best is the Logistic Regression model. Naive Bayes and Random Forest have almost equal accuracies and last is the KNN model.

### Future work