# door-simulator
Using ROS and Gazebo, door mechanisms are simulated (including the door hinge, handle, and latch). In addition, the door knob dataset can be used to swap the default handle with a desired configuration.

## Structure
```
door-simulator                     # Door Simulator Project
├── door                           # door package
│   ├── config                     # config folder
│   │   ├── config.yaml
│   │   ├── joint_names_complete_door_1.yaml
│   │   ├── rviz.rviz
│   ├── launch                     # launch folder for launch files
│   │   ├── control.launch
│   │   ├── display.launch
│   │   ├── gazebo.launch
│   ├── meshes                     # meshes folder for door components
│   │   ├── door.stl
│   │   ├── frame.stl
│   │   ├── handle.stl
│   │   ├── latch.stl
│   ├── urdf                       # urdf folder for xarco files
│   │   ├── door_fixed.gv
│   │   ├── door_fixed.pdf
│   │   ├── door_fixed.urdf
│   ├── CMakeLists.txt             # compiler instructions
│   ├── package.xml                # package info
└──
```

## Requirement
* Ubuntu 20.04
* ROS 1 Noetic
* Python 3.8
* Gazebo 11 Simulator

## Build and Launch

1. Clone and initialize project with a catkin workspace
```sh
$ mkdir catkin_ws && cd catkin_ws
$ git clone https://github.com/koki-shin/door-simulator.git
$ mv RoboND-Go-Chase-It src
$ cd src && catkin_init_workspace
```

2. Move back to `catkin_ws\` and build
```
$ cd ..
$ catkin_make
```

3. Launch the world
```
$ source devel/setup.bash
$ roslaunch control.launch
```

## Usage


## Contact
Koki Shin - kokishin@tamu.edu

Project Link: https://github.com/koki-shin/door-knob-dataset

## Acknowledgments
Reference Model: https://grabcad.com/library/door-2000x700x40mm-1
