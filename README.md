# 7MRI0070-Image-guided-Navigation-for-Robotics

## Introduction
This package is for stereoelectroencephalography (SEEG) electrode insertion path planning and robot simulation using 3D Slicer and ROS Noetic in Ubuntu 20.04. 

## Acknowledgement
This package was developed from [Rachel Sparks](https://gitlab.com/rsparks) [7MRI0070 Guidance ](https://gitlab.com/rsparks/7mri0070).

## Requirement
- Ubuntu 20.04
- 3D Slicer
- ROS Noetic

## Installation
### Path Planning
- To run Ubuntu 20.04 on Windows, download [Ubuntu 20.04 Image](https://releases.ubuntu.com/20.04.6/?_gl=1*1l0rqgf*_gcl_au*ODczNjA3MDAzLjE3MTYyOTMzNDI.&_ga=2.68851985.1299058927.1716814026-1204609532.1716814026) instead of Ubuntu 22.04 Image and use this [link]([https://github.com](https://ubuntu.com/tutorials/how-to-run-ubuntu-desktop-on-a-virtual-machine-using-virtualbox#1-overview)) as a guide. 
- Install 3D Slicer using this [link](https://download.slicer.org)
- To import the pathplanning module, download this repository, open 3D Slicer > Edit > Application Setting > Modules > Additional module paths and put the module path
- To use the SEEGPathPlanning.py, manually copy and paste them to the Python Console in 3D Slicer
### ROS
- To install ROS, open Ubuntu Terminal and use this [link](http://wiki.ros.org/noetic/Installation/Ubuntu) as guidance
- Install [moveit](http://docs.ros.org/en/kinetic/api/moveit_tutorials/html/doc/setup_assistant/setup_assistant_tutorial.html)
- Navigate to the `catkin_ws/src` directory:
    ```sh
    cd catkin_ws/src
    ```
- Download the `SEEG_moveit_config` folder from one of my projects on GitHub. You can do this by cloning the repository:
    ```sh
    git clone https://github.com/estyanadya/7MRI0070-Image-guided-Navigation-for-Robotics/SEEG_moveit_config.git
    ```
- Navigate back to the `catkin_ws` directory and build the project:
    ```sh
    cd ../..
    catkin build
    ```
- To run robot simulation, use this following command:
  ```
  roslaunch SEEG_moveit_config demo.launch
  ```
### 3D Slicer - ROS Integration
- Install ROS-IGTL-Bridge by following the steps in this [link](https://github.com/openigtlink/ROS-IGTL-Bridge/blob/master/README.md)
- Follow configuration steps in this [link](https://github.com/openigtlink/ROS-IGTL-Bridge/blob/master/README.md)

