# Project description

The goal of this part of the programming assignment is to learn more about the practical issues that arise when designing a tracking system. We are asked to track moving objects in video sequences, i.e., identifying the same object from frame to frame:


#  Methods and Implementation
First we need to do the data segmentation. We use Frame differencing to checks the difference between two video frames so that we can segment our objects from the background. Next, we create a tracker. The tracker will create a track for each object. The track implements Kalman filter to predict the area of a given object's next location. Then we use Hungarian Algorithm to match exist tracks and new points.

#  Challenging Situations

1.  One challenging situation our tracker succeeds in is when two objects meet at one place our tracker does not lose the tracking path and maintains the path line well after the two objects separate. However, our tracker may fail in the case that our detection for some small objects is not accurate.
    
2.  We begin a new tracker by detecting the position of a new object. However, we fail to terminate the old tracks. We tried to set a timer and a threshold. We thought once the timer passes the threshold, we delete the track, but somehow it does not work
