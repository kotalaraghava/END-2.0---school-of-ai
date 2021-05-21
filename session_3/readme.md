
## data preparation & data : 

used dataloader from pytorch and in that injected random variable as a input int he __getitem__ along with random 
traget which is sum of random_input + label

we didn't do one-hot encoding because its numeric variable and don't want to complicate the things.

## combined two inputs :

took a argmax of image output and stacked with random input number and passed onto further feed forward layers.


## evaluating results : 
we made test loader using the same stratagy as the train data loder and doing evaluation on it.


## loss function : 

for image classification we were using cross-entropy loss as its a classification task & mse loss for random_ouput evaluation as its numeric variable.

and combined loss is propagated back to update the weights.


## GitHub Link : 
https://github.com/kotalaraghava/END-2.0---school-of-ai/blob/master/session_3/MNSIT_Model.ipynb
