# Juggle Counter

## Problem

My brother is getting very good at juggling a soccer ball and he records himself to count how many he has done later. As you progress, this number can be in the thousands. Counting this number of juggles by hand to see if you broke your PB is not that fun. This program counts the number of juggles for you. Automation.

## Overview

![side](docs/side-by-side.png)


## Tech stack

- Python 3
- OpenCV
- SciPy
- Matplotlib
- NumPy




The y coordinates are the center of the detected ball with the x-axis being the number of frames.

Each marked X is a peak, when the ball is up and just about to fall down. The number of preaks should be the number of juggles done.

Uses OpenCV (cv2) for the ball detection, SciPy to find the peaks, and Matplotlib to graph.
Run the program by doing `python3 HSV/counter_HSV.py path/to/juggle_video.mp4`
Works with other video files as well, like .MOV.
