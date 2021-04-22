# Reflection

## Problems Encounterred

I encountered some problems while trying to finish this project.

### Tracking the ball 

This is the first problem I encountered. As you can see in the no-hsv branch, my first attempt was just using OpenCV's builtin circle detector to dected a ball. The problem with that is that it wasn't very accurate: often times the tracking would go somewhere else. I had to swtich to something more precise, which is detecting the ball based on color.

### Counting the peaks

The graph used to count the peaks is determined by the x-axis (number of frames) and y-axis (y position of the ball in the frame). However, sometimes there were little fluctations in the height of the ball in the frame. SciPy's `find_peaks` method has a `threshold` parameter to mitigate small peaks that are just volitile fluctiations, but there is another issue with that. Sometimes the ball would get too far from the frame's perspective and the ball's up-and-downs would accidentally be erased and counted as fluctuations when that is not the case. So the `threshold` parameter depends on each video, and how the camera with realtion to the ball is positioned.

## What I liked

## Improvements

### Use Deep Learning to find/track the ball

## What I learned

- Python OpenCV
- Manipulating videos all around
- Little SciPy