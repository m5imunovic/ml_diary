# 2021-03-13

Notes from todays learning:
I think I finally understand the architecture of the graphs. What we are trying to do is good
learning function for processing the information from the neighboring nodes. Message function
actually operates on each edge connected to a specific node. Reduce function then combines all
these partial information in a single one relevant for that particular node. Therefore, if we
want to include information from the node we can artificially add the self-loop (even though
there is no edge in the input graph). Then we operate with this same message-reduce protocol
for each node. What happens is that by repeated applications the information propagates to
the more distant nodes. Each node becomes aware of the N-neighborhoud after the N steps of
GNN execution.

- Wrap up the data processing step
-- The data needs to contain the original graph, intermediate states of the nodes and path
   through which the graph was explored (indices of the graph nodes)
-- Padding is done in such a way that the training algorithm executes the whole graph - therefore
   even though the graph is explored earlier due to missing connections neural network still 
   needs to "understand" that there is nothing to be done considering there are more nodes than 
   steps
-- Create a basic model for prediction with message passing (does not need to be any specific
   paper implementation but should work good with the given data, i.e. make parameter sizes 
   consistent)
