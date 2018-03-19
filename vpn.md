## Video Propogation Network
Focus: propagating structured information across video frames

Applications: semantic segmentation; depth estimation

### Methods
This method combines two components:
- temporal bilateral network 
  - perform image-adaptive spatio-temporal dense filtering
  - connect densely pixelwise to propagate pixel information across frames
  - can define a metric between pixels
  
- spatial CNN 
  

### Previous Works & their contribution
optimization based techniques
contribution: improve the computational efficiency and prediction accuracy 
perform better and faster in video object segmentation and semantic label propogation tasks

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
