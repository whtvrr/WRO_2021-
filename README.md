# WRO_2021-
The machine is designed on the basis of a wheelbase and is controlled by a Raspberry Pi board, the base is powered by a battery. Also, the camera and ultrasonic sensors located in the front of the machine allow it to navigate in space. The camera detects the presence of an obstacle by its color (it is set to red and green). Ultrasonic sensors located on the sides, as well as in the front of the machine determine the distance from the sides.

On the first round, the car is required to drive three laps and stop. The solution developed by us will be launched via the built-in button that also starts the wheel mechanism. The program code for this stage is written separately for each completed segment of the path. An example of the prescribed program code is below:
"
while True:

  if (QWE.input(21)):
    while(1):
      motors(100, 100)
      time.sleep(2.7)
      motors_left(100, 100)
      time.sleep(0.23)
      
      motors(100,100)
      time.sleep(2.9)
      motors_left(100, 100)
      time.sleep(0.34)
      
      motors(100,100)
      time.sleep(3.3)
      motors_left(100, 100)
      time.sleep(0.25)
      
      motors(100,100)
      time.sleep(3.3)
      motors_left(100, 100)
      time.sleep(0.25)
      
      motors(100,100)
      time.sleep(1.2)
      motors_stop(0,0)
      break
"
As you can see above, for convenience, 4 functions were created – for driving forward, turning right and left, and for stopping, with the corresponding names: motors, motors_right, motors_left, motors_stop.


