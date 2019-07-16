# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report




---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, 
Secondly, I applied gaussian blur to smooth out the hight frequency component from the image,
thirdly , I applied canny edge detection algorithm to line the outling of lane lines 
fourthly , I applied ROI(Region of intrest to trim off unncessary parts of our image)
fifthly , I applied hough transform to find the lines in the image by fitting a line equation(done internally)
sixthly, I calculated the slope of the line to figure out which is left and which is right lane by taking slope of the line(if slope is positive then it is right lane and of slope is negative then it is left lane)
finally , I approximated a line over the averages to make one solid line and drew over the actual image




### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when we reach a corner then the algorithm doesn't do the job in tracing the line

Another shortcoming could be it is really hard to calibrate the hough transform to generalize for variety of scenarios , 


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to add a feture which keeps track of the curve of the lane line to accurately locate the lane line


