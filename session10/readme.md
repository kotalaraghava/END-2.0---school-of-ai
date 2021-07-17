## Assignment code changes:
1. changed flag to the 'readLangs' functions to reverse the translation from eng to fra
2. Added code to load pre-trained glove embeddings of 50d as a weighted_matrix


## Training Loss comparision: 

training loss without adding embedding : 

![](https://github.com/kotalaraghava/END-2.0---school-of-ai/blob/master/session10/seqToSeqWithoutEmbedding.png)




training loss with embeddings:

![](https://github.com/kotalaraghava/END-2.0---school-of-ai/blob/master/session10/seqToSeqWithEmbeddings.png)




as we see training loss is 50% high compared to without embeddings following might be the reasons:
1. since we are filtering training samples with defined texts like (me, i , he she) the vector representation
   for these words might not having much context included.
2. on the fly running of embeddings may be contributing more since very less data is present.

ways to increase the accuracy:
1. add embeddings for both languages
2. try different attention machanisims.
3. add all the training samples while training without filtering.


## Teacher forcing : 
Teacher forcing is a strategy for training neural networks that usues ground truth as input, instead of model
output from previous time input.

This teacher forcing will be used for model which has recurrent connections leading back into the model by feeding 
ground truth for previous time input.






## Encoder & Decoder in translation with attention:

Encoder is used for encoding the meaning of the entire sentence in terms of context vector, decoder uses the context vector to translate to target languge.

attention: Most articles on the Attention Mechanism will use the example of sequence-to-sequence (seq2seq) models to explain how it works. This is because Attention was originally introduced as a solution to address the main issue surrounding seq2seq models, and to great success. If you are unfamiliar with seq2seq models, also known as the Encoder-Decoder model, I recommend having a read through this article to get you up to speed.
