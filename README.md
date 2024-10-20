# autonomus-modular-pipeline

An implentation of a modular pipeline for autonomous driving based on a front view image
![image](https://github.com/user-attachments/assets/6625c17f-2a63-441c-bc31-42b10e095c45)

## lane_detection.py

The front view image is converted to birds eye view, converted to grayscale, then has its absolute gradients calculated. The rowise maximas are found and used as the outline for the lanes. The first lane points are used for the lanes. Each maxima is placed into either the left or right lane. 
![image](https://github.com/user-attachments/assets/df6e2d39-4b92-45c3-8171-f98e1e6c7084)
![image](https://github.com/user-attachments/assets/312424ab-9cbc-4f24-9ed1-9f691656c0a8)
![image](https://github.com/user-attachments/assets/8cefd90e-6c73-4499-a6db-e1f97fd95e0b)

## waypoint.py

I used scipy to create splines for our lanes. We take N equidistant points for each spline. We take the midpoint between these points to find our waypoints. 
![image](https://github.com/user-attachments/assets/14ec9f95-b71c-4df4-8376-2dad79b0de8a)
![image](https://github.com/user-attachments/assets/ba45bd16-8d04-483e-8893-9476a5eb7cd0)

## lateral_control.py

I incorporated a stanely controller. A stanely controller is a nonlinear controller used for path following that is meant to minimize lateral air between the current postion and desired trajectory. 
![image](https://github.com/user-attachments/assets/8cd45c02-e623-4e66-bc8c-66e5fc4cbccb)
![image](https://github.com/user-attachments/assets/42364659-0f7c-426e-9a1f-9046903e188f)

## longitundinal_control.py

For longitundinal control, I incoporated a basic PID controller. 

![image](https://github.com/user-attachments/assets/f678d830-44c7-4f37-b43c-501ca22ab940)
