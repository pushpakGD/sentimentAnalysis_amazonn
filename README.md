# Amazon Food Review- Sentiment analysis

- A mini project on Natural Language Processing by doing sentiment analysis on Amazon Food Reviews.
- Utilized Python NLP tool called NLTK, and implemented a complex  model called Roberta and Huggingface pipeline.

A quick check to see the number of times a score occurs before seeing the results of each model.

![sAn1](https://github.com/pushpakGD/sentimentAnalysis_amazonn/blob/main/images/sAn1.png)

- Most of the reviews are 5 stars, basically more biased towards positive reviews.

## Two main techniques:

### VADER (Valence Aware Dictionary and Sentiment Reasoner) - Bag of Words approach

This first technique employs the VADER approach to conduct sentiment analysis on Amazon food reviews. VADER is a powerful tool for understanding the emotional tone behind a piece of text. By utilizing a Bag of Words approach, this method is used to extract valuable insights from the reviews, providing a nuanced understanding of customer sentiments towards food products on Amazon.

Results:

This first method will use NLTK's sentiment analyzer to get neg/neutral/pos scores of the text.

Bag of words approach is used
- stop words are removed (words that dont have a positive or negative meaning to them)
- each word is scored and combined to a total score

#### VADER outputs results as shown below

![sAn2](https://github.com/pushpakGD/sentimentAnalysis_amazonn/blob/main/images/sAn2.png)

The positive, negative and neutral scores are displayed. And according to this one comment, it has tagged it more negative which means its a negative sentiment. 

Compound score as mentioned is an aggregation of pos, neg and neu scores, from -1 to +1 considering how neg and pos, a comment is. And it seems to indicate how positive and negative a comment is.

Lets have a look at the barplots plotting the VADER results

![sAn3](https://github.com/pushpakGD/sentimentAnalysis_amazonn/blob/main/images/sAn3.png)

Now looking at distribution pos, neg and neu reviews 
![sAn4](https://github.com/pushpakGD/sentimentAnalysis_amazonn/blob/main/images/sAn4.png)

- positivity is higher as the score is higher
- neutral is kind of flat
- it becomes less negative of a comment as the star review becomes higher

Its exactly as expected, the more positive a comment is, the more higher the compound score and vice-versa.

### Roberta Model and Hugging Face Pipeline

The Roberta Model, developed by Facebook AI, is an advanced natural language processing (NLP) model known for its superior performance in various language-related tasks. The the Hugging Face library, a popular NLP library provides easy access to pre-trained models like Roberta.
- Roberta model is a pre-trained model using various comments and reviews from Twitter.
  
Results:

- Model trained on a large corpus of data
- This model not only accounts for a single word but also the context related to other words

## Comparing Models and reveiwing examples:

![rOm1](https://github.com/pushpakGD/sentimentAnalysis_amazonn/blob/main/images/rOm1.png)

From the pairplot we can see, VADER model is less confident in all of its predictions compared to Roberta model which clearly seperates the positivity, neu and neg scores for each of the predicted values.

#### some examples where the model scoring and review score differ the most.

- Text is said to be positive by the model but is given one score by what the actual reviewer.

![rev1](https://github.com/pushpakGD/sentimentAnalysis_amazonn/blob/main/images/rev1.png)

- now to negative sentiment but given a 5 star review 

![rev2](https://github.com/pushpakGD/sentimentAnalysis_amazonn/blob/main/images/rev2.png)

- positive review but a negative sentiment (kind of funny)
- both models got confused with that review, however the models performed well as its a negative sentiment but with a positive review.



