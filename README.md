# Estimating-Firebrand-Properties-from-Multiple-Video-Cameras
 In this project, we use image data collected from a system of 4 video cameras to characterize the firebrands. 

Background: Wildland fires have caused significant destruction to communities in Australia, Greece, Portugal, Spain, and the USA. The 2007 Southern California Fire displaced more than 300,000 people, destroyed over 1,000 structures, and resulted in $1B paid by insurers in 2007 alone. WUI fires continue to burn in the USA and are rapidly getting worse; most recently, the tragic Camp Fire in California in 2020 [1,2].

When vegetation and structures burn in large outdoor fires, pieces of burning material, known as firebrands, are generated, become lofted, and may be carried by the wind. This results in showers of wind-driven firebrands that may land ahead of the fire front, igniting vegetation and structures, and spreading the fire very fast. Post-fire disaster studies indicate that firebrand showers are a significant factor in the fire spread of multiple large outdoor fires.

Project Statement: To protect communities from firebrand ignition, it is critical to understand the characteristics of the firebrand shower. In this project, we use image data collected from a system of 4 video cameras to characterize the firebrands. The researcher who has collected the video images wants to know the following information about the firebrands.

a) What is the energy content of the firebrand? What is the propensity for ignition?

b) What is the size of the firebrand? This includes

Volume of the firebrand.

Length, Width, Height of the firebrand.

Orientation (3 D rotation angle) of the firebrand.

c) What is the general shape of the firebrand? Is the firebrand a cylinder or a sphere or a disk?

The goal of this project is to investigate if images collected from a system of four video cameras accurately characterize the firebrands? For each task a) through c), report the accuracy of prediction, assumptions and limitations in performing and completing the task [3-6].

DATASET : https://drive.google.com/file/d/10H3ohDJTGproNjZPn0SBZhzTwMjuUd6w/view?usp=sharing

NOTE : First we have done the classification problem because the shape of firebrand is needed in order to approach the regression problem. So we have used the original dataset to classify shape of firebrand and then exported 3 CSV files which we will use for the regression problem later on.

NOTE : Plesae download the whole repository as .zip and then see the python notebooks. Will fix that compatibility soon as well.
