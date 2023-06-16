# Saturday 17th June, 2023

### 1. Explore the architectures of AlexNet, VGGNet.

**Ans**: 

##### AlexNet
AlexNet was a breakthrough in image classification tasks. It consists of eight layers, with five convolutional layers followed by three fully connected layers. AlexNet employed the rectified linear unit (ReLU) activation function, which accelerates convergence compared to traditional activation functions. It also incorporated dropout regularization to mitigate overfitting. AlexNet's most distinctive aspect was its utilization of parallel processing on two GPUs, which allowed it to process a large amount of data efficiently.

##### VGGNet

VGGNet aimed to explore the impact of deeper networks on image recognition. It features a simple and uniform architecture with 16 or 19 layers. VGGNet employed a stack of 3x3 convolutional layers with a stride of 1 and 2x2 max pooling layers with a stride of 2. The repeated small filters were effective in capturing complex patterns. VGGNet also employed the ReLU activation function, followed by fully connected layers. However, its depth made it computationally expensive and required a significant amount of memory.

Both architectures made significant contributions to the development of CNNs.
AlexNet's parallel processing and use of ReLU activation function set the stage for subsequent architectures. VGGNet, on the other hand, demonstrated the importance of deeper networks in improving accuracy, although at the cost of increased complexity.
These models were pivotal in advancing the field of deep learning and laid the foundation for subsequent state-of-the-art CNN architectures.

### 2. Explore different activation functions. What are the pros and cons of each activation function?

**Ans**: Activation functions are an essential part of neural nets for they introduce non-linearities to the net, enabling it to learn complex patterns and make better predictions. 

#### Sigmoid :

##### Pros:
1. Output range [0 to 1].
2. Continuously differentiable, helps for gradient-based optimization.
3. Used in the hidden layers of shallow nets.
##### Cons:
1. Vanishing gradients problem.
2. Outputs are not zero-centered, which can slow down convergence in certain scenarios.
3. Computationally expensive.

#### Tanh :
#####   Pros:
1. Output ranges [-1 to 1].
2. Non-linear & continuously differentiable.
##### Cons:
1. Vanishing gradients problem.

#### Rectified Linear Unit (ReLU):

##### Pros:
1. Simple and computationally efficient.
2. Faster convergence during training. Hence it avoids the vanishing gradient problem.
##### Cons:
1. Not zero-centered, which may hinder convergence in certain scenarios.
2. "Dying ReLU" problem: Neurons can become permanently inactive during training if it consistently outputs zero.

#### Leaky ReLU:

##### Pros:
1. Overcomes the "dying ReLU" problem by introducing a small slope for negative values, allowing gradients to flow even for negative inputs.
2. Same Advantages as ReLU
##### Cons:
1. Still not zero-centered, which may affect convergence problem.
2. Introduces another hyperparameter (slope for negative part).



### 3. Explain in detail Vanishing and Exploding gradient problems.           

**Ans**:

##### Vanishing  Gradient

The vanishing gradient problem is a difficulty encountered in training deep neural networks. It occurs when the gradients of the loss function with respect to the parameters of the network become extremely small as they propagate backward from the final layers to the initial layers. This is because the gradients are multiplied by the weights of each layer during the chain rule, and if these weight multipliers are less than 1, the gradients can exponentially decrease as they propagate through layers. As a result, the weights in the early layers of the network receive tiny updates, and their learning can be significantly slower compared to the later layers.

The vanishing gradient problem can cause the network to struggle to learn long-term dependencies, as the gradients representing these dependencies diminish rapidly over time. This issue is especially pronounced in tasks such as natural language processing, where context dependencies often span long sequences.

There are a number of techniques that can be used to mitigate the vanishing gradient problem, such as using activation functions with larger gradients, initializing the weights of the network carefully, and using regularization techniques.

##### Exploding Gradient

The exploding gradient problem is a phenomenon that occurs during backpropagation in deep neural networks. It is caused by the multiplication of large weights with gradients, which can lead to exponentially increasing gradients. This can make the network unstable and prevent it from learning effectively.

There are a number of techniques that can be used to mitigate the exploding gradient problem, such as gradient clipping, adaptive learning rates, and normalization. These techniques can help to stabilize the learning process and prevent the gradients from becoming too large.

The exploding gradient problem is a serious issue that can prevent deep neural networks from learning effectively. However, there are a number of techniques that can be used to mitigate this problem. By using these techniques, it is possible to train deep neural networks that are both accurate and stable.

### 4. Why are NN with skip connections known as Residual networks?

**Ans**:

Residual networks (ResNets) are a type of neural network that uses skip connections to address the vanishing gradient problem. The vanishing gradient problem occurs when the gradient signal becomes very small as it propagates through the network, making it difficult for the network to learn.

Skip connections allow information from earlier layers to be directly propagated to deeper layers, bypassing some of the intermediate layers. This helps to keep the gradient signal from becoming too small and allows the network to learn more effectively.

The core idea behind ResNets is that instead of directly learning the mapping between the input and the desired output, the network learns the residual mapping. The residual mapping is the difference between the input and the desired output. This residual mapping is easier for the network to learn and optimize.

ResNets have been shown to be very effective for training deep neural networks. They have achieved state-of-the-art results on a variety of tasks, including image classification, object detection, and natural language processing.



### 5. Understand the Resnet and Inception architectures?

**Ans**:

##### ResNet
ResNet (Residual Network) is a deep convolutional neural network architecture that addresses the vanishing gradient problem by introducing residual connections or skip connections. These connections allow information from earlier layers to bypass several layers and directly reach deeper layers, making it easier for the network to learn and propagate gradients.

The main building blocks of ResNet are residual blocks, which consist of a series of convolutional layers followed by batch normalization and rectified linear unit (ReLU) activation functions. The key feature of a residual block is the skip connection that adds the original input to the output of the convolutional layers. This allows the network to learn residual functions, i.e., the differences between the desired output and the input features.

ResNet is typically composed of multiple stacked residual blocks, which allow the network to learn more complex representations as the depth increases. Deeper variants of ResNet have achieved state-of-the-art performance in various computer vision tasks, including image classification, object detection, and semantic segmentation.

##### Inception

The Inception architecture is a deep convolutional neural network architecture that was developed by researchers at Google. It addresses the limitations of computational efficiency and representational power of previous architectures by using Inception modules and dimensionality reduction.

An Inception module consists of multiple parallel convolutional layers of different filter sizes (e.g., 1x1, 3x3, 5x5) and a max-pooling layer. This allows the network to capture multi-scale features at different levels of abstraction.

Dimensionality reduction is used to reduce the number of channels in the network to reduce computational complexity. This is done using 1x1 convolutions before applying larger convolutions. The 1x1 convolutions perform a linear transformation on the input channels, allowing the network to reduce the number of parameters.

Inception networks typically have several stacked Inception modules, which are connected by intermediate layers and topped with a global average pooling layer and a softmax layer for classification. Variants of the Inception architecture, such as InceptionV2, InceptionV3, and InceptionV4, have achieved high accuracy in image classification tasks while being computationally efficient.


### 6. Write a Residual Network  in PyTorch?

**Ans**:

* ResNet + MNIST with PyTorch: [Notebook](./resnet-mnist.ipynb)
* ResNet + MNIST with Fast.ai: [Notebook](./fastai-resnet34.ipynb)