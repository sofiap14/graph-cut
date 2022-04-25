sofiap1, Sofia Panuganti

Texture Synthesis: Implementation of a graph cut algorithm to generate a texture from a smaller sample image, or patch, according to the paper: Graphcut Textures: Image and Video Synthesis Using Graph Cuts. 

The general idea of the implementation is building a graph whose vertices are overlapping regions of pixels, edges are created between neighbors and additional Source and Sink nodes are also created. The pixels close to the patch are linked with the source, and the pixels close to the texture are linked with the sink. A min-cut is computed in this graph. The output is the copy of pixels belonging to the source (left) part of the graph. 

I used a max-flow/min-cut algorithm Ford Fulkerson and BFS find augmenting paths and calculate maximum flow for the original graph using the residual graph.

Results: 

