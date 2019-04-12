Milestone 1!

Sunday:
We spent a long time trying to get an external LED to blink on the beagle bone. We realized we didn't have the right connectors, and we also couldn't figure out how to really run code on the beagle bone. For running code, we started out trying to ssh in and run things from the command line, but after lots of googling it seemed like using the cloud9 IDE was the way to go. We spent some time messing around with that and then decided that we were going to switch to an mBed. We initially chose to use the beagle bone when we thought we would need wifi, which we no longer need, and the mbed is much smaller.

Monday:
We wrote code to have pressure sensors and an accelerometer control state LEDs. The pressure sensor turns on the red LED when it's being pressed, and the blue LED when it isn't being pressed. This isn't the actual pressure sensor we will use for the final project, but it helped us think through the logic of the project and write some of the code. The accelerometer flashed an LED red when it sensed acceleration in the x-direction, and put on the blue LED when it didn't.

We tried to start writing code that could use the accelerometer data to sense when specifically the roller was turning. I was thinking that it would a combination of two axes, but when we started actually trying to write it seemed very difficult. After talking to Kim, we realized we should actually be using a gyroscope, so we got one from Detkin.

Tuesday: 
We figured out how to use the gyroscope! The state LEDs now show when the board is being rotated. 

Here's a picture of our circuit as of today (with the pressure sensors unattached):
~ lol jk gonna figure out how to put a picture in ~

We just got a lot of parts in, so going forward towards next week we're hopefully going to start integrating our actual parts. First step is figuring out how to use the pressure sensing sheet, which I think we can do with a voltage divider. 
