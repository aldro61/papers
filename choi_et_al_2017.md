# Coarse-to-Fine Question Answering for Long Documents

* Inspiration: how a reader skims through a document and only reads important parts in details to answer a question.

* The idea is to identify relevant pieces of a document using a coarse representation and then to detect detailed patterns using a fine representation.

* The selection of relevant pieces of text is treated as a latent variable, so it must be learned.

* The method jointly optmizes sentence selection and answer generation

* Sentence selection: p(s | x, d), where x is a question and d is a document. This is given by an attention model.

* Answer generation: p(y | x, ^d), where ^d is the learned document summary.

* In the attention model, they use the concatenated representations of a sentence and the query and then apply transformation ending with a softmax to get the probability.

Points to:
* Multi-level structured models for document- level sentiment classification.
* Rationalizing neural predictions (The one Dima suggested)
* Zichao Yang, Diyi Yang, Chris Dyer, Xiaodong He, Alex Smola, and Eduard Hovy. 2016b. Hierarchical attention networks for document classification.
