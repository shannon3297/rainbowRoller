Milestone 1!

Sunday:
We spent a long time trying to get an external LED to blink on the beagle bone. We realized we didn't have the right connectors, and we also couldn't figure out how to really run code on the beagle bone. For running code, we started out trying to ssh in and run things from the command line, but after lots of googling it seemed like using the cloud9 IDE was the way to go. We spent some time messing around with that and then decided that we were going to switch to an mBed. We initially chose to use the beagle bone when we thought we would need wifi, which we no longer need, and the mbed is much smaller.

Monday:
We wrote code to have pressure sensors and an accelerometer control state LEDs. The pressure sensor turns on the red LED when it's being pressed, and the blue LED when it isn't being pressed. This isn't the actual pressure sensor we will use for the final project, but it helped us think through the logic of the project and write some of the code. The accelerometer flashed an LED red when it sensed acceleration in the x-direction, and put on the blue LED when it didn't.

We tried to start writing code that could use the accelerometer data to sense when specifically the roller was turning. I was thinking that it would a combination of two axes, but when we started actually trying to write it seemed very difficult. After talking to Kim, we realized we should actually be using a gyroscope, so we got one from Detkin.

Tuesday: 
We figured out how to use the gyroscope! The state LEDs now show when the board is being rotated. 

Here's a picture of our circuit as of today (with the pressure sensors unattached):
![First Circuit, right click to view](https://github.com/shannon3297/rainbowRoller/blob/master/assets/milestone1.jpg)

We just got a lot of parts in, so going forward towards next week we're hopefully going to start integrating our actual parts. First step is figuring out how to use the pressure sensing sheet, which I think we can do with a voltage divider. 

Milestone 2:
Fully armed with all our parts, we successfully coordinated the gyroaccelerometer, pressure sensor, and LED strip to respond 
to user inputs. Initally, we were able to get the gyroscope to print out values independently, the pressure sensor to print out values independently, and are able to control the LED strip to light up how we wanted. The LED strip was a challenge because there is not much official documentation or data sheets, but we were able to figure it out based on many different sources online. The big problem we ran in to is that when we tried to integrate any of the parts together, the mbed had a HardFault and would crash. Turns out all we needed to do was take out print statements.

We talked with Dr. Nalaka on Monday about the specific requirements he had. With where we are right now, he thought that giving feedback to the user through the LED strip was a good implementation. We discussed a specific rolling routine with him, and agreed to implement 30 seconds stationary on the muscles group, and then 30 seconds of rolling. He also recommended that we focus on one specific muscle group, such as the calf. 

Moving forward, there were two main features/changes he was interested in that we didn't quite have. The first was some sort of data collection - he would really like some way to get the data back to the physician about how frequently, and for how long, the patient is rolling. We're still unsure how to include this, but we would like to include it somehow. The other change he was interested in is increased resolution in the pressure readings. Right now, we can only tell whether or not there is pressure on the roller, but it would be very useful to tell the difference between different amounts of pressure. 

In the hopes of increasing resolution, we decided to cut the pressure sensor into strips that would fit well onto the roller. We also double the strip over (connecting the sides with electrical tape) based on the suggestions of another group. We are planning to use an analog mux to read in the values of the different strips. This increased the sensitivity a little bit, but we are still looking for a better way to measure different levels of pressure.

Here is a picture of our base circuit:
![Base Demo Circuit, right click to view](https://github.com/shannon3297/rainbowRoller/blob/master/assets/circuit2.JPG) 

We also moved the circuit to a smaller breadboard in preparation for putting it inside the roller, here's a picture of that:


Moving forward, we are aiming to finish integrating these parts into one on the roller. We plan to discuss a way to bring our project up to the next level with Dr. Rahul tomorrow. We currently envision personalizing a rolling routine based on the target muscle group and body type and/or improving on data collection and data output feedback.

Baseline Demo:
This week, we focused on design implementation and worked to develop a more compact system. To do so, we teamed up with Hal who helped us drill a slit through the roller so that we could tuck the flaps of the pressure sensor inside and continue to use alligator clips to connect pressure readings to the mbed. We also successfully powered the entire system with a battery pack also hidden inside the roller. Moving forward, we are looking to experiment with the placement of the LED strip, though we are finding that the lights are bright and give feedback well when laying horizontal to the roller. 
![Baseline Product, right click to view](https://github.com/shannon3297/rainbowRoller/blob/master/assets/baseline.png)


Talk about meeting with Rahul and Sarah Rottenberg
