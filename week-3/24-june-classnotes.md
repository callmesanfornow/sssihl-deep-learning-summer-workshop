# June 24

1. Word2Vec without cleaning data + stopwords : [Notebook](/week-3/20-newsgroup-classification/20-newsgroup-word2vec.ipynb)
2. Word2Vec improved : [Notebook](/week-3/20-newsgroup-classification/20_newsgroup_word2vec_improved.ipynb), where 87% accuracy was achieved using SVC Linear
3. What is an RNN Mathematically?

At each time step t, an RNN takes an input vector x(t) and the hidden state vector h(t-1) from the previous time step (or an initial hidden state h(0)) and produces an output vector y(t) and an updated hidden state h(t) for the current time step. The hidden state vector h(t) represents the network's memory or information retained from previous time steps, which allows the RNN to process sequential information and capture long-term dependencies.

Equations governing the computation of an RNN:
  1. Input to Hidden State:
     
     h(t) = f(W_h * h(t-1) + W_x * x(t) + b_h)
     
     In this equation, W_h and W_x are weight matrices that control the flow of information from the previous hidden state and the current input, respectively. b_h is a bias term, and f() is an activation function applied element-wise.
  2. Hidden State to Output:
     
     y(t) = g(W_y * h(t) + b_y)
     
     Here, W_y is the weight matrix connecting the hidden state to the output layer, b_y is a bias term, and g() is another activation function that transforms the combined input to the output layer.

During training, the RNN parameters (weights and biases) are learned by optimizing a loss function that quantifies the discrepancy between the predicted outputs and the true outputs. This optimization process, such as gradient descent, adjusts the parameters to minimize the loss and improve the RNN's performance.

4. What is CBOW?

CBOW (Continuous Bag-of-Words) is a popular model architecture used in natural language processing (NLP) for word embeddings. It aims to learn distributed representations of words by predicting a target word based on its context. In CBOW, the model predicts a target word given a window of context words surrounding it. The context words are used as input, and the target word is the output. The order of the context words does not matter; hence, CBOW is referred to as a "bag-of-words" model.

5. What is Skip-Gram?
Skip-Gram is another popular model architecture used for learning word embeddings in natural language processing (NLP). Unlike CBOW, which predicts the target word given its context, Skip-Gram predicts the context words given a target word. It is specifically designed to capture the relationships between a target word and its surrounding context words.
