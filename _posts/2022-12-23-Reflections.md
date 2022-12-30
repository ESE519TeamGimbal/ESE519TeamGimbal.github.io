---
layout: post
title: Design Reflections
subtitle: Reflecting on our Design and Future Plans
cover-img: /assets/img/GimbalRendered1.png
thumbnail-img: /assets/img/3DPRINTSS2.JPG
comments: true
---

## Design Reflections:

Overall we were happy with how our final project turned out. We feel that the electric components selected fit the design very well and were simple enough that someone could recreate our design if they wanted. The 3-D printed components also were designed well so that they were light and the electronics fit into them well. I think we were very satisfied with how few components we needed to make the design and with how responsive it was. Any slight movement seemed to be instantly accounted for by the servos. There was little to no delay which we were excited about and many people commented on during our demo.


## Future Changes:

If we were to repeat the design I think adding a 3-D printed shelf of some sort on top of the gimbal for the power supply and battery would be a nice addition. Since in theory the design is meant to be inside a working rocket it would be nice to have a shelf to place the electronics that don't snap into the gimbal. 

Next having more time to configure the electronics for accuracy. As we discussed on the project demo day there is some amount of drift that occurs over time on the gimbal. Adding some sort of zero point to the design to prevent drift could be a nice addition. Also updating the code so it better tracks when it goes past the servo angle limits. Right now it just sets the servos to their max or min value if it goes over the limit so that the chip doesn't produce too much current and fry itself. The problem is that this current setup causes drift if the servo maxes out. Adding an additional variable to the code to track this drift could be a useful addition.

Finally, it would be cool to actually test our design in a read rocket and get some sort of data showing the stability it provides. This was our original plan but due to the limited time frame of the class, delays in the rocket engines being shipped, and concerns over launching our only design hundreds of meters in the air we never got the opportunity.
