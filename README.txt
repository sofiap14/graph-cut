sofiap1, Sofia Panuganti

Texture Synthesis: Implementation of a graph cut algorithm to generate a texture from a smaller sample image, or patch, according to the paper: Graphcut Textures: Image and Video Synthesis Using Graph Cuts. 

The general idea of the implementation is building a graph whose vertices are overlapping regions of pixels, edges are created between neighbors and additional Source and Sink nodes are also created. The pixels close to the patch are linked with the source, and the pixels close to the texture are linked with the sink. A min-cut is computed in this graph. The output is the copy of pixels belonging to the source (left) part of the graph. 

I used a max-flow/min-cut algorithm Ford Fulkerson and BFS find augmenting paths and calculate maximum flow for the original graph using the residual graph.

Results: 

![test](https://user-images.githubusercontent.com/91835033/165175348-4ade7049-f7e7-4ebd-8848-d395d58096c8.png) --> ![test_output](https://user-images.githubusercontent.com/91835033/165175347-6d417349-d786-454c-8d25-afccc0d6e1ce.png)

![test2](https://user-images.githubusercontent.com/91835033/165175362-98c0752f-977b-4b71-a555-cad0d14034fe.png) --> ![test2_output](https://user-images.githubusercontent.com/91835033/165175361-461c0391-8cc3-4671-a3e0-c0b896b233c4.png)
