# Reflection

## Problems I Faced

I encountered some problems while trying to finish this project.

### Tracking the ball 

This is the first problem I encountered. As you can see in the no-hsv branch, my first attempt was just using OpenCV's builtin circle detector to dected a ball. The problem with that is that it wasn't very accurate: often times the tracking would go somewhere else. I had to swtich to something more precise, which is detecting the ball based on color.

### Counting the peaks

The graph used to count the peaks is determined by the x-axis (number of frames) and y-axis (y position of the ball in the frame). However, sometimes there were little fluctations in the height of the ball in the frame. SciPy's `find_peaks` method has a `threshold` parameter to mitigate small peaks that are just volitile fluctiations, but there is another issue with that. Sometimes the ball would get too far from the frame's perspective and the ball's up-and-downs would accidentally be erased and counted as fluctuations when that is not the case. So the `threshold` parameter depends on each video, and how the camera with relation to the ball is positioned.

## What I liked

I liked the fact that I actually solved a small problem with this project, and helped my brother out. After inputing various videos, it actually did pretty well one I fine tuned the threshold argument. Running the same video multiple times (a video of my brother doing ~2000 juggles), it was getting conistently a value 5 +/- the actual number of juggles. I also learned a lot of OpenCV.

## Improvements

### Use Deep Learning to find/track the ball

This improvement is not too ambitious. I think I can use a YOLO model and train it on lots of images of soccer balls to detect the ball super accurately therefore reducing some of the number of fluctuations.

### Make it more accessible to general public

I know lots of people that would like this project and help them, but right now the color selecting process is not intuitive (as well as running a python script from the terminal).

## What I learned

- Python OpenCV
- Some SciPy
