# PID controller

## Overview

The goal of this project is to design a PID controller to control the steering angle and throttle to maneuver the vehicle around a track in Udacity simulator.

The simulator provides the cross track error (CTE) which is the distance of car from center of the lane and instantaneous speed and steering angle. 

---

## Reflection

### PID gains (Kp, Ki and Kd)

- The P (proprtional) part is directly proportional to the error and thus it had the most effect on the car's behaviour. Bigger values of Kp lead to overshooting of steering angle and oscillation of car around center lane.
- The D (differential) part is dependent on rate of change of error. This term counteracts the effect of P part by damping the steering angle and the car approaches the center line smoothly. Increasing the value of Kd did not have direct effect on reducing the CTE.
- The I part is proportional to accumulated error over time. This term counteracts any systematic bias in the system.

### Parameter tuning

I implemented two PID controllers in this project, one for steering control and other for throttle to maintain a set speed. The parameter tuning of both controllers are optimized for 30 Mi/h speed.

I initially started with setting Kd and Ki to 0 and increase Kp until the car started to osciallte steadily around the center of the lane.

Increaing Kp for throttle controller lead to steady vehicle speed without any oscillations and thus Kd was set to 0 and Ki was set to 0.001 in order to counteract steady state error if any. Below set of gains worked well for various speeds

```
PID_throttle = {0.1,0.001,0.0}
```

However to counteract the overshoot created by P part for steering angle controller, I started increasing Kd and that dampened the oscillations. Below set of gains worked well for speeds upto around 45 Mi/h.

```
PID_steering = {0.12, 0.001, 1.0}
```


