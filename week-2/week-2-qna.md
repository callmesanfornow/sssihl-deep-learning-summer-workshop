# Wednesday 14th June 2023

### 1. What is the relation between convolutions and Correlations?

**Ans**: Both operations are linear in nature.

Convolution is a mathematical operation that combines two functions, typically a signal(a function over time) and a filter(a mathematical operation), to produce a third function. 

In the context of image processing, a convolution operation involves applying a filter or a kernel to an image. The filter is typically a small matrix of numerical values. The convolution operation is carried out by sliding the filter over the image, performing an element-wise multiplication between the filter and the underlying pixel values, and then summing up the results. This process is repeated for each pixel in the image.

Correlation, on the other hand, measures the similarity between two signals or functions. It determines how much one signal resembles another by comparing their values at different time points or positions. In correlation, the filter used is not flipped before being applied to the signal.

In image processing, correlation is useful for tasks such as object detection, where a known template or pattern is matched against an image to locate instances of the template. It is also used in image registration, where two or more images are aligned based on their similarity.


### 2. Prove that $\sigma(x)$ = $\frac{1}{1+e^{-x}}$, where is a sigmoid function.

**Ans**: Here is the [Proof](./sigmoid%20Proof.jpg)!

### 3. Implement a simple Convolution Neural Network in PyTorch.

**Ans**: Implemented CNN in pytorch using FashionMNIST. Here is the [Notebook](./simplecnn.ipynb) with implemetation.

### 4. Solve a numerical problem on Backpropagation.

**Ans:** Here is the [Notebook](./backpropogation-numerical.ipynb) with implementation.

### 5. Implement Backpropagation in NumPy.

**Ans**:Implementing it

Sample Data:

|*X1*|*X2*|*y*|
|---|---|---|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|0|

with 1000 epochs and learning rate of 0.1. Here is the [Notebook](./backpropogation-numpy.ipynb) with implementation.


### 6. Add Batch Normalization layer to your CNN + L1, L2 Normalisation

**Ans:** Implented the same FashionMNIST by modifying model to include Batch, L1 and L2 Normalisation. Here is the [Notebook](./simplecnn-batch-l1-l2.ipynb) with implementation.