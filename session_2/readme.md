## Back propagation : 
back propagation is a technique in which try to reduce the loss value (prediction - actuval) by adjusting the weights of the neural network using gradient descent algorithem.

The example network which we will be using is:
![image](https://github.com/kotalaraghava/END-2.0---school-of-ai/blob/master/session_2/network.png)

The main steps in training a neural networks as follows : 
### calculating predicted value (forward propagation):
given a neural netowork and inputs we calculate the what is that our network is predicting given a intial weights and biases, and then we calculate the total loss by subtracting from actuval value.

the below is the how total loss (E_total) looks like.

![image](https://github.com/kotalaraghava/END-2.0---school-of-ai/blob/master/session_2/forward_propagation.png)

### back propagation:
so back propagation is reduce the error by modifying weights in the neural network.
we figure out how much of weights needs to be updated by taking derivative of each weights with respect to total loss.
below is the derivatives of last four weights in the above network.
![image](https://github.com/kotalaraghava/END-2.0---school-of-ai/blob/master/session_2/last_4_weights.png)

similary derivatives of first four weights
![image](https://github.com/kotalaraghava/END-2.0---school-of-ai/blob/master/session_2/first4weights.png)

Then we subtract the each weights with new values with the maginitude of learning of rate.
like this we prepare for each of all weights in our network.

### loss reduction with learning rate.

we can see below how by variaing different learning rate the maginitude of weights updates changes so does the their effect on total loss.
![image](https://github.com/kotalaraghava/END-2.0---school-of-ai/blob/master/session_2/when%20learning%20rate%20is%200.1.png)
![image](https://github.com/kotalaraghava/END-2.0---school-of-ai/blob/master/session_2/when%20learning%20rate%20is%200.2.png)
![image](https://github.com/kotalaraghava/END-2.0---school-of-ai/blob/master/session_2/when%20learning%20rate%20is%200.5.png)
![image](https://github.com/kotalaraghava/END-2.0---school-of-ai/blob/master/session_2/when%20learning%20rate%20is%200.8.png)
![image](https://github.com/kotalaraghava/END-2.0---school-of-ai/blob/master/session_2/when%20learning%20rate%20is%201.png)
![image](https://github.com/kotalaraghava/END-2.0---school-of-ai/blob/master/session_2/when%20learning%20rate%20is%202.png)



at the end we choose the ones which gives us the best optimal parameters.

# Links:
XLS : https://github.com/kotalaraghava/END-2.0---school-of-ai/blob/master/session_2/BackPropagation.ods
