# Attention is all you need

> Attention mechanisms have become an integral part of compelling sequence modeling and transduction models 
> in various tasks, allowing modeling of dependencies without regard to their distance in the input or output 
> sequences [2, 18].

> Self-attention, sometimes called intra-attention is an attention mechanism relating different positions of 
> a single sequence in order to compute a representation of the sequence.

> An attention function can be described as mapping a query and a set of key-value pairs to an output, where
> the query, keys, values, and output are all vectors.

> The output is computed as a weighted sum of the values, where the weight assigned to each value is computed
> by a compatibility function of the query with the corresponding key.

* They are really using dot product attention, just like we did in the local genome hashing experiments softmax(<k, q>).
However, they add some normalization.

> We suspect that for large values of dk, the dot products grow large in magnitude, pushing the softmax function 
into regions where it has extremely small gradients 4. (so that's why they use scaling)

> In this work, we presented the Transformer, the first sequence transduction model based entirely on attention, 
> replacing the recurrent layers most commonly used in encoder-decoder architectures with multi-headed self-attention.
