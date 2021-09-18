# Project description

This goal of this project is to design and implement algorithms that recognize hand shapes (such as making a fist, thumbs up, thumbs down, pointing with an index finger etc.) or gestures (such as waving with one or both hands, swinging, drawing something in the air etc.) and create a graphical display that responds to the recognition of the hand shapes or gestures.


#  Methods and Implementation


First, we need to extract the features of sample gestures. We choose the contour of gesture as the main feature. We get the contour of each sample gesture and label them with the feature name. When we present a new gesture in front of the camera, we get the contour of the testing gesture, and then compare the contour of the testing gesture with all sample gestures. Therefore, we return the name of the gesture which matches the testing gesture most

1. skin_detect() We use this function to convert our input image to a binary image and then separate our gesture from the background. 
2.  contour_detect() Next we use the gesture as input and find the contour of the gesture
3. gesture_detect() We use this function to compare our testing gestures with sample gestures. 
4. cv2. matchShapes() This function is an Opencv Built-in function that enables us to compare two shapes, or two contours and returns a metric showing the similarity. The lower the result, the better match it is. It is calculated based on the Hu moment values.

#  Demo

https://www.youtube.com/watch?v=xeqWw_RbnG0&feature=youtu.be