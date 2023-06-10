# Wednesday, 7th June 2023

## Questions to Ponder and Answer

### 1. **Difference between having multiple neurons in a single layer Vs distributing them across multiple layers.**

The main difference between having multiple neurons in a single layer and distributing them across multiple layers is that multiple layers allow for more complex representations of the data. Each layer represents different aspects or some specific part of a complex structure of the data.

In the context of image classification, which we discussed during the workshop, a single layer Neural Network(NN) can be used to classify images. Maybe a neuron can be used to represent a pixel color, a presence of objects or brightness etc.

We also can have a multi layer neural network that can classify images, where one layer can represent low level features of the image, like colors, brightness. The next can be shapes or object presence etc. The final hidden layer can be used to combine all the features from the previous layer to classify the image for output.

Advantages:

*   Complex representations: Multiple layers allow for more complex representations of the data. 
*   Better generalization: Multi-layer neural networks are often better at generalizing to new data than single-layer neural networks. This is due to the multiple layers in the NN that allow the network to learn more complex relationships between the input and output data.
*   Noise Sensitivity: Multi-layer neural networks are often less sensitive to noise in the input data than single-layer neural networks. This is because the multiple layers allow the network to learn to ignore noise and focus on the underlying signal.

Disadvantage:

*   Complexity: It is difficult to train due to the presence of multiple layers.
*   Need for Data: Due to the complexity of the data being broken down in layers, it requires more data to perform the classification task.
*   Overfitting Problems: Multi-Layer NN are very prone to overfitting compared to single layer NN due to the ability to fit as perfect as possible to input data.


### 2. **Generative Vs Discriminative**

**Discriminative Models:**

They learn from decision boundaries, based on labeleed data that is provided to the model, mostly supervised learning tasks. The goal is to predict the label class given a bunch of training features and the  features that is to be predicted.
    Ex: Classification Task, Regression Task etc.

**Generative Models:**
    This type of model learns the underlying distribution of every class of data. It is usually used for unsupervised tasks.
    Ex: Image Generation, Text Generation etc.

**Differences:**

|Feature|Discriminative Model|Generative Model|
|-------|-------|-------|
|Learning|Supervised|Unsupervised|
|Goal|Predict based on existing data| Understand the distribution|
|Example|Classifiers, Regressors|GPT, Midjourney, Stable Diffusion, Bard|


### 3. **Cross Entropy Loss**

**Binary cross entropy loss(BCE)**
It is a commonly used loss function in binary classification tasks. BCE measures the dissimilarity between the predicted probabilities and the true binary labels (0 or 1) for each sample from the dataset.

**Cross entropy loss**
Also known as categorical cross entropy.
It is a loss function used in multi-class classification tasks. It measures the dissimilarity between the predicted class probabilities and the true class labels.

Cross entropy loss encourages the model to assign high probabilities to the correct class and low probabilities to the incorrect classes, therefore minimizing the cross entropy loss leads to the model to learn to make more accurate predictions across multiple classes.

Both BCE loss and cross entropy loss are commonly used as objective functions in training machine learning models, especially in classification tasks. The choice between them depends on the specific problem and the number of classes being predicted.

### 4. **KL Divergence**

**KL Divergence (Kullback-Leibler Divergence)**
A.K.A Relative Entropy. It is a measure of the difference between two probability distributions. KL Divergence quantifies how a probability distribution diverges from another. KIt is commonly used in machine learning to compare and evaluate models or estimate the difference between two data distributions.


### 5. **Relation between KL Divergence and Entropy.**

Entropy is a measure of the average amount of information or uncertainty in a random variable. It characterizes the randomness or unpredictability of a distribution. 

It can also be seen as a measure of the additional information or extra average bits needed to encode data from one distribution when using a code optimized for another distribution.

KL divergence is a measure of dissimilarity between probability distributions, quantifying the additional information required to encode data from one distribution using a code optimized for another.
___