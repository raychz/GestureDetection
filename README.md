# Gesture_Detection
Technologies
We used OpenCV-Python, a library of Python bindings designed to solve computer vision problems. OpenCV-Python makes use of Numpy, a highly optimized library for numerical operations.  The exact versions of software we used are OpenCV 2.4. 9 and Python 2.7.9.

Skin Color and Red Color Detection
Initially, we used the skin color detection code provided from the labs to detect hands. Eventually we changed the threshold values for RGB to detect red color instead of skin color because the camera would also take in our head and neck area and disrupt contour recognition.

Contours
Contours are the curves joining all the continuous points along the boundary of the input. The contour is drawn along the boundary of the hand image which is found after thresholding the image. We used contours for shape analysis and hand/input detection in this project.

Convex Hull and Defect Points
Convex hull is the set of continuous points that is connected to contours; it works like an envelope around the hand. By definition, the convex hull of a set X of points in the Euclidean plane is the smallest convex set that contains X. So when the convex hull is drawn around the contour, it uses minimum points to form the hull and maintain convexity. This causes the formation of defects in the convex hull with respect to the contour drawn on the hand. As a result, we can determine the number of fingers in the hand gesture by determining the number of defect points in the captured image.
