SLAM - simultaneous localization and mapping


@Page 2
@From: In this Work, we seek...

| Key                               | Explanation, first run                                                                                                                                                                                                                                         |
| --------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|                                   |                                                                                                                                                                                                                                                                |
|                                   |                                                                                                                                                                                                                                                                |
| hierarchical scene representation |                                                                                                                                                                                                                                                                |
| neural implicit representation    |                                                                                                                                                                                                                                                                |
| dense RGB-D SLAM                  |                                                                                                                                                                                                                                                                |
| NICE-SLAM                         | dense RGB-D SLAM system                                                                                                                                                                                                                                        |
| predictive ability                |                                                                                                                                                                                                                                                                |
| scene geometry                    |                                                                                                                                                                                                                                                                |
| scene appearance                  |                                                                                                                                                                                                                                                                |
|                                   |                                                                                                                                                                                                                                                                |
| feature grid                      |                                                                                                                                                                                                                                                                |
| hierarchical feature grids        |                                                                                                                                                                                                                                                                |
| decoder                           |                                                                                                                                                                                                                                                                |
| inductive bias                    |                                                                                                                                                                                                                                                                |
| neural implicit decoder           |                                                                                                                                                                                                                                                                |
| spatial resolution                |                                                                                                                                                                                                                                                                |
| rendered depth images             | These images represent the distance between the camera and different points in a scene                                                                                                                                                                         |
| rendered color images             | regular color images                                                                                                                                                                                                                                           |
| occupancy decoder outputs         |                                                                                                                                                                                                                                                                |
| color decoder outputs             |                                                                                                                                                                                                                                                                |
| viewing frustum                   |                                                                                                                                                                                                                                                                |
| re-rendering losses               |                                                                                                                                                                                                                                                                |
| indoor RGB-D sequences            |                                                                                                                                                                                                                                                                |
| RGB-D Camera                      | A camera that provides both depth (D) and color (RGB) data as the output in real-time.<br>https://www.e-consystems.com/blog/camera/technology/what-are-rgbd-cameras-why-rgbd-cameras-are-preferred-in-some-embedded-vision-applications/<br>`2025-04-06 14:43` |
| scalability                       | smal room -> big room or so                                                                                                                                                                                                                                    |
| predictive ability                |                                                                                                                                                                                                                                                                |
| mapping                           |                                                                                                                                                                                                                                                                |
| tracking                          |                                                                                                                                                                                                                                                                |
|                                   |                                                                                                                                                                                                                                                                |
|                                   |                                                                                                                                                                                                                                                                |
|                                   |                                                                                                                                                                                                                                                                |

@Page2, 2. Related Work

| Key                | Explanation, first run |
| ------------------ | ---------------------- |
| Dense Visual SLAM  |                        |
| Sparse Visual SLAM |                        |
| mapping            |                        |
| tracking           |                        |
|                    |                        |



---
Playground and Templates for the Glossar section





---
Prompt:
chatgpt 
`create a markdown table template which i can fill out in regard to the levels of understanding`

| Level of Understanding | Description | Your Explanation / Example |
|------------------------|-------------|-----------------------------|
| 1. Recognition         | Can identify or has heard the term; no real understanding. |                             |
| 2. Definition          | Can provide a dictionary-style definition or basic meaning. |                             |
| 3. Explanation         | Can explain the concept in their own words and give a simple example. |                             |
| 4. Application         | Can use the concept correctly in context (e.g., writing, code, experiments). |                             |
| 5. Analysis            | Can compare, critique, or analyze the concept in different contexts. |                             |
| 6. Synthesis           | Can extend or creatively apply the concept to novel situations or combine it with others. |                             |

| Level of Understanding | Description | Helper Questions | Your Explanation / Example |
|------------------------|-------------|------------------|-----------------------------|
| 1. Recognition         | Can identify or has heard the term; no real understanding. | - Have I seen or heard this term before?<br>- Where did I come across it? |                             |
| 2. Definition          | Can provide a dictionary-style definition or basic meaning. | - What does the term literally mean?<br>- How would I define it in one sentence? |                             |
| 3. Explanation         | Can explain the concept in their own words and give a simple example. | - How would I explain this to a non-expert?<br>- Can I give a simple real-world analogy or example?<br>- What problem does it help solve? |                             |
| 4. Application         | Can use the concept correctly in context (e.g., writing, code, experiments). | - How is this term used in practice?<br>- Can I describe a scenario where I used it?<br>- What’s a typical use case? |                             |
| 5. Analysis            | Can compare, critique, or analyze the concept in different contexts. | - How does this term relate to or differ from similar concepts?<br>- What are its strengths and limitations?<br>- In which contexts does it perform best or worst? |                             |
| 6. Synthesis           | Can extend or creatively apply the concept to novel situations or combine it with others. | - How can I combine this concept with another idea?<br>- Can I apply it to a new or unconventional domain?<br>- How might I improve upon or generalize it? |                             |


### Example (Filled out for "Inductive Bias"):

| Level of Understanding | Description                                                                               | Your Explanation / Example                                                                                   |
| ---------------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| 1. Recognition         | Can identify or has heard the term; no real understanding.                                | "I've seen this term in machine learning papers."                                                            |
| 2. Definition          | Can provide a dictionary-style definition or basic meaning.                               | "Assumptions a model makes to predict outputs."                                                              |
| 3. Explanation         | Can explain the concept in their own words and give a simple example.                     | "It's like a model's built-in guesswork that helps it learn faster."                                         |
| 4. Application         | Can use the concept correctly in context (e.g., writing, code, experiments).              | "We used CNNs because their spatial inductive bias suits image data."                                        |
| 5. Analysis            | Can compare, critique, or analyze the concept in different contexts.                      | "Transformers lack certain biases that CNNs have, which can affect performance on visual tasks."             |
| 6. Synthesis           | Can extend or creatively apply the concept to novel situations or combine it with others. | "We created a hybrid model that mixes spatial and temporal inductive biases to improve video understanding." |

