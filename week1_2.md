## Temporally Coherent Local Tone Mapping of HDR Video
Focus / Aim: to reduce the dynamic range of HDR content while (1) maintaining a high level of local contrast and (2) reducing temporal and halo artifacts
Context: local tone mapping method often suffer from halo artifacts that appear near strong image edges
### Problems
- produce temporal artifacts
- 

### Methods
Decomposing each frame into a base and detail layer
```
base layer
- edge-aware spatiotemporal filtering
- components: cental frame, temporal neighbors 

detail layer
- temporal filtering
```
Recipes:
1. Obtain temporal neighbor frames: +/-10 frames
2. Edge-aware Spatial filtering with permeability map
- used to prevent filtering across strong image edges
- iterative application of shift-variant spatial filter
3. Warping
- used to align the pixels
- method: forward and backward optical flow
4. Temporal filtering with flow confidence map

compared with WLS filter: this method uses a larger diffusion range controlled by permeability weights, which results in fast convergence

#### video tone mapping problems
Two trade-off:
- fine and coarse scale contrast 
- spatial and temporal contrast

### Pros & Cons
#### Pros:
- user adjustable scale (control)
  - offline pre-computation of the base and detail layers
  - explicit control over the tone mapping parameters and temporal contrast 
  
- paralelizable, fast (generate visually similar results to WLS filter with a small number of iteration)
- general ?
    1. other tone curves can be easily integrated to our method
    2. can be easily extended to perform temporal filtering
- can be applied to low light sequences with fewer camera noises

#### Cons:
  - number of neighbor frames is chosen empirically
  - only support single detail layer (while multiple detail layers are needed at different contrast scales)
  - Susceptible to visual artifacts due to the errors and limits of the optical flow 

### Contributions / Insights
- A temporally coherent and local video tone mapping method than can maintain a high level of local contrast 
with fewer temporal artifacts
- spatial-temporal filtering
  - specially designed for tone mapping
  - reduce halo artifacts by approximating a global solution


### My Questions
1. Don't quite understand the two trade-offs in video tone mapping..
2. Why not consider global tone mapping?
3. What does it mean by "use forward and backward optical flow estimates to warp each frame's temporal neighbor" ?
4. How to compute the spatial permeability map? What is the intuition behind "diffusion length" and "permeability weight"in spatial filtering ?
5. What 


### Feedback and advice on the presentation 
- pay attention to the logic of introducing new topics
- show images bigger 
- Do not cover too much information/math in one slide, try to control the attention of the audience
- Do not go into deep details for the mth
- add citations 
