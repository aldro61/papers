# Classification and regression trees

## Interpretation

> Another difficulty in tree structured classification is that the simple structure of the final 
classification tree can be deceptive

> If a variable is never split on in the final tree, one interpretation might be that the variable has very little association
with class membership. The truth may be that its effect was masked by other variables.

> Tree structures may be unstable

* They provide methods for ranking variables in chap 5

* Advantages of tree methods is discussed in section 2.7

* The best way to compute variable importance is to consider surrogate splits, which also gives the importance of rules that are not used by the tree, based on their correlation with the rules used to split.
