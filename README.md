# grad_clip
Gradient clipping is a technique that is used to prevent explosive gradients that neural networks often encounter, especially in deep models.

### Why do you need gradient clipping?
This method is a process of limiting the magnitude of the gradient to avoid too many parameter updates during error back propagation.

This method is especially important in tasks related to the training of complex models, such as convolutional neural networks for image processing, where using a large number of layers can lead to learning problems. In recent years, gradient clipping has become an important tool in areas such as image processing, image generation, segmentation, and object detection.

### Setting the task
The goal of our project is to use gradient clipping to stabilize the learning of a convolutional neural network in an image classification task. We will use a popular dataset, for example, ImageNet-100, and try to train the model without gradient clipping and using it to show in practice how this method affects training and model performance.

<br>
<br>

#### <a name="NormClip"></a> Norm Clipping
Norm-clipping is a basic clipping method that uses a constant to clip gradient.
$$\alpha_{norm} = {\frac{\eta}{||\nabla f(x^k, \xi^k)||_2}}$$

-----------
<br>
<br>

#### <a name="LinearRandNormClip"></a> Linear Random Norm Clipping
LinearRandNormClip is a norm-clipping method using randomization when clipping gradient, which helps to shift the mathematical expectation less.
$$P(\text{clip})=\beta^{\alpha_{\text{norm}}}, \text{where}\ 0<\beta<1 \text{ and}\ \alpha = \alpha_{\text{norm}}$$

-----------
<br>

