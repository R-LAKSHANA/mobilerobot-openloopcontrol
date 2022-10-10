# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:

Initiate the MobileRobot.

Step2:

Connect your PC with the MobileRobot.

Step3:

Open Python program.

Step4:

Program the movements of the robot using python code.

Step5:

Execute the python program and record the movements.




## Program
```python
'''
Program to move the mobilerobot along the predefined path.
Developed by: R LAKSHANA
RegisterNumber: 22004909
'''
from robomaster import robot
import time

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led

    ep_led.set_led(comp="all",r=100,g=100,b=0,effect="on")
    
    ep_chassis.move(x=0.7, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=100,g=100,b=0,effect="on")   
    
    ep_chassis.move(x=0, y=0, z=-83, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=2.85, y=0, z=0, xy_speed=0.75).wait_for_completed()
    
    ep_chassis.move(x=0, y=0, z=85, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=100,b=100,effect="on")
    
    ep_chassis.move(x=2.5, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on")
    
    ep_led.set_led(comp="all",r=0,g=100,b=100,effect="on")
    ep_chassis.move(x=0, y=0, z=55, xy_speed=1).wait_for_completed()
    
    ep_chassis.move(x=3, y=0, z=0, xy_speed=0.75).wait_for_completed()
    
    ep_chassis.drive_speed(x=0.5,y=0,z=-20)
    time.sleep(14)
    ep_chassis.drive_speed(x=0,y=0,z=0)

    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

Initial Position:

![initial](/Initial_position.png)

Final Position:

![final](/Final.png)

## MobileRobot Movement Video:

https://youtube.com/shorts/t8nVyGZvT7w

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
