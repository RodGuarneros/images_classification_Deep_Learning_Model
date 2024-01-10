# Traffic signs: The use of Convolutional Neural Networks (CNN)
Predicting the class of traffic signs based on a deep learning classifier.
Traffic sign classification for self-driving cars.

The CNN used here is known as LeNet (A convolutional neural network).

The dataset contains 43 different classes of signs.

What is amazing is the accuracy shown by the model (almost 0.99). The F1 score is also very high: 0.98.

Having in mind the architecture of convolutional linear neural networks. The elements are simple: 

## KERNEL (Feature detector)
A great explanation regarding **Kernel** as a feature detector in image processing is available at Victor Powell's site: https://setosa.io/ev/image-kernels/ 

## RELU
In this case, the Rectified Linear Unit Activation Functions are used to add non-linearity to the feature map. It, also, enhances the sparsity or how scattered the feature map is.

The gradient of the RELU does not vanish as we increase x compared to the sigmoid function.

## Pooling (Downsampling)
Those are placed after convolutional layers to reduce feature map dimensionality. The pooling process improves computational efficiency while preserving the features. Also, it helps the model to generalize by avoiding overfitting: If one of the pixel is shifted, the pooled feature will still be the same. 

Max pooling works, for instance, by retaining the maximum feature response within a given sample size in a feature map. 

![](https://production-media.paperswithcode.com/methods/MaxpoolSample2.png)

If you want to play with CNN in 2D and 3D, please visit the Harley's website: [https://adamharley.com/nn_vis/mlp/2d.html](https://adamharley.com/nn_vis/). An interactive node-link visualization of Convolutional Neural Networks.

# Increase filters or drop out

- Improve accuracy by adding more feature detectors/filters or adding dropouts.
- Dropout refers to dropping out units in a neural network.
- Neurons develop co-dependency amongst each other during training.
- Dropout is a regularization technique for reducing overfitting in neural networks.
- It enables training to occur on several architectures of the neural network.

## Convolutional Neural Network Achitecture (LENET)

STEP 0: 

- Input

STEP 1, la primera capa convolucional - LAYER #1: 

- Input = 32x32x1
- Output = 28x28x6
- Output = (Input-filter+1)/Stride* => (32-5+1)/1 = 28
- Used a 5x5 Filter with input depth of 3 and output depth of 6
- Apply a RELU Activation function to the output
- pooling for input 28x28x6 and Output = 14x14x6

STEP 2, the second convolutional  - LAYER #2:

- Input = 14x14x6
- Output = 10x10x16
- Layer 2: Convolutional layer with output = 10x10x16
- Output = (input-filter +1)/strides => 10 = (14 - 5 + 1)/1
- Apply a RELU Activation function to the output
- Pooling with Input = 10x10x16 and Output = 5x5x16

STEP 3: Flattening the network

- Flatten the network with Input = 5x5x16 and Output = 400

STEP 4: Fully connected layer

- Layer 3 fully connected layer with input 400 and Output 120
- Apply RELU activation function to the output

STEP 5: Another fully connected layer

- Layer 4: Fully connected layer with input = 120 and Output = 84
- Apply a RELU Activation function to the output

STEP 6: 

- Layer 5: Fully connected layer with input = 84 and output = 43 (different classes)

## LENET NETWORK (Gradient-Based Learning Applied to Document Recognition)
### A creation by Yann LeCun, Léon Bottou, Yoshua Bengio, and Patric Haffner, 1998
![Here you can find the article](http://vision.stanford.edu/cs598_spring07/papers/Lecun98.pdf)









