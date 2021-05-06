# Assignment:

## What is a neural network neuron?

Neural network neurons are similar to the biological neurons where they take an input, act on the input with an activation fuction and gives us an output. A single neuron will look as shown below.

![Neuron](https://github.com/ganeshkcs/END2/blob/master/S1/Neuron.png)

Collection of such neurons and their interactions will form a neural network.

![Neural-Network](https://github.com/ganeshkcs/END2/blob/master/S1/Neural-network.png)

## What is the use of learning rate?

We know that at the end of forward propagation in neural network there would be difference between the actual value and the predicted value, this difference, between actual and predicted value is called as Loss/Error/Cost. To reduce the loss we need to update the weights and biases and this process is achieved by back propagation where based on the loss, the weights and biases that comes as input ( from previous hidden layer ) to the output layer is updated, similarly all the other layers ( except the layer 1 or the input layer ) are also updated. 
                   
 If we plot a graph between the weight and cost ( Y axis ) as shown below 
 
 ![LR](https://github.com/ganeshkcs/END2/blob/master/S1/lr_different_ones.png)

 We can infer that to achieve the minimum point in the graph we should know two things
 
 1. In which direction we should move
 2. How much we should move ( Learning Rate )

 So we should always update the weights such that it moves towards the minimum loss, which is given by the below equation.
 
 new_weight = existing_weight — learning_rate * gradient
 
Learning rate is a hyper-parameter that controls how much we are adjusting the weights of our network with respect the loss gradient. The lower the value, the   slower we travel along the downward slope.
 
Typically learning rates are configured naively at random by the user. At best, the user would leverage on past experiences (or other types of learning material) to gain the intuition on what is the best value to use in setting learning rates.

## How are weights initialized?

To understand the initialization weights we will go through the below cases.

**When weights are initialized to Zero:**

If the weights are set to 0 then the derivative with respect to loss is same for all the weights and makes the hidden units symmetric and continueos for all the iterations, which will result getting the same output.

**When weights are initialized randomly:**

When the weights are initialized randomly which follows a normal distribution, we should ensure that the weights are not too high and too low. If we initialize large weights, the activation will be large, resulting in zero slope (in case of sigmoid and tanh activation function). Hence, learning will be slow. If the weights are intialized with very low values, it gets mapped to 0 and we will face the problem as discussed above, this is called as Vanishing Gradient Problem. So we generally multipy the randomly intialized weights with a constant ( say 0.01) so that it is not too large and low.


## What is 'Loss' in a neural network?

Loss is prediction of error in a Neural Network and the method to calculate the loss is called Loss Function.

There are various Loss functions, the most common ones are shown below.

**Mean Sqaured Error:**

MSE loss is used for regression tasks. As the name suggests, this loss is calculated by taking the mean of squared differences between actual(target) and predicted values.

**Binary Crossentropy:**

BCE loss is used for the binary classification tasks. If you are using BCE loss function, you just need one output node to classify the data into two classes. The output value should be passed through a sigmoid activation function and the range of output is (0 – 1).

 **Categorical Crossentropy:**
 
When we have a multi-class classification task, one of the loss function you can go ahead is this one. If you are using CCE loss function, there must be the same number of output nodes as the classes. And the final layer output should be passed through a softmax activation so that each node output a probability value between (0–1).

## What is the "chain rule" in gradient flow?

According to Chain rule if a variable z depends on the variable y, which itself depends on the variable x, so that y and z are dependent variables, then z, via the intermediate variable of y, depends on x as well.

![CR](https://github.com/ganeshkcs/END2/blob/master/S1/chain-rule.png)

So in terms of neural network

![BP](https://github.com/ganeshkcs/END2/blob/master/S1/BP.png)

We back propagate to reduce the loss, so to minimise the loss the weights are adjusted from the output layer, so the output layer is dependent on the prevevious layer output, similarly all the layers output are dependent on their previous layer outputs, this is called chain rule in neural networks.

## Neural Network:

Rewrite the Colab file and:

* remove the last activation function
* make sure there are in total 44 parameters
* run it for 2001 epochs

Link to the file https://github.com/ganeshkcs/END2/blob/master/S1/END2_0_Session_1.ipynb


 



