# Text Summarization
Here I have implemented and trained a text sumarization model, using a LSTM encoder-decoder model. The decoding was done with an attention layer. The code is written in pytorch.
I have used the [amazon review dataset](https://www.kaggle.com/currie32/summarizing-text-with-amazon-reviews) for training and evaluating my model.  
The dataset contains long text reviews and their summary pairs.  

# Model
The model uses pretrained word-embeddings from google [word2vec](https://code.google.com/archive/p/word2vec/).  
```Words_sequence-->Embeddings-->LSTM_encoder-->Attention_decoder```
### Training
The model trains using both ```teacher forcing``` and ```Non teacher forcing```. There is 50% chance to use either one.  
#### Teacher forcing
In this case we feed the model the target sequence and allow it to predict the next step of the same. This helps in convergence but is not how the model will output at test time.
#### Non teacher forcing
In this case the model has the same target, but at each step we feed the model the word it produced in previous time step. This is slower but helps achieve better results.

```
Read the Notebook for all the details and results

```


  




