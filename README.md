# Cat-Recognition-using-Deep-neural-Network
This project is an example of building and train a deep L-layer neural network, and applying it to supervised learning. It consists of a 4 layers neural network that predict whether the image is of a cat or not. 

## Dataset:
The dataset is a "Cat vs non-Cat" dataset of images labelled as cat (1) or non-cat (0), a test set of images labelled as cat and non-cat and each image is of shape (num_px, num_px, 3) where 3 is for the 3 channels (RGB). As usual, we first reshape and standardize the images before feeding them to the network. Standardization is a scaling technique where the values are centered around the mean with a unit standard deviation. This means that the mean of the attribute becomes zero and the resultant distribution has a unit standard deviation. 
![Reshape cat images](/images/reshape.png)
The dataset consists of:
* Number of training examples: 209
* Number of testing examples: 50
* Image of size: (64, 64, 3)
* train_x_orig shape: (209, 64, 64, 3)
* train_y shape: (1, 209)
* test_x_orig shape: (50, 64, 64, 3)
* test_y shape: (1, 50)

## Model Architecture: 
To build your neural network, you'll be implementing several "helper functions" from [function.py](https://github.com/shreeyalotankar/Cat-Recognition-using-Deep-neural-Network/blob/main/functions.py).
Here is an outline of the model used in this project:
* Initialize the parameters for an  𝐿 -layer neural network
* Implement the forward propagation module (shown in purple in the figure below)
  * Complete the LINEAR part of a layer's forward propagation step (resulting in  𝑍[𝑙] ).
  * The ACTIVATION function is provided for you (relu/sigmoid)
  * Combine the previous two steps into a new [LINEAR->ACTIVATION] forward function.
  * Stack the [LINEAR->RELU] forward function L-1 time (for layers 1 through L-1) and add a [LINEAR->SIGMOID] at the end (for the final layer  𝐿 ). This gives you a new L_model_forward function.
* Compute the loss
* Implement the backward propagation module (denoted in red in the figure below)
* Complete the LINEAR part of a layer's backward propagation step
  * The gradient of the ACTIVATE function is provided for you(relu_backward/sigmoid_backward)
  * Combine the previous two steps into a new [LINEAR->ACTIVATION] backward function
  * Stack [LINEAR->RELU] backward L-1 times and add [LINEAR->SIGMOID] backward in a new L_model_backward function
* Finally, update the parameters.

![Image of outline](/images/outline.png)

[Function.py](https://github.com/shreeyalotankar/Cat-Recognition-using-Deep-neural-Network/blob/main/functions.py) has the above mentioned fucntions which are then used to train a 4-layer model having layer dimensions **12288, 20, 7, 5, 1**.

![Image of Cat architecture](/images/outlin2.png)

## Accuracy:
The accuracy of this model on training data is 98.56% while on test data it is 80%. As this dataset has a insufficient images the accuracy is low you can increase the accuracy by using more examples or by training a deep network (more number of layers).

## References and Credit:
**[Neural Network and Deep Learning](https://www.coursera.org/learn/neural-networks-deep-learning), Andrew N.G**





