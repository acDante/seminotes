## Video Propogation Network
Focus: propagating structured information across video frames
1. Video Object Segmentation: focus on semi-supervised task of propagating foreground mask from the first frame to the entire video
Challenge: scene/camera motion and its effect on the output foreground mask
our Solution: adapt the connectivity of bilateral network to video sequences 

Applications: semantic segmentation; depth estimation

### Inspiration
```
- Fast Bilateral Upsampling across Frames
The bilateral filtering operation can be viewed as a computation in a higher dimensional space

- Learnable Bilateral Filter
The generalized permutohedral lattice filter can be learned via back-propagation
```

### Methods
This method combines two components:
- temporal bilateral network 
  - perform image-adaptive spatio-temporal dense filtering
  - connect densely pixelwise to propagate pixel information across frames
  - can define a metric between pixels
```
Why bilateral network ?

```
- spatial CNN 
  - refine the information 
> Three steps in Bilateral Convolution Layer(BCL)
> 1. splating: map into permutohedral lattice space
> 2. convolving: bilateral filtering (parameters learned by back propagation)
> 3. slicing: map back to input space

### Related Work 
### Previous Works & their contribution
optimization based techniques
contribution: improve the computational efficiency and prediction accuracy 
perform better and faster in video object segmentation and semantic label propogation tasks

### Prior work v.s. Proposed method
- semi-supervised methods
  - graph cuts
  - this paper's focus: learn propagation filters in the high-dimensional bilateral space
  1. more generic
  2. allow integration into deep neural network
  3. rely only on offline training (previous frames), can be adapted to online processing
- unsupervised techniques

### Pros & Cons
Pros:
- General applicability
  - can propogate both discrete and continuous information
- Online video analysis
  - need no future frames
- Long-range and image adaptive
- End-to-end trainable
  - can be used in other deep network architectures
- Faster and more accurate

### Their work
1. use six dimensional feature for bilateral fitering : (x,y,r,g,b,t)^T
2. optical flow estimate: shift the pixel position features by their optical flow displacement vectors (referred as "VPN flwo")

### Experiment and results
Experiment setting
- three metrics: Intersection over Union score, Contour accuracy, Temporal instability

### My questions
1. What is the intuition behind the permutohedral lattice space ? What does a point in the lattice space represent ? 
2. Why does the method perform bilateral filtering in this permutohedral lattice space ? Why does it work ? Why is it image-adaptive
Not quite understand the process of Bilateral Layer
3. What is the loss function used for foreground mask propagation ?
4. What does it mean by "superpixel sampling" ?
5. What is the output of the CNN layer, is it the mask for a certain pixel ?

### Feedback and advice on the presentation :-)
1. begin with some introduction about the topic/paper
2. enhance the important points in the slides
3. add referernce  
4. explain important graph with math
5. shorten the recap parts, focus on the proposed method in the paper, timing ! 
6. Evaluation part: show less and guide the audience step by step when comparing different methods with graph
