# Glossary
This is a glossary of the common terms in ML picked up from the various articles and blog posts.

A

attention function - described as mapping a query and a set of key-value pairs to an output, where query, keys, values and output are all vectors. The output is computed as a weighted sum of the values, where the weight assigned to each value is computed by a compatibility function to the query with the corresponding key (Vaswani et al. 2017)

M

multi-head attention - concatenates a values of multiple single attention functions. It allows the model to joinly attend to information from different representation subspaces at different positions.

S

self-attention - attention mechanism relating different positions of a single sequence in order to compute a representation of the sequence (Vaswani et al. 2017)


