# Sentiment-Analysis-On-Amazon-Food-Review
## Sentiment Analysis with RoBERTa and VADER

### Intoduction
Sentiment analysis, also known as opinion mining, is a natural language processing (NLP) task that involves determining the sentiment or emotional tone expressed in a piece of text. The goal is to classify the sentiment as positive, negative, or neutral. Sentiment analysis has applications in customer feedback analysis, social media monitoring, product reviews, and more.

### Overview
This project demonstrates the use of RoBERTa and VADER models for sentiment analysis on textual data. The goal is to classify text into positive, neutral, or negative sentiments based on their content.

### Tools used for this project:
* Python
* Google Colab (Notebook)
* NLTK
* Hugging Face
* Numpy
* Pandas
* Seaborn
* Matplotlib

### Dataset:
https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews

**About the  dataset**:
This dataset consists of reviews of fine foods from amazon. The data span a period of more than 10 years, including all ~500,000 reviews up to October 2012. Reviews include product and user information, ratings, and a plain text review. It also includes reviews from all other Amazon categories.

### Models Used:
**RoBERTa**: A state-of-the-art NLP model from Hugging Face's Transformers library.

**VADER**: A lexicon and rule-based sentiment analysis tool that is particularly effective for social media texts.

### Usage
**i)Preprocess the data**:
Clean the text data by removing unwanted characters, stopwords, and applying tokenization.

**ii)Run the sentiment analysis**:
Execute the notebook or script to classify the text data into positive, neutral, or negative sentiments using the RoBERTa and VADER models.

### Key Issues and Solutions
1. **Loss of Sentiment Context During Preprocessing**
   - *Issue*: Removing stop words and lemmatization/Stemming altered sentiment context.
   - *Solution*: Updated preprocessing to preserve key sentiment words and negations.

2. **Minimal Preprocessing Approach**
   - *Issue*: Needed to maintain sentiment context while simplifying preprocessing.
   - *Solution*: Implemented a basic preprocessing function that only removes punctuation and converts text to lowercase.

3. **Evaluation of Sentiment Analysis with VADER**
   - *Issue*: Lack of direct evaluation metrics for VADER.
   - *Solution*: Compared VADER predictions with the actual 'Score' column to calculate evaluation metrics.

### Results
The sentiment analysis results will provide the probability distribution over the sentiment classes (negative, neutral, positive) for each text sample.

**Results of an example text**:

{
    "roberta_neg": 0.97635514,
    "roberta_neu": 0.020687465,
    "roberta_pos": 0.0029573692
}

**Interpretation**:
The example indicates a strong negative sentiment according to the RoBERTa model.

