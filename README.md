# Cat-Recognition-using-Deep-neural-Network
This project is an example of building and train a deep L-layer neural network, and applying it to supervised learning consists of a 4 layers neural network that predict whether the image is of a cat or not. 

##Dataset:
The dataset is a "Cat vs non-Cat" dataset. This dataset contains a training set of `m_train` images labelled as cat (1) or non-cat (0), a test set of `m_test` images labelled as cat and non-cat and each image is of shape (num_px, num_px, 3) where 3 is for the 3 channels (RGB). As usual, we first reshape and standardize the images before feeding them to the network. Standardization is a scaling technique where the values are centered around the mean with a unit standard deviation. This means that the mean of the attribute becomes zero and the resultant distribution has a unit standard deviation. The train-set consists of 209 training examples while the test set consists of 50 testing examples each of dimension 64×64×3 , which is the size of one reshaped image vector.

##Model Architecture: (functions.py)
To build your neural network, you'll be implementing several "helper functions" which are given in [functions.py](https://github.com/shreeyalotankar/Cat-Recognition-using-Deep-neural-Network/blob/main/functions.py) These helper functions will be used in the next assignment to build a two-layer neural network and an L-layer neural network.
The initialization for a deeper L-layer neural network is more complicated because there are many weight matrices and bias vectors. When completing the initializing the parameters, you should make sure that your dimensions match between each layer.


