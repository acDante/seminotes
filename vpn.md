## Video Propogation Network
Focus: propagating structured information across video frames
1. Video Object Segmentation: focus on semi-supervised task of propagating foreground mask from the first frame to the entire video
Challenge: scene/camera motion and its effect on the output foreground mask
our Solution: adapt the connectivity of bilateral network to video sequences 

Applications: semantic segmentation; depth estimation

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
  3. rely only on offline training 
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
