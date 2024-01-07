# Feedforward-Neural-Network

### Aim: Build a Feedforward Neural Network Image Classifier. 

In the first part, I built a feedforward neural network from the ground up leveraging on the skeleton code provided in Andrej Karpathy's micrograd project. The most fundamental component of the neural network is the Value class that stores a single scalar value and its corresponding gradient with respect to the loss function. Methods such as add, multiply, log, exponent and ReLU are created to perform numerical operations on the scalar value in the forward propagation, as well as calculation of its gradient using chain rule during backpropagation. Then, I constructed the Neuron, Layer, and Perceptron classes, each building upon the other to establish the entire neural network architecture. 

The weighted sum of all input neurons are calculated first, before the ReLU activation function is applied to the weighted sum to introduce non-linearity to the model. In the final layer, the softmax function is used to derive probabilities for each output value, indicating the likelihood of the input image belonging to respective categories. To evaluate the model's accuracy, the deviation of the predicted output from its true value is calculated using the cross-entropy loss function. Finally, the model undergoes backpropagation to adjust the weights and biases of each neuron to minimize loss, and therefore increase the model's accuracy.

In the second part, I implemented the same neural network with stochastic gradient descent using built-in functions from the PyTorch library. Here are the accuracies of my model implemented in PyTorch when tested on the Iris and MNIST datasets:

## Model Accuracy
| Dataset | Accuracy |
| :---: | :---: |
| Iris | 0.9667 |
| MNIST | 0.9507 |
