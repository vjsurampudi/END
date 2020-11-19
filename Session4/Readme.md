Use the Sentiment Analysis code using Pytorch on IMDB dataset at: https://github.com/bentrevett/pytorch-sentiment-analysis/blob/master/2%20-%20Upgraded%20Sentiment%20Analysis.ipynb

Change this code in such a way that:

it has 3 LSTM layers
it has used a for loop to do so in the forward function
the dropout value used is 0.2
trained on the text that is reversed (for example "my name is Rohan" becomes "Rohan is name my"
achieves 87% or more accuracy

<h3>Approaches tried:</h3>
1. Reduced the default Learning Rate to 0.0001 <br>
2. Tried Glove embeddings of 300 dimensions instead of the 100 dimensions orignally used
