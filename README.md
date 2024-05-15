# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

### STEP 1: Initialize Robot and Components:
Import necessary modules from robomaster.
If the script is being run directly:
    Initialize the robot and its components: chassis, LED, and camera.
### STEP 2:Start Video Streaming:
Start the video streaming from the robot's camera with specified parameters.
### STEP 3:Execute Movement and LED Commands:
Execute a series of movement commands for the chassis to move the robot in various directions.
Set LED colors and effects corresponding to each movement.
### STEP 4:Stop Video Streaming and Close Connections:
After completing all movements and LED effects:
    Stop the video streaming.
    Close the robot connection.
### STEP 5:Main Execution Flow:
Wrap the main code logic inside a conditional block to ensure it only runs when the script is executed 
## Program
```python
#Developed by : Vignesh S
#Register number : 212223230240
from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.5, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=255,effect="on")

    ep_chassis.move(x=0.5, y=0, z=75, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=100,b=0,effect="on")

    ep_chassis.move(x=0.9, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")
    
    ep_chassis.move(x=0, y=-0.1, z=70, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=.5, y=0, z=30, xy_speed=.7).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=102,b=255,effect="on")

    ep_chassis.move(x= 1, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")

    ep_chassis.move(x= 0, y=0, z=-35, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=0,effect="on")

    ep_chassis.move(x= 1.5, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=192,b=203,effect="on")

    ep_chassis.move(x= .1, y=0, z=40, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=204,b=255,effect="on")

    ep_chassis.move(x= 1.5, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=128,b=128,effect="on")

    ep_chassis.move(x= 0, y=0, z=95, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")
    
    ep_chassis.move(x= 2.1, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

 
    ep_chassis.move(x=0, y=0, z=80, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=143,g=0,b=255,effect="on")


    ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=0,effect="on")


    ep_chassis.move(x=0, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=100,b=0,effect="on")

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()


    
    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

Insert image here


<br/>
<br/>
<br/>
<br/>

## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

https://youtu.be/geEYPoYfX5Y

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
