# **Finding Lane Lines on the Road**

[image1]: ./images_witeup/1.png
[image2]: ./images_witeup/2.png
[image3]: ./images_witeup/3.png
[image4]: ./images_witeup/4.png
[image5]: ./images_witeup/5.png



## 1. Describtion of my pipeline.
My pipeline consisted of 5 steps:  
**1st**  
Convert the images to grayscale  
![alt text][image1]  
**2nd**  
Get the edges with canny function  
![alt text][image2]  
**3rd**  
Get the region that interests me  
![alt text][image3]  
**4th**  
Get the lane lines with Hough transform  
![alt text][image4]  
**5th**  
Draw the lane lines on the original images  
![alt text][image5]  

In order to draw a single line on the left and right lanes,I divided the points into two groups by using the slope of lines.Then I get two group of points marked with left and right.Then I calculate a line by using the farthest point and the nearest point in each group.After all of these steps,I extend the line I calculated to the mask scale.


### 2. Shortcomings with your current pipeline
1.My pipeline can't divide the lines correctly on the curved lane.  
2.My pipeline can't work well when the color of road is approach to the lane line.  


### 3. Suggest possible improvements to your pipeline

Maby we can use two-dimensional polynomial fitting to get a curve,instead of a straight line.

