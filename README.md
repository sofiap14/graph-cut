sofiap1, Sofia Panuganti

## Texture Synthesis:

Implementation of a graph cut algorithm to generate a texture from a smaller sample image, or patch, according to the paper: Graphcut Textures: Image and Video Synthesis Using Graph Cuts. 

The general idea of the implementation is building a graph whose vertices are overlapping regions of pixels, edges are created between neighbors and additional Source and Sink nodes are also created. The pixels close to the patch are linked with the source, and the pixels close to the texture are linked with the sink. A min-cut is computed in this graph. The output is the copy of pixels belonging to the source (left) part of the graph. 

I used a max-flow/min-cut algorithm Ford Fulkerson and BFS find augmenting paths and calculate maximum flow for the original graph using the residual graph.

Submitted as an .ipynb file

## Results

![test](https://user-images.githubusercontent.com/91835033/165178132-f80948c1-703c-4de4-88e4-6acae5e3dfc9.png)

![test_output](https://user-images.githubusercontent.com/91835033/165178134-846f1563-ea5d-419a-ac48-fe38051aa280.png)

The resulting texture (to the right) is synthesized at twice the size of the original image (to the left).  

![test2](https://user-images.githubusercontent.com/91835033/165178135-8e4bcb3f-6f48-4158-8061-d56e2bb29e91.png)

![test2_output](https://user-images.githubusercontent.com/91835033/165178136-6b164c43-9401-48b1-b6a2-815a7ac9fc37.png)

## Resources:
https://brilliant.org/wiki/ford-fulkerson-algorithm/

https://www.youtube.com/watch?v=GoVjOT30xwo

Kwatra, Vivek, et al. “Graphcut Textures.” ACM Transactions on Graphics, vol. 22, no. 3, 2003, pp. 277–86. Crossref, https://doi.org/10.1145/882262.882264.


