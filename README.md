## Sentiment Analysis
### Motivation
Embarking on the journey of creating a Sentiment analyser holds the promise of unveiling valuable insights into the collective emotions and opinions coursing through the vast social media landscape. In a world where information is disseminated at an unprecedented pace, understanding the sentiment behind the tweets allows us to decipher the pulse of the online community. By delving into the nuances of sentiment expressed in tweets, we not only gain a deeper understanding of public perception but also open doors to real-time market insights, political trends, and societal shifts. Harnessing the power of sentiment analysis on Twitter provides a unique opportunity to navigate the ever-evolving digital discourse, enabling businesses, policymakers, and individuals to make informed decisions, cultivate meaningful engagements, and stay attuned to the dynamic currents of public sentiment.
### Goal
In order to create a real-time sentiment analyser, I decided to test some models using the above dataset. This will help me understand which model works the best along with the required pre-processing and feature engineering techniques. 
### Dataset
The dataset is present on Kaggle called [Sentiment140 dataset](https://www.kaggle.com/datasets/kazanova/sentiment140) with 1.6 million tweets. The dataset consists of 1,600,000 tweets and have been extracted using the twitter api.
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
   
![image](https://github.com/parth-16/SentimentAnalysis/assets/59089155/c9764828-af25-4bb7-87b0-c6c1f63e4fa1)

### Data pre-processing
1. **Reducing the sample size**
The sample size that I will be using for the project is 100000 rows where I have taken 50000 tweets marked "Positive" and 50000 tweets marked "Negative" for simplicity.
2. **Stop word removal**
Stop word removal involves eliminating common words (e.g., "the," "and," "is") from any text to focus on meaningful words and reduce noise in NLP tasks.
3. **Removing punctuations, repeating characters, URLs, and Numbers**
Removing punctuations, repeating characters, URLs, and numbers in text preprocessing is essential to enhance the quality of NLP models by reducing noise, ensuring uniformity, and mitigating the impact of irrelevant or variable data patterns.
4. **Performing Stemming and Lemmetization**
Performing stemming and lemmatization is crucial for reducing words to their base or root form, promoting consistency in textual representation and improving the efficiency of language understanding and analysis by reducing variations of words.
5. **Performing vectorization**
Vectorization is essential to represent text data numerically, assigning weights to words based on their importance in a document relative to the entire text, enabling meaningful feature representation for machine learning models.
6. **Performing train-test split**
I have divided the dataset and assigned 95% to training and 5% to testing. 
### Model implementation
The models that I have implemented are:
1. Logistic Regression
2. KNN
3. Naive Bayes
4. Random Forest
5. Support Vector Machine
### Model evaluation

![image](https://github.com/parth-16/SentimentAnalysis/assets/59089155/2de4d3ff-8367-4ce6-afeb-b36f303a70e2)

### Future work
1. I plan to implement more advanced deep learning architectures like transformer-based models (e.g., BERT, GPT) to capture more intricate patterns in sentiment data.
2. I also plan to explore techniques for sentiment analysis that can handle multiple languages for improved user experience and also perform text summarization.
3. I will be developing a real-time sentiment analyzer using this trained model to perform sentiment analysis on tweets extracted from the Twitter API in real-time.
