---
layout: post
title: Project Overview
subtitle: Breif Introduction and Overview
cover-img: /assets/img/IMG_4739.JPG
thumbnail-img: /assets/img/IMG_4737.JPG
comments: true
---



## Table of Contents

1. [Project Overview and Introduction](https://ese519teamgimbal.github.io/2022-12-27-Introduction/)
2. [Components and Assembly Details](https://ese519teamgimbal.github.io/2022-12-26-Instructions/)
3. [Development and Troubleshooting](https://ese519teamgimbal.github.io/2022-12-25-Development/)
4. [PIO Module and Conclusion](https://ese519teamgimbal.github.io/2022-12-24-PIO/)
5. [Design Reflections and Future Plans](https://ese519teamgimbal.github.io/2022-12-23-Reflections/)
6. [Team Bio](https://ese519teamgimbal.github.io/aboutme/)

## Other Important Links
1. [Datasheet](https://datasheets.raspberrypi.com/pico/raspberry-pi-pico-c-sdk.pdf)
2. [SDK Install Guide](https://github.com/mvpeters/ESE-5190-Guides/blob/main/ESE5190-Lab2-Setup-Windows.md)
3. [Midpoint Repo](https://github.com/mvpeters/ESE519-Team-Gimbal-Midpoint)
4. [Final Code](https://github.com/ESE519TeamGimbal/Project-Code)


## Introduction


We are Team Gimbal and for our ESE519 Final Project we created a rocket engine stabilizer using the C SDK and the Adafruit QT Py RP2040. During a model rocket launch the goal is to have the rocket stay as vertical as possible so it can reach the highest possible altitude. However, there are usually a variety of factors that can cause it to drift slightly and redude altitude. Our gimbal is designed to be attached around the engine inside a model rocket and provide counter forces to stabilize the engine.

<iframe width="389" height="774" src="https://user-images.githubusercontent.com/114199773/210104405-ba835d42-da17-481c-b8f5-0b03fc46ebdc.mp4" frameborder="0"> </iframe>




We accomplished this by attaching an MPU6050 accelerometer and gyro sensor to the inside of the rocket to measure any angle changes the body of the rocket experiences. This sensor data is then fed into the Adafruit QTPY RP2040 microcontroller for processing. The microcontroller calculates any drift experienced by the rocket and uses that information to control two servo motoros that are used to counter the forces the rocket is experiencing so the engine maintains stability. These servos are held in a customly designed and 3-D printed gimbal stand that along with all the other electronics can be easily fitted inside a rocket for actual use. An important note about the video above is the first breadboard, battery pack, and wires are all for the LEDs we used to illuminate the inside and are not necessary. For actual use of our design only the power supply and wires associated with it are necessary. 
