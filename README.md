# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:
Use from robomaster import robot

Step2:
choose the x,yz axis movement

Step3:
Give ep_chasis.move to move straight

Step4:
Give time.sleep() for a break

Step5:
Give ep_chasis.drive_speed to have a circular movement

## Program
Developed by: Yuvaraj V
Ref no:23013769

from robomaster import robot
import time
from robomaster import camera
if name == 'main':
ep_robot = robot.Robot()
ep_robot.initialize(conn_type="ap")
ep_chassis = ep_robot.chassis
ep_led = ep_robot.led
ep_camera = ep_robot.camera
print("Video streaming started.....")
ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)
ep_chassis.move(x=2.6, y=0, z=0, xy_speed=1.2).wait_for_completed()
ep_led.set_led(comp = "all",r=255,g=255,b=255,effect="on")
ep_chassis.move(x=0.3, y=0, z=80, xy_speed=1.2).wait_for_completed()
ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
ep_chassis.move(x=1.02, y=0, z=0, xy_speed=1.2).wait_for_completed()
ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")
ep_chassis.move(x=0, y=-1.45, z=0, xy_speed=1.2).wait_for_completed()
ep_led.set_led(comp = "all",r=0,g=0,b=255,effect="on")
ep_chassis.move(x=0, y=0, z=-118, xy_speed=1.2).wait_for_completed()
ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")
ep_chassis.move(x=-1.55, y=0, z=0, xy_speed=1.2).wait_for_completed()
ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")
ep_chassis.move(x=0, y=0, z=-48, xy_speed=1.2).wait_for_completed()
ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")
ep_chassis.move(x=0, y=1.4, z=0, xy_speed=1.2).wait_for_completed()
ep_led.set_led(comp = "all",r=128,g=0,b=0,effect="on")
ep_chassis.move(x=2, y=0, z=0, xy_speed=1.2).wait_for_completed()
ep_led.set_led(comp = "all",r=0,g=128,b=0,effect="on")
ep_chassis.move(x=0, y=0, z=85, xy_speed=1.2).wait_for_completed()
ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")
ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1.2).wait_for_completed()
ep_led.set_led(comp = "all",r=153,g=51,b=102,effect="on")
ep_chassis.move(x=0, y=0, z=0, xy_speed=1.2).wait_for_completed()

ep_led.set_led(comp = "all",r=51,g=153,b=102,effect="on")
time.sleep(4)
ep_camera.stop_video_stream()
print("Stopped video streaming.....")
ep_robot.close()

## MobileRobot Movement Image:

![robo](./img/robomaster.png)
![293392563-023e18bd-f597-45be-9da2-2a885bc70773](https://github.com/YuvarajVB/mobilerobot-openloopcontrol/assets/151488375/bd62e605-1963-4735-ae26-14f3ada2ef5a)

![293392649-b7588c6b-4569-4501-87c7-67fd7882fb60](https://github.com/YuvarajVB/mobilerobot-openloopcontrol/assets/151488375/a3bacffd-d61e-4ede-bd36-fbd7dd61d5f7)


## MobileRobot Movement Video:
https://youtube.com/shorts/XhjSTCJpYnU?si=1geJ62jxv78Nf-0K

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.
```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
