# door-simulator

  ![](door-opening.gif)
  
  <p align="center">
  <img width="400" height="250" src="https://github.com/koki-shin/door-simulator/blob/main/imgs/handledoor_closingfaster.gif">
  <img width="400" height="250" src="https://github.com/koki-shin/door-simulator/blob/main/imgs/handledoor_latch.gif">
  </p>
  
  <p align="center">
  <img width="400" height="250" src="https://github.com/koki-shin/door-simulator/blob/main/imgs/pulldoor_closing.gif">
  <img width="400" height="250" src="https://github.com/koki-shin/door-simulator/blob/main/imgs/transparent-handle-turning.gif">
  </p>

## Summary
Using ROS and Gazebo, door mechanisms are simulated (including the door hinge, handle, and latch). In addition, the door knob dataset can be used to swap the default handle with a desired configuration.

## Directory Structure
```
door-simulator                 # Door Simulator Project
├── door                       # door package
├── config                     # config folder
    ├── controller.yaml
├── launch                     # launch folder for launch files
    ├── door.launch
    ├── door_with_controller.launch
├── meshes                     # meshes folder for stl files
    ├── door.stl
    ├── frame.stl
    ├── frame_16x22.stl
    ├── frame_17x22.stl
    ├── frame_18x22.stl
    ├── frame-kevin.stl
    ├── handle.stl
    ├── latch.stl
    ├── pull_handle1.stl
├── urdf                       # urdf folder urdf files
    ├── handle_door.urdf       # urdf description of the handle door model
    ├── handle_door_actuated.urdf
    ├── pull_door.urdf         # urdf description of the pull door model
    ├── pull_door_actuated.urdf  
├── world
├── CMakeLists.txt             # compiler instructions
└── package.xml                # package info
```

## Requirement
* Ubuntu 20.04
* ROS 1 Noetic
* Python 3.8
* Gazebo 11 Simulator

## Build and Launch

1. Clone and initialize project with a catkin workspace
```sh
$ mkdir -p catkin_ws/src && cd ~/catkin_ws/src
$ git clone https://github.com/koki-shin/door-simulator.git
$ catkin_init_workspace
```

2. Move back to `catkin_ws\` and build
```
$ cd ~/catkin_ws 
$ catkin_make
```

3. To spawn the controllers and the model in gazebo:
```
$ source devel/setup.bash
$ roslaunch door_simulator door.launch --ros-args
$ roslaunch door_simulator door.launch door_type:=handle gui:=true
```
```
$ roslaunch door_simulator door.launch door_type:=pull gui:=true
$ roslaunch door_simulator door_with_controller.launch door_type:=handle 
$ roslaunch door_simulator door_with_controller.launch door_type:=pull 
```

## Usage


## Contact
Koki Shin - kokishin@tamu.edu

Project Link: https://github.com/koki-shin/door-simulator

## References
Reference Model: https://grabcad.com/library/door-2000x700x40mm-1
