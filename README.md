# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

### Step1:
Import necessary modules from the RoboMaster SDK.

<br/>

### Step2:
Check if the script is being run as the main module.

<br/>

### Step3:
Initialize the robot connection using "ap" (access point) mode.

<br/>

### Step4:
Get references to the robot's chassis, LED, and camera objects.

<br/>

### Step5:
Command the robot to move and change LED colors/effects at different positions:

i) Move the robot forward by 2.8 meters, set LED color to yellow.

ii) Move the robot up by 50 degrees, set LED color to purple.

iii) Move the robot forward by 0.6 meters, set LED color to yellow.

iv) Move the robot up by 55 degrees, set LED color to purple.

v) Move the robot forward by 0.6 meters, set LED color to yellow.

vi) Move the robot up by 62 degrees, set LED color to blue.

vii) Move the robot forward by 1.5 meters, set LED color to red.

viii) Move the robot down by 28 degrees, set LED color to green.

ix) Move the robot forward by 1.3 meters, set LED color to dark purple.

x) Move the robot up by 40 degrees, set LED color to magenta.

xi) Move the robot forward by 1.5 meters, set LED color to cyan.

xii) Move the robot up by 90 degrees, set LED color to dark green.

xiii) Move the robot forward by 1.8 meters, set LED color to dark blue.

xiv) Move the robot up by 55 degrees, set LED color to cyan.

xv) Move the robot forward by 0.5 meters, set LED color to light blue.

xvi) Move the robot up by 30 degrees, set LED color to light purple.

xvii) Move the robot forward by 0.5 meters, set LED color to light purple.

### Step6:
Wait for 4 seconds.

### Step7:
Close the robot connection.

<br/>

## Program
```python
from robomaster import robot
import time

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)


    ep_chassis.move(x=2.8,y=0,z=0,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=204,b=0,effect="on")

    ep_chassis.move(x=0,y=0,z=50,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=102,effect="on")

    ep_chassis.move(x=0.6,y=0,z=0,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=204,b=0,effect="on")

    ep_chassis.move(x=0,y=0,z=55,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=102,effect="on")

    ep_chassis.move(x=0.6,y=0,z=0,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=204,b=0,effect="on")

    ep_chassis.move(x=0,y=0,z=62,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=255,effect="on")

    ep_chassis.move(x=1.5,y=0,z=0,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=0,y=0,z=-28,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=1.3,y=0,z=0,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=102,g=0,b=102,effect="on")

    ep_chassis.move(x=0,y=0,z=40,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=1.5,y=0,z=0,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")

    ep_chassis.move(x=0,y=0,z=90,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=128,b=0,effect="on")

    ep_chassis.move(x=1.8,y=0,z=0,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on")

    ep_chassis.move(x=0,y=0,z=55,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")

    ep_chassis.move(x=0.5,y=0,z=0,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=204,b=255,effect="on")
    
    ep_chassis.move(x=0,y=0,z=30,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=102,b=255,effect="on")

    ep_chassis.move(x=0.5,y=0,z=0,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=204,b=255,effect="on")








    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")
    



    
    ep_robot.close()
```

## MobileRobot Movement Image:

![Alt text](image.png)

<br/>
<br/>
<br/>
<br/>

## MobileRobot Movement Video:



[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](https://youtu.be/LpNgazyLxsg)

<br/>
<br/>
<br/>
<br/>

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
