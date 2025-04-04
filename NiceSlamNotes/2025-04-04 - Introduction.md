Dense visual Simultaneous Localization and Mapping (SLAM) 
	is a
		 fundamental problem in 3D computer vision 
	 with 
		 many applications in autonomous driving, indoor robotics, mixed reality, etc.

@terms: 
fundamental problem
3d computer vision

@domains:
autonomous driving, indoor robotics, mixed reality, etc.



*In order to make a SLAM sys-*
*tem truly useful for real-world applications, the following*
*properties are essential. First, we desire the SLAM system*
*to be real-time. Next, the system should have the ability*
*to make reasonable predictions for regions without obser-*
*vations. Moreover, the system should be able to scale up to*
*large scenes. Last but not least, it is crucial to be robust to*
*noisy or missing observations.*

@problems:
real-time. how is this achieved?
reasonable predictions for regions without observations. why? how?
scaling up to large scenes
robust to missing observations. define robust?
robust to noisy observations. example?


In the scope of real-time dense visual SLAM system,
many methods have been introduced for RGB-D cameras in
the past years. Traditional dense visual SLAM systems \[30,
42, 59, 60] fulfil the real-time requirement and can be used
in large-scale scenes, but they are unable to make plausible
geometry estimation for unobserved regions. 

@what RGB-D cameras


@dig Traditional dense visual SLAM systems
fulfil the real-time requirement
can be used in large-scale scenes
unable to make plausible geometry estimation for unobserved regions

@dig learning-based SLAM approaches \[3,12,48,68\]
attain a certain level of predictive power
since they typically train on task-specific datasets

@dig learning-based methods
tend to better deal with noises and outliers
typically only working in small scenes with multiple objects

@term outliers
Plural form of outlier
1. One that lives or is located outside or at the edge of a given area.    
2. One that exists outside or at an extreme of a category, pattern, or expectation; an extreme case or exception.
3. A value far from most others in a set of data.



Sucar et al. \[47\] applied 
a neural implicit representation 
in the real-time dense SLAM system (called iMAP)
results: 
- decent tracking and mapping results for room-sized datasets
- scaling up to larger scenes, an apartment consisting of multiple rooms
	- significant performance drops are observed
		- in both the dense reconstruction 
		- and camera tracking accuracy.


@Observation so far. 
It is quicker to summarize the key points instead of annotating everything.
A second read must be done for deeper refinement. For now, it should be enough to summarize and point out questionable elements.

key limiting factor of iMAP \[47\] originates from
- use of a single multi-layer perceptron (MLP) to represent the entire scene
	- which can only be updated globally with every new, potentially partial RGB-D observations

@terms perceptron

In contrast, recent works \[38, 49\] demonstrate
- establishing multi-level grid-based features 
	- can help to preserve geometric details and enable reconstructing complex scenes, 
		- problem: these are offline methods without real-time capability.



