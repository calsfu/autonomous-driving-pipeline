# autonomus-modular-pipeline

An implentation of a modular pipeline for autonomous driving based on a front view image

## lane_detection.py

The front view image is converted to birds eye view, converted to grayscale, then has its absolute gradients calculated. The rowise maximas are found and used as the outline for the lanes. The first lane points are used for the lanes. Each maxima is placed into either the left or right lane. 

## waypoint.py

I used scipy to create splines for our lanes. We take N equidistant points for each spline. We take the midpoint between these points to find our waypoints. 

## lateral_control.py

I incorporated a stanely controller. A stanely controller is a nonlinear controller used for path following that is meant to minimize lateral air between the current postion and desired trajectory. 

## longitundinal_control.py

For longitundinal control, I incoporated a basic PID controller. 