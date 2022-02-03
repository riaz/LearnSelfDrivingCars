Localization
===================

### Localization

Accelometer [3 axes] - accurately measure acceleration

Records - based on co-frame of vehicle
We need to translate the acc/velocity in the global co-od frame
To translate : local co-od -> global co-od  [ we need a gyroscope [3D]]

Gyroscope:
    The 3 external gimbals of 3-axis gryo are always rotating
    But the spin axis, is always fixed to world co-od system
    We can calc loc of vehicle by measing the relative pos of spin axis in the 3 external gimbals
    
An Acc & Gyro are main components of an IMU - 1000 hz (high-freq update)
Disadvantage of IMU - only good for certain time, but we can do well with gpu info [ IMU [high update], GPU [slow update]] -> loc

### Lidar Location

We can localize based on point cloud matching, on the pre-computed HD maps
Many algorithms for matching point clouds

Eg:
    i.  Iterative Closest Point (ICP)  [Minimize the distance between point in PC and real world]
    ii. Filter Algorithms
    iii. Kalman Filter

Apollo uses histrogram filter,  sum of squared distance [SSD], we do a sliding-window scan between points in (PC and HD maps).

Kalman Filter is used to measure current state as func of (curr measurement, prev position), leading to a prediction update cycle.

Adv of lidar location - Robustness, [just needs HD maps & lidar , disadv: need upt to date map data]

### Visual Localization

Camera data + Map + GPS Data 

Particle - using observations to filter choices and approach to the right choice
https://classroom.udacity.com/courses/cs373/lessons/48704330/concepts/487500080923

Disadv: Hard to map 2d images at arbitracy camera angles with 3d maps.


### Apollo Sensor Fusion / Localization

Apollo uses a multi-sensor fusion , since not one device in itself is the most reliable

GPS , IMU and Lidar , Radar and HD Maps

Supports: GNSS loc [position and velocity], Lidar loc [position and heading info]

Fusion [based on KF filter] -> GNSS loc [is used for measurement update step of KF]

KF based Localization [Apollo]

![Apollo Localization](https://video.udacity-data.com/topher/2018/July/5b39a1b3_kalman-filter/kalman-filter.png)



### Reference

Apollo Localization Module
https://github.com/ApolloAuto/apollo/tree/master/modules/localization


Apollo Localization Paper
Robust and Precise Vehicle Localization based on Multi-sensor Fusion in Diverse CityScenes, ICRA, 2018
https://arxiv.org/pdf/1711.05805.pdf
