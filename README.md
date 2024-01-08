# Traffic signs: The use of Convolutional Neural Networks (CNN)
Predicting the class of traffic signs based on a deep learning classifier.
Traffic sign classification for self-driving cars.

The CNN used here is known as LeNet (A convolutional neural network).

The dataset contains 43 different classes of signs.



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



