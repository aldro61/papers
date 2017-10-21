# Paper reading sprints


I browser through a bunch a papers, taking a maximum of 5 minutes (using a timer) to extract the general ideas and findings. Then, if the paper seems relevant, I read the details at another time. For most papers, I just want an overview to keep track of the latest improvements in the fields. I think that this strategy will allow me to be better informed and reduce the number of tabs that are open in my Chrome Browser, while not being too time consuming.


## October 21, 2017

### PHYLOViZ 2.0: providing scalable data integration and visualization for multiple phylogenetic inference methods

* Platform independent java tool for phylogenetic visualization

* Works on bacterial data

* Can generate figures for use in papers

* Handles large datasets (many samples and loci)

* Does phylo inference (i.e., tree building) with NJ and clustering algorithms.

* Tutorials http://www.phyloviz.net/tutorials.html

* Documentation: http://phyloviz.readthedocs.org/



### PyBoolNet: a python package for the generation, analysis and visualization of boolean networks

* Python package to handle boolean networks

* Generation and manipulation of networks, attractor and basin computation, model checking and trap space computation, execution of established graph algorithms as well as graph drawing and layouts.

* In cell biology boolean networks are used to model gene regulatory and signal transduction networks (and more)



### stringMLST: a fast k-mer based tool for multilocus sequence typing

* Multi-locus sequence typing (MLST): Rapid and accurate identification of the sequence type (ST) of bacterial pathogens by looking at short pieces taken from many parts of their genome.

* Pros: assembly and alignment-free, lightweight, platform-independent, fast

* Works on raw sequence reads

* Implements a simple hash table data structure to find exact matches between short sequence strings (k-mers) and an MLST allele library

* Code: http://jordan.biology.gatech.edu/page/software/stringMLST

* User can define his own typing schemes (e.g.: amikacin resistant clostridium difficile), although I doubt that this works better than a classifier based on k-mers.

* They have used types obtained from this method to reconstruct phylogenies with the same accuracy as whole genome MLST. Not sure if this works better than whole genome or if it is just faster and OK accurate.



### DOMINO: development of informative molecular markers for phylogenetic and genome-wide population genetic studies in non-model organisms

* It is well known that phylogenetic inferences based on a single or very few genetic markers can lead to systematic errors and reach invalid conclusions (Brito and Edwards, 2009; Maddison et al., 1997).

* New bioinformatics tool that facilitates the development of highly informative markers from different data sources

* Basically, it is a tool that discovers markers that are useful for phylogenetic inference.



### Convolutional neural networks for structured omics: OmicsCNN and the OmicsConv layer

* They propose a convolutional layer that can be applied to omics data

* Conv layers cannot generally be applied to this type of data since there is no definition of proximity (unlike in images, videos, graphs, etc.)

* Need to embed omics data in a metric space

* Metric for metagenomics data: OTU counts -> distance between counts is the distance in the phylo tree

* Interesting idea, so many details missing. The first application of their "convolution" makes sense, since the distance is given by the tree. However, past the first layer, the mapping into a k-dimensional space is unclear and I don't get it.

* Even if this method allows to take into consideration the proximity between features, why would that be relevant for prediction. For instance, if I know that some pattern of closely related OTUs are present in the input, this is not necessarily relevant. In such a case, a simple MLP would be more appropriate.

* Looking forward to reading about the details of this idea.



### Self-Normalizing Neural Networks (NIPS 2017)

* While batch normalization requires explicit normalization, neuron activations of SNNs automatically converge towards zero mean and unit variance.

* The activation function of SNNs are “scaled exponential linear units” (SELUs), which induce self-normalizing properties.

This convergence property of SNNs allows to (1) train deep networks with many layers, (2) employ strong regularization schemes, and (3) to make learning highly robust.

* We prove an upper and lower bound on the variance (of the gradient), thus, vanishing and exploding gradients are impossible

* Interesting, should read the details.



### The inconvenience of data of convenience: computational research beyond post-mortem analyses

Stop collecting data and analyzing it a posteriori. Model/hypothesis-driven data generation is the way to go and the authors report a DREAM challenge that is putting this idea to the test.
