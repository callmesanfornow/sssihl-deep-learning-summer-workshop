# Week 1
---
## Course 1
    https://course.fast.ai/Lessons/lesson1.html
    https://github.com/fastai/fastbook/blob/master/01_intro.ipynb

## Course 2
    https://course.fast.ai/Lessons/lesson2.html
    https://github.com/fastai/fastbook/blob/master/02_production.ipynb

---


Performed a weather classification using images from Kaggle. Achieved **90%** accuracy using resnet34. [Notebook](./weather-data-classification/weather-classification-kaggle-dataset.ipynb)

Created a Huggingface spaces using gradio: https://huggingface.co/spaces/callmesan/weather-classification

Used 2 sample images to perform prediction for testing.


## Saturday, 3rd June 2023

Language Models: A probabilty distribution over a sequence of words.

Unigram Model : p(w) = Π<sub>i=1</sub><sup>n</sup> p(w<sub>i</sub>)

Bigram Model : p(w) = p(w<sub>1</sub>) Π<sub>i=2</sub><sup>n</sup> p(w<sub>i</sub>|w<sub>i-1</sub>)

### The Universal Approximation Theorem

Mathematically speaking, any neural network architecture aims at finding any mathematical function y= f(x) that can map attributes(x) to output(y). 

The accuracy of this function i.e. mapping differs depending on the distribution of the dataset and the architecture of the network employed. The function f(x) can be arbitrarily complex.

The Universal Approximation Theorem tells us that Neural Networks has a kind of universality i.e. no matter what f(x) is, there is a network that can approximately approach the result and do the job! This result holds for any number of inputs and outputs.

___

## Wednesday, 7th June 2023

1. Basic PyTorch Model and how to create a Neural Network in PyTorch: 
[Notebook](./simplePytorchNeuralNet.ipynb).

2. Modify the above neural network to perform picture classification. [Notebook](./simplepytorchmodel.ipynb)

3. Answer the questions asked : [QnA](question-answers.md)