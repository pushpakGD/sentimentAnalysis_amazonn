# Amazon Food Review- Sentiment analysis

- A mini project on Natural Language Processing by doing sentiment analysis on Amazon Food Reviews.
- Utilized Python NLP tool called NLTK, and implemented a complex model called Roberta and Huggingface pipeline.

A quick check to see the number of times a score occurs before seeing the results of each model.


## Two main techniques:

### VADER (Valence Aware Dictionary and Sentiment Reasoner) - Bag of Words approach

This first technique employs the VADER approach to conduct sentiment analysis on Amazon food reviews. VADER is a powerful tool for understanding the emotional tone behind a piece of text. By utilizing a Bag of Words approach, this method is used to extract valuable insights from the reviews, providing a nuanced understanding of customer sentiments towards food products on Amazon.

Results:

This first method will use NLTK's sentiment analyzer to get neg/neutral/pos scores of the text.

Bag of words approach is used
- stop words are removed (words that dont have a positive or negative meaning to them)
- each word is scored and combined to a total score



### Roberta Model and Hugging Face Pipeline

The Roberta Model, developed by Facebook AI, is an advanced natural language processing (NLP) model known for its superior performance in various language-related tasks. The the Hugging Face library, a popular NLP library provides easy access to pre-trained models like Roberta.
- Roberta model is a pre-trained model using various comments and reviews from Twitter.
  
Results:

- Model trained on a large corpus of data
- This model not only accounts for a single word but also the context related to other words

### Comapring Models and reveiwing examples:


