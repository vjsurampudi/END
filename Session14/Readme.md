This folder contains the program to train a transformer to write simple python codes when the question is given. The data used o train the transformer is also attached.

Data Cleaning
--------------
Most of the data was cleaned using hand. The data file attached is the cleaned file which are corrected for correct tabs. The data provided contained 4324 samples totally.

Data Augmentation
-----------------
Data Augmentation was done. We used the CoNaLa dataset which contains snippets of python code. The CoNaLa dataset had train and test files with 'intents' and 'rewritten-intents' which acted as questions for the code snippets 'snippets'. Thus we could get two question for the same snippet. The CoNaLa dataset added 5656 samples and thus increased the total number of samples to train the transformers to 9980.

Data Reading
------------
Some of the code had comments in it. Thus it became necessary to replace the '#' symbol to be replced with '#$$$' so that the Question can be distinguished from python code and hence can be easily read. Thus all the python questions starts with the symbol '#$$$'.

Tokenisation
------------
For the Python Questions, since they are in English, we used the spacy tokenizer. The Python code was tokenized using 'tokenizer' in python which can be used to tokenize the source code.

Embedding layer
---------------
1. We have used the default embedding layer that is available in pytorch to train the embeddings for the transformers. 
2. Customized Embedding Layer is next in line though we have not implemented it here.

Transformer Model
-----------------
The transformer model is the same as the one in the famous paper -  'Attention is all we need'. 

Loss Function
-------------
Here we have used the cross-entropy loss function. We have not tried any other loss function. The goodness of the result (i.e. python code prediction from the transformer) is given using the perplexity. Though there are other measures like BLEU score, ROUGE etc which can probably provide a better insight on the prediction.

Some of the example outputs are given in the file at this link https://github.com/vjsurampudi/END/blob/main/Session14/SampleResults.txt
