---
layout: post
title: Development
subtitle: Evolution and Troubleshooting History
#cover-img: /assets/img/IMG_4739.JPG
#thumbnail-img: /assets/img/IMG_4737.JPG
comments: true
---

We began this project with the initial idea of creating a gyro for a smartphone camera using the RP2040. From this initial idea is where we branched off to focus on creating it for the engine of a model rocket. Both of us have some background in aerospace engineering and rockets so we thought that this would be a more interesting alternative to a simple gyro.

The first step was to verify our proof of concept and test the idea using Python code.

We initially found some sample code to get the MPU6050 sensor read over I2C and a servo to turn using the PIO module. Links to these can be seen below:

[Default MPU Code](https://github.com/raspberrypi/pico-examples/tree/master/i2c/mpu6050_i2c)

[Default Servo Pio Code](https://www.hackster.io/naveenbskumar/raspberry-pi-pico-drive-servo-using-pio-d7a0e7)

From these baseline codes we began combining them and getting both servos to turn.
