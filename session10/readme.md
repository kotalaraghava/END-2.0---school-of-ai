## Assignment code changes:
1. changed flag to the 'readLangs' functions to reverse the translation from eng to fra
2. Added code to load pre-trained glove embeddings of 50d as a weighted_matrix


## Training Loss comparision: 

training loss without adding embedding : 
![](





## Teacher forcing : 
Teacher forcing is a strategy for training neural networks that usues ground truth as input, instead of model
output from previous time input.

This teacher forcing will be used for model which has recurrent connections leading back into the model by feeding 
ground truth for previous time input.






## Encoder & Decoder in translation with attention:

Encoder is used for encoding the meaning of the entire sentence in terms of context vector, decoder uses the context
vector to translate to target languge.






