---
layout: post
title: Goldboy Color Emulator
category: projects
tags: software
---

<img src="../assets/img/gameboy/gouldboy_color.png" alt="Gouldboy Color IMG" style="width:100%; height:100%; margin-left: auto; margin-right:auto"/>

<center>
<a href="https://github.com/maxsvetlik/gouldboycolor"> Check out the project on GitHub </a>
</center>
<br>

# At a glance

## What does it do? 
    This project emulates the hardware of a Nintendo Gameboy Color on a desktop.

## What is it? 
    A desktop application

## What technologies are used? 
    C

## What is the ambition of the project? 
    To learn and understand the lower level architecture of embedded hardware.
    This emulator successfully emulates the memory and CPU of a handheld device that was at one time the height of gaming.

<br>
# Details
<br>

Gouldboy Color is a Gameboy Color emulator written from scratch in C. This was pitched as an alternative, independent project for my Advanced Computer Architecture course at the University of Texas.
It implements over 100 CPU codes to perform essential tasks like mathematic operations, memory storage and manipulation, and graphics handling. 

This more/less fully implements a Zilog Z80 Hybrid CPU over ~1200 lines of code. Though nominally an 8-bit CPU, there are 2 16bit registers, one of which is the Stack Pointer (SP) which allows for much more available memory (2^16 bits). 

Not all titles are playable, as many games utilized tricks to squeeze as much performance out of the machine as possible. Many of these features are not well documented, if at all. Still, its usable and a very thourough lesson in implementing the essential CPU codes of a limited system.


