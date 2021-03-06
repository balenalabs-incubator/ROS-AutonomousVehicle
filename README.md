# Autonomous Vehicle Demo - ROS on balenaCloud

The [Robot Operating System](https://www.ros.org/), or ROS as it is commonly known, is a popular open source framework for building, programming, controlling, and interacting with a wide range range of “robots”.  The definition of robots here can vary, from traditional robotic arms that grasp, pivot, rotate, and use actuators to move around in 3-dimensional space, to things like autonomous vehicles, drones, delivery bots, and other machines that self-navigate and move around the world.  This repo focuses on the latter definition, and creates a simulated vehicle driving around a virtual world.

This particular demo highlights the features and capabilities of ROS to build and test autonomous vehicles, showing functions such as cameras and LIDAR, in a simulated environment.  ROS uses a framework of topics and messages, in a publisher and subscriber model.  All of that can be done programmatically without any displays, input, or other real “interaction” with the robot or device.  But, for learning purpose, it can be helpful to visualize what is occurring, which is the aim of this project.

## Requirements
 - x86-powered device, like an Intel NUC or similar "PC-like" hardware.  It will not run on a Raspberry Pi, Nvidia Jetson, or other Arm-powered devices.
 - 4gb RAM
 - Monitor, Keyboard, Mouse

![Simulator Image](https://github.com/balena-io-examples/ROS-AutonomousVehicle/blob/main/simulator.png)

This demo was built by the [Open Source Robotics Foundation](https://www.openrobotics.org/), all credit is due to them for the construction of this application.  We simply placed it into a balena container to make it easy to deploy and begin learning from and experimenting with.

## Getting Started

To get started, do a `git clone` of this repo, and then a `balena push YourApplicationNameHere`.  You can read about the process more here:  https://www.balena.io/docs/learn/deploy/deployment/

However, ever easier than that, is to just click this button:

[![balena deploy button](https://www.balena.io/deploy.svg)](https://dashboard.balena-cloud.com/deploy?repoUrl=https://github.com/balenalabs-incubator/ROS-AutonomousVehicle)

The container will begin building in balenaCloud, installing all of the packages defined in the Dockerfile.  Once your device is provisioned and connected to balenaCloud, the container will download onto the device (a NUC or similar in this case) and the application will start up.  After everything is launched and the virtual world starts up, you may need to rearrange windows to see that there are two applications running.  You can use the `W` `A` `S` and `D` keys to drive the Prius, and the mouse can manipulate the viewing angle.  

The usage of RVIZ and Gazebo is beyond the scope of this documentation, so, you may need to consult the official websites for those projects for usage and options.  The goal of this repo, is to just do the containerization and make it easy to deploy on balena.

## Additional Info

More information is available in the ReadMe in the `prius` directory, have a look there for added info provided by the OSRF.

Further reading on ROS can found on their website, specifically:
 - http://wiki.ros.org/
 - https://index.ros.org/
 - https://www.ros.org/
 
![Prius Image](https://www.osrfoundation.org/wordpress2/wp-content/uploads/2017/06/prius_roundabout_exit.png)
