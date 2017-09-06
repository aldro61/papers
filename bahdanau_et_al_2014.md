# Neural Machine Translation by Jointly Learning to Align and Translate

* In the encoder/decoder setting, the **encoder** is tasked with transforming the input sequence into a fixed length vector *c*.
 The **decoder** then starts from *c* and generates the words in the output sequence.

* The idea of this paper is that, instead of conditionning on all the previously generated words, the decoder uses a learned "alignment function" that produces a probability distribution on all the hidden states (one per input word) of the encoder and uses a weighted sum to compute a "context vector" *c_i*, which is later transformed into the output word by a neural net.

* The alignment function is basically a neural network that is trained to predict which pieces of the input sequence are relevant for predicting a specific word of the output sequence.
