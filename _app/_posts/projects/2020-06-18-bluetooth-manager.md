---
layout: post
title: Multiagent Bluetooth Manager
category: projects
tags: software
---

<center>
<a href="https://github.com/utexas-bwi/bluetooth_bridge"> Check out the project on GitHub </a>
</center>
<br>

# At a glance

## What does it do? 
    This library enables robots to communicate with each other while in close proximity over bluetooth. 
    It is specifically designed to share ROS messages to support multi-agent systems.

## What is it? 
    A desktop or embedded application for robots.

## What technologies are used? 
    ROS, Python 3+, Py-serial, bluez, bluez-tools

## What is the ambition of the project? 
    To ease the reliance on internet connectivity for intra-robot communication. This library is very promising to me, and I have a strong desire to continue development. 
    It has been tested and deployed on actual robots. Additional users would be helpful to help stress test the system and report what features are missing for their usecase.

<br>
# Details
<br>

This project was designed around a singular issue that was present in my robotics lab: robots needed to communicate their position with one another, but due to non-deterministic aberrations in wireless connectivity, messages would be lost, slow, out of order, or catastrophically dropped. For the project goal, robots passing each other reliably in the hallway, these networking issues were a major road block.

The methodology I introduce with the `Bluetooth Bridge` library is to eliminate the need to internet connectivity completely. Since the robots need to share their location with other robots while near by, a local area data exchange would suffice. Bluetooth is a great candidate for this.

The project's [README](https://github.com/utexas-bwi/bluetooth_bridge/blob/master/README.md) is comprehensive, so I won't repeat it fully. The System contains the following components: 
- `bidirectional serial bridge` responsible for serializing and deserializing messages between robots
- `port manager interface` manages in/active connections to the bluetooth device 
- `blueooth port manager` manages and interacts with the low level bluetooth driver interface

The overall system can be seen below. One of the more exciting aspects of this is that **it SCALES**! You can run this on multiple robots and it will passively connect and disconnect when a robot is within range of the others.

<img src="../assets/img/bluetooth_bridge/bluetooth_bridge_flow.png" alt="Bluetooth Bridge system diag   " style="width:95%; height:95%; margin-left: auto; margin-right:auto"/>
