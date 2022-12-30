---
layout: post
title: Development
subtitle: Evolution and Troubleshooting History
cover-img: /assets/img/DevelopmentCOVER.JPG
thumbnail-img: /assets/img/DevelopmentCOVER.JPG
comments: true
---

We began this project with the initial idea of creating a gyro for a smartphone camera using the RP2040. From this initial idea is where we branched off to focus on creating it for the engine of a model rocket. Both of us have some background in aerospace engineering and rockets so we thought that this would be a more interesting alternative to a simple gyro.

The first step was to verify our proof of concept and test the idea using Python code. Both of us have had prior experience with Python, collecting sensor data, and turning servos so to test our idea we deceided to do our initial draft using python for the bulk of the coding. With some work and preexisting python libraries we were able to pretty quickly get the MPU gyro sensor reading and turning the servos in all three axis of rotation. It did this by taking a measurment in radians/second and converted this into degrees. This degree value was then added or subtracted to the current servo reading to turn the servo the same amount the sensor moved. See below for a breif video of our midpoint design verification. Each of the three servos represents a different axis of rotation (X, Y, Z).



![MidpointGif](https://user-images.githubusercontent.com/114199773/210019229-04e302cc-0c6a-4adb-8808-961d9fab36dd.gif){: .mx-auto.d-block :}


[Midpoint Repo](https://github.com/mvpeters/ESE519-Team-Gimbal-Midpoint)


This design had a few issues such as the gyro not being perfectly zerod or the value exceeding the 180 degree limit of a servo motor. We chose to move on from the python code however without fixing these issues as they would be addresses in the final C code. From here we knew that the components and code could achieve what we were looking for, it was just a matter of transitioning our code to use C and the PIO module. To do this we initially found some sample code to get the MPU6050 sensor read over I2C and a servo to turn using the PIO module. Links to these can be seen below:

[Default MPU Code](https://github.com/raspberrypi/pico-examples/tree/master/i2c/mpu6050_i2c)

[Default Servo Pio Code](https://www.hackster.io/naveenbskumar/raspberry-pi-pico-drive-servo-using-pio-d7a0e7)

From these baseline codes we began combining them and getting both servos to turn identically to how we did with the python code previously. We deceided to only work with two axis of rotation (X & Y) as it would make the design simpler, lighter, and the X axis does not help in stability much given the rocket is elevating anyway. The code uses the STEMMA QT cable and I2C connection to get readings from the sensor. This data feeds into the PIO module 0. The module uses state machines 0 & 1 to each control each servo. We were also able to fix our previous issues of the servos turning too much by implementing a simple if statement loop. We were also able to fix the sensor nt being acurately zerod by adding or subtracting this small offset so our readings were more accurate.
