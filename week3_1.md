## Interactive Design of 3D-Printable Robotic Creatures
### Main Topics
interactive design system that allows casual users to quickly design 3D-printable robotic creatures
- generate stable motions for legged robots by solving a trajectory optimization problem

Challenges
1. physical feasibility
2. balance between complexity of design and cost

### Contirbutions
- optimization-based method that generates stable motions for legged robots
- geometric view of trajectory optimization 
- interactive tools for robot design , which provides support for 3D printing
editable properties include: morphology, proportion, gait and motion style 

### Previous Work
 
### Methods
#### Deisgn Interface
- Left: editing structure and motion of the robot
- Rigth: preview of real-world behavior

#### Structure Editing
1. load a description file which defines an initial model for robot (hierarchical description of joint connection)
2. edit the structure by adding / removing motors

#### Motion Editing

#### Trajectory Optimization
Goal: Given structure and motion goals -> compute time-varying motor values for stable motions 

### My questions
1. What is the "supporting polygon" ?
