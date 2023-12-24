This repo contains the source files of the design project of EECS467. 
The project, inspired by RTS games, develops a multi-agent robot system that can be controlled by laser pointers. Users can circle a group of robots to activate them and then shoot a target point as the destination for them. The robots we use are Mbots provided by UMich and each of them has a Raspberry Pi 4B and an RPi Lidar. 
The computer vision algorithm for detecting laser points is completed with Intel RealSense Depth Camera and OpenCV package. The depth camera is employed to obtain the distance of target point. The pipeline of the CV algorithm is briefly shown in the following diagram. 

<div align=center>
<img src="https://github.com/nexuszhan/EECS467-Design-Lab/blob/main/imgs/laser_diagram.png" width="400px">

We use ROS2 to control the pico board as well as enable robots to communicate with each other. In this way, if one activated robot fail to see the target point, another activated robot that see the point will tell it the position. 