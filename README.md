Engineering materials
====

This repository contains engineering materials of a self-driven vehicle's model participating in the WRO Future Engineers competition in the season 2022.

## Content

* `t-photos` contains 2 photos of the team (an official one and one funny photo with all team members)
* `v-photos` contains 6 photos of the vehicle (from every side, from top and bottom)
* `video` contains the video.md file with the link to a video where driving demonstration exists
* `schemes` contains one or several schematic diagrams in form of JPEG, PNG or PDF of the electromechanical components illustrating all the elements (electronic components and motors) used in the vehicle and how they connect to each other.
* `src` contains code of control software for all components which were programmed to participate in the competition
* `models` is for the files for models used by 3D printers, laser cutting machines and CNC machines to produce the vehicle elements. If there is nothing to add to this location, the directory can be removed.
* `other` is for other files which can be used to understand how to prepare the vehicle for the competition. It may include documentation how to connect to a SBC/SBM and upload files there, datasets, hardware specifications, communication protocols descriptions etc. If there is nothing to add to this location, the directory can be removed.

## Introduction

_This part must be filled by participants with the technical clarifications about the code: which modules the code consists of, how they are related to the electromechanical components of the vehicle, and what is the process to build/compile/upload the code to the vehicle’s controllers._

For the open challenge round, we used VL53L0X Time of Flight (ToF) distance sensors to sense the inner walls. There is 1 ToF sensor on each side of the robot, hence allowing the robot to sense the inner walls regardless of which direction it is moving and which side of the robot the inner wall is on. The ToF senses the distance from the walls. When the ToF senses a large distance, meaning that the inner wall is no longer in the range of the ToF, the robot would turn in the corresponding direction, hence going along the inner wall. Since the ToF also senses the distance the robot is from the inner wall, the robot would be able to turn away from the inner wall if it is too close and turn away from the inner wall if it is too far. Hence, it would not crash into the inner wall, or be too far from the inner wall that it hits the outer walls. 
For the obstacle challenge round, we used a camera. The camera would sense the traffic signs (green or red), hence allowing the robot to know which direction it should be turning in (if it senses green, it turns left and if it senses red, it turns right).
