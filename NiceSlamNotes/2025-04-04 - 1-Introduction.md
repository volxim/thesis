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



Weiter bei: In this work, we seek to combine the strengths of hier-
archical scene representations with those of neural implicit
representations for the task of dense RGB-D S...
Seite 2



![[Pasted image 20250406123152.png]]
@strengths of hierarchical scene representations
@strengths of neural implicit scene representations
@for the task of dense RGB-D SLAM
--> NICE-SLAM


@term NICE-SLAM is a "RGB-D SLAM system"
@aim: application to large-scale scenes while preserving the predictive ability.


@key idea: 
- represent scene geometry and appearance with hierarchical feature grids
- incorporate the inductive biases of neural implicit decoders pretrained at different spatial resolutions.
![[Pasted image 20250406124701.png]]
what?

chat gpt explanation:

**Original:**  
_Our key idea is to represent the scene geometry and appearance with hierarchical feature grids and incorporate the inductive biases of neural implicit decoders pretrained at different spatial resolutions._

**Simplified with elaboration:**  
Our main idea is to describe both the **shape** (geometry) and the **look** (appearance) of a 3D scene using **hierarchical feature grids**—which are layered grids that store information about the scene at different levels of detail. We also make use of **neural implicit decoders**—these are special types of neural networks that can learn to represent complex shapes and surfaces in a smooth, continuous way without using traditional 3D meshes. These decoders come with **inductive biases**, meaning they have built-in tendencies or assumptions learned during earlier training. We train them at different **spatial resolutions**, which means they learn to understand scenes at both coarse (zoomed out) and fine (zoomed in) levels of detail.

Let me know if you'd like a visual analogy too—it can help solidify this further!

---


@Observation: too much questionable unknown elements.
@Next Approach: 
Read the whole paper, only extend the glossar on the fly.
Don't dig to deep into the details on the first read. Read the paper, try to understand the key ideas on the surface.

chatgpt:

```text
prompt: 
looking at scientific difficult terms and the levels of understanding, what levels of understanding can be defined


Great question. When dealing with scientific terminology—especially in technical fields—understanding can often be broken down into **levels** or **tiers**. These help categorize how deeply someone comprehends a term, concept, or process. Here’s a structured breakdown of the **levels of understanding** typically used in education, communication, and cognitive science, adapted for scientific language:

---

### **1. Recognition (Surface-Level)**

- **What it is:** Can recognize the term and possibly match it to a broad topic.
    
- **Example:** “I’ve heard of _inductive bias_, but I don’t know what it means.”
    
- **Audience:** General public, beginners.
    

---

### **2. Definition (Literal Understanding)**

- **What it is:** Can define the term using memorized or dictionary-style language.
    
- **Example:** “Inductive bias refers to the assumptions a model makes to predict outputs.”
    
- **Audience:** Early learners, non-specialist readers.
    

---

### **3. Explanation (Conceptual Understanding)**

- **What it is:** Understands the concept enough to explain it in their own words, often with a simple example.
    
- **Example:** “Inductive bias is like a model’s ‘gut feeling’—it’s a built-in way of guessing that helps it learn faster.”
    
- **Audience:** Undergraduate students, interdisciplinary collaborators.
    

---

### **4. Application (Contextual Use)**

- **What it is:** Can correctly use the concept or term in real-world or academic settings.
    
- **Example:** “We introduced a model with a strong spatial inductive bias to speed up training on 3D scenes.”
    
- **Audience:** Graduate students, technical professionals.
    

---

### **5. Analysis (Critical Understanding)**

- **What it is:** Can compare, critique, or analyze how the term works in different contexts.
    
- **Example:** “Different neural architectures encode inductive biases differently, and this affects generalization.”
    
- **Audience:** Researchers, advanced practitioners.
    

---

### **6. Synthesis (Creative/Innovative Use)**

- **What it is:** Can extend or modify the concept, integrate it with others, or use it to generate new ideas or frameworks.
    
- **Example:** “We designed a hybrid system that combines hierarchical feature grids with learned inductive biases from multi-resolution implicit decoders.”
    
- **Audience:** Domain experts, thought leaders, innovators.
    

---

These levels can help you assess your audience and choose how to present complex scientific material—whether in teaching, writing, or public outreach. Would you like a visual diagram or table summarizing these levels?
```



Weiter bei Seite 21

With the rendered depth and color images from the occu-
pancy and color decoder outp