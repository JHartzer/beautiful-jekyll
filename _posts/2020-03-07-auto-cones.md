---
layout: post
title:  Autonomous Cone Placement
image: /assets/img/ConeSetup.png
---

The Auto Cone project is an effort to develop cones that are capable of localizing and placing themselves to improve safety conditions for highway workers. These cones utilize RTK GPS and onboard localization filtering to produce decimeter-level accuracy in placing themselves in road conditions. Additionally, they are capable of transitioning through GPS-denied environments such as under bridges or overpasses. Pictured are two of the cones and the real-time kinematic (RTK) base station.

![cone](/assets/img/ConeSetup.png)

# Problem:

The goal of this project is to develop a robotic platform capable of automatically placing cones in a defined wedge shape behind the work vehicle within the starting lane. Specifically the cones shall: 
- Place three cones in 40 foot increments in a wedge
- Begin the wedge 80 feet from the end of the vehicle
- Operate on highway surfaces unaffected by small debris
- Remain within the lane despite road curvature
- Not rely on magnetic or road-embedded sensors
- Have a speed greater than 0.3 m/s
- Cost less than $1,500 per cone unit
- Be easy to use and require little training

# Kinematics:

The omnidirectional platform makes the system holonomic, which means that with only three motors, the system can smoothly and directly move between any two states. This allows orientation to be independently controlled from position, and makes the system unconstrained by initial conditions. This is very advantageous for pick and place when deploying. The image outlines the kinematics used to drive the cone's motion. 

![Kinematics](/assets/img/Kinematics.png)

# Sensor Fusion:

Using a system of RTK GPS and a ground base station, the cone's acheive a much lower positon error than typical GPS for a relatively small increase in cost. 

![RTK GPS](/assets/img/RTK.png)

Fusing these corrected GPS measurements with the higher rate encoders on the wheel motors provides the system with a high rate localization estimate that is robust in handling drift and sensor noise. 

# Results:

The results of this project were a functioning prototype system that is capable of deploying multiple cones without collision to a wedge shape formation while remaining within lane lines. The system is also capable of operating in GPS-denied environments. 

# Video

[![Autonomous Cone Placement](http://img.youtube.com/vi/0hgOc2csaWE/0.jpg)](https://youtu.be/0hgOc2csaWE "Autonomous Cone Placement")

# Citation:

J. Hartzer and S. Saripalli, “Autocone:  An omnidirectional robot for lane-level cone placement,” inProceedings of the IEEE Intelligent Vehicles Symposium, (Las Vegas, NV), p. 440, 2020.