# Week 1
---
## Course 1
    https://course.fast.ai/Lessons/lesson1.html
    https://github.com/fastai/fastbook/blob/master/01_intro.ipynb

## Course 2
    https://course.fast.ai/Lessons/lesson2.html
    https://github.com/fastai/fastbook/blob/master/02_production.ipynb

---


Performed a weather classification using images from Kaggle. Achieved **90%** accuracy using resnet34. [Notebook](/week1-weather-classification/weather-classification-kaggle-dataset.ipynb)

Created a Huggingface spaces using gradio: https://huggingface.co/spaces/callmesan/weather-classification

Used 2 sample images to perform prediction for testing.


## Class Notes:

Language Models: A probabilty distribution over a sequence of words.

Unigram Model : p(w) = Π<sub>i=1</sub><sup>n</sup> p(w<sub>i</sub>)

Bigram Model : p(w) = p(w<sub>1</sub>) Π<sub>i=2</sub><sup>n</sup> p(w<sub>i</sub>|w<sub>i-1</sub>)

