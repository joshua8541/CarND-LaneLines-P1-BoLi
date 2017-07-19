# **Finding Lane Lines on the Road** 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I detected the edges with Canny edge detection. Meanwhile, I defined a polygon region of interest based on the poses of the two lanes. Finally, I ran the Hough transform on the edge detected image to locate the candidate lines along the two lanes. 
![alt text](/Users/Joshua/CarND-LaneLines-P1/test_images_lines/lines_solidYellowCurve.jpg "Detected lanes")

In order to draw a single line on the left and right lanes, I modified the draw_lines() function to draw_lines_solid() by averaging the slope and intercept of candidate lines of left and right lanes perspectively.
![alt text](/Users/Joshua/CarND-LaneLines-P1/test_images_lines/lines_solidWhiteRight.jpg "Extrapolated lanes")


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
