
## data preparation & data : 

used dataloader from pytorch and in that injected random variable as a input int he __getitem__ along with random 
traget which is sum of random_input + label

we didn't do one-hot encoding because its numeric variable and don't want to complicate the things.

## combined two inputs :

took a argmax of image output 


## evaluating results : 
we made test loader using the same stratagy as the train data loder and doing evaluation on it.


## loss function : 

for image classification we were using cross-entropy loss & mse loss for random_ouput evaluation.

and combined loss is propagated back to update the weights.

