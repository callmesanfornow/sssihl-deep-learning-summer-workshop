# Sunday 18th June

Pre Class Work : 

Running the notebook from coursework : [Notebook](./pre-classwork/10_nlp.ipynb)

Solving [Question and Answers](./question-and-answer-sat.md)
    
Quick Links:

* ResNet with PyTorch: [Notebook](./resnet-mnist.ipynb)
* ResNet with Fast.ai: [Notebook](./fastai-resnet34.ipynb)

## Sunday 18th June, 2023

### Class Notes:
    
* Question to ask:
    
    * LSTMs and vanishing Gradients problem? Are they still an important concept to learn?

### Word Embeddings:
Representing Words in a vector space.

|    |Battle|Horse|King|Man|Queen|...|Woman|
|----|----|----|----|----|----|----|----|
|authority|0|.01|1|.2|1|...|.2|
|event|1|.01|1|.2|1|...|.2|
|.|.|.|.|.|.|...|.|
|.|.|.|.|.|.|...|.|
|.|.|.|.|.|.|...|.|

### What are Langauge Models

Language Model predicts the next word based on previous words on the vocabulary that the model has. Words must be represented with a vector representation.

Bi-Gram Model. Sliding window to predict the next word.

Thou shalt not make a machine in the likeness of a human mind.

|input 1    |input 2    |output|
|-----------|-----------|------|
|thou       |shalt      |not|
|shalt      |not        |make|
|not        |make       | a|
|a          |machine    |in|
|machine    |in         |the|
|in         |the        |likeness|
|the        |likeness   |of|
|likeness   |of         |a|
|of         |a          |human|
|a          |human      |mind|

FastText, GLoVE embeddings.

Then BERT.

Use 20 news dataset to classify using word2vec, GLoVE or fast text. Run it through LR, SVC, RF, DT, XGBoost, some simple CNN.

Read up about CBOW, skip-gram

Mathematical Notation of RNNs

## Wednesday

RNN, LSTM, BERT