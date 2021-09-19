# PID Controller

## Overview

The goal of this project is to implement a PID controller to conrol the steering angle and throttle of a car. The controller is tested on a car to be driven around a lake track in [Udacity Simulator](https://github.com/udacity/self-driving-car-sim/releases). The controller is written in C++ and communication between Udacity simulator is done using [uWebSockets](https://github.com/uWebSockets/uWebSockets).

---

## Dependencies

* Linux based OS.
* cmake >= 3.5
* make >= 4.1(mac, linux), 3.81(Windows)
  * Linux: make is installed by default on most Linux distros
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
* [uWebSockets](https://github.com/uWebSockets/uWebSockets)
  * Run `./install-ubuntu.sh`
  * If you install from source, checkout to commit `e94b6e1`, i.e.
    ```
    git clone https://github.com/uWebSockets/uWebSockets 
    cd uWebSockets
    git checkout e94b6e1
    ```
    Some function signatures have changed in v0.14.x. See [this PR](https://github.com/udacity/CarND-MPC-Project/pull/3) for more details.
* Simulator. You can download these from the [project intro page](https://github.com/udacity/self-driving-car-sim/releases) in the classroom.

---
## Basic Build Instructions

1. Download the [Udacity Simulator](https://github.com/udacity/self-driving-car-sim/releases) and install it.
1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run: `./pid`. 
5. Start the simulator and see the car driving around itself on the track!!








