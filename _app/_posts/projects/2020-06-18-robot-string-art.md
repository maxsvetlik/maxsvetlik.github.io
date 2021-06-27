---
layout: post
title: Autonomous Robotic String Art
category: projects
tags: software
---

<img src="../assets/img/string_art/revel_yarn_art.gif" alt="Revel Yarn Art" style="width:85%; height:85%; margin-left: auto; margin-right:auto"/>
<center>
<a href="https://github.com/SvenzvaRobotics/raapps/tree/master/gcode_processor/src"> Check out the project on GitHub </a>
</center>

# At a glance

## What does it do? 
    1) Enables users to generate movement codes (`.gcode` files) based on their preference for the string-art final product
    2) Interpret `.gcode` files to command a 6-DOF robot arm to automate the construction of the string art 

## What is it? 
    A desktop or embedded application for robots.

## What technologies are used? 
    ROS, Python, MoveIt

## What is the ambition of the project? 
    This project was a weekend endeavor and has been used and tested in a limited setting. The goal was to provide customers and users of the Revel robot arm with additional options for control methods, and to possibly inspire customers that were using the arm for academic purposes. 

<br>
# Details
<br>
String Art is 60’s-era craze that used pegs and string to make 2.5D patterns. There are low-dimension robots that are very good at making string art, but I was interested if a general purpose 6DOF robot could.

It turns out the answer is yes. This weekend project has two components:
- A gcode interpreter
- A gcode generator

Gcode was chosen since it is already a common place, well defined control spec. If a customer wanted to use this as the basis for an industrial gcode controller, they very well could.
The gcode is generated based on a parameterized file that specifies the physics of the workspace and art piece. E.g. the number and size of the pegs, the layout and the overall diameter.


This project also required designing a custom gripper attachment that allowed the robot to hold a spool of thread, while having a compliant end-effector so interaction with the pegs would not be damaging to the robot or the workpiece. 

<img src="../assets/img/string_art/revel_yarn_art.jpg" alt="Revel Yarn Art" style="width:60%; height:60%; margin-left: auto; margin-right:auto"/>
