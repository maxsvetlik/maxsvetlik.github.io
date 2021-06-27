---
layout: post
title: Scavenger Hunt Robot Interface
category: projects
tags: software
---
<center>
<a href="https://github.com/utexas-bwi/scavenger_interface"> Check out the project on GitHub </a>
</center>
<br>

# At a glance

## What does it do? 
    Provides a library to fetch hunts and tasks, and to submit image and video proofs. 

## What is it? 
    A desktop application for robots.

## What technologies are used? 
    ROS, CMake, C++11

## What is the ambition of the project? 
    This project is currently live and will continue to be extended as there are more users on the system. More users means more complex tasks and hunts, and may require adding additional types of proof of completion. 
    The hope is this library lowers the barrier for users to integrate their robots into the Scavenger Hunt challenge, and facilitates a critical mass of users.

<br>
# Details
<br>
Introduced in **A Scavenger Hunt for Service Robots** by Yedidsion et al, the Robot Scavenger Hunt is an international call to robots across the world to compete for points achieving everyday tasks. The [Scavenger Hunt website](https://scavenger-hunt.cs.utexas.edu/) has a leaderboard and an opportunity for users to create new tasks and hunts to push other groups to rise to the challenge.

Part of the challenge was a release of a REST API that robots could use to interact with the website; to get tasks, hunts, submit proofs and check proof status.

After initial release, users reported that the API was difficult and confusing to use. In an attempt to address this, I wrote an interface that can be easily modified and extended, and facilitates critical interactions with the Scavenger Hunt API. This allows the users of the system to focus on enhancing their robot's abilities, rather than re-implementing the same actions individually.

The interface provides a virtual `Hunter` that a user should implement for their robot. I've provided an example hunter, `PassiveHunter`, that attempts to finish tasks passively as its already engaged in something else. This would be the easiest way to encourage others to run the system, since it simple runs in the background.



