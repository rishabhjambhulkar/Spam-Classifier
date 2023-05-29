# Spam-Classifier

- Dataset Link: https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset
Dataset contains set of SMS tagged messages that have been collected for SMS Spam research. It contains one set of SMS messages in English of 5,574 messages, tagged acording being ham (legitimate) or spam. The files contain one message per line. Each line is composed by two columns: v1 contains the label (ham or spam) and v2 contains the raw text.
## 1. Data cleaning 
- drop last 3 col and renaming the cols ham as target and content  as text.
- converting target into numerical form by label encoder and removed duplicates.
## 2.EDA
- count of spam and ham values by value counts and visualized  spam and ham data by pie chart.
- Using Nltk Tokenization no. of characters, words, sentences are calculated.
## Data Visualization
- Histogram is plotted to visualize value counts of no of words, sentences, characters.
- Pairplot and Heatmap is plotted to visualize relationship between this variables.
## Data Preprocessing
Following transformation is done to text and created new col name transformed_text which contains text after data preprocessing:
- 1 Lower case
- 2 Tokenization
- 3 Removing special characters
- 4 Removing stop words and punctuation
- 5 Stemming 
- 6 two List is created named Spam corpus and ham corpus which contains spam and ham  words.
- 7 Visualized  most common Ham and spam 30 words with bar plot and counter,

## Model Building
- transformed_text is vectorized by TF-Idf.
- GaussianNB,MultinomialNB,BernoulliNB are applied to transformed_text while target variable contains 0 or 1.
- GaussianNB : accuracy- 0.86 precision- 0.45, MultinomialNB: accuracy- 0.97 precision- 0.98 , BernoulliNB: accuracy- 0.97 precision- 0.97
- TF-Idf and MultinomialNB is selected because it gives high accuracy and high precision.


