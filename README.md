# WRO_2021-
The machine is designed on the basis of a wheelbase and is controlled by a Raspberry Pi board, the base is powered by a battery. Also, the camera and ultrasonic sensors located in the front of the machine allow it to navigate in space. The camera detects the presence of an obstacle by its color (it is set to red and green). Ultrasonic sensors located on the sides, as well as in the front of the machine determine the distance from the sides.

Used stuff and its description:

The ultrasonic sensor (HC-SR04 module): uses acoustic radiation to determine the distance to an object. This non-contact sensor ensures high measurement accuracy and stability. The measurement range is: from 2 cm to 400 cm.

Raspberry Pi: is a miniature single-board computer that can easily fit in the palm of an adult. Despite its modest size, the board has high performance, which allows it to reach the same level as desktop PCs.

The L293D: provides power separation for the chip and for the motors controlled by it, which allows you to connect electric motors with a higher supply voltage than that of the chip.

The Raspberry Pi Camera Module v2: equipped with an eight-megapixel Sony IMX219 Exmor sensor, which allows you to capture, record and broadcast video in 1080p, 720p and VGA formats. For photos, the maximum frame resolution is 3280×2464 pixels.

Power supply system: It is based on a portable powerbank for (I don't know exactly yet) recharging. Size (something)x (something)

The mechanical basis of the robot is two-wheeled with a differential drive — it has 2 independent wheels and its movement is controlled exclusively by the speed and direction of their rotation. In addition to the actual wheels, there is a ball/wheel support, in advanced systems-encoders for feedback and control of the current speed of the engines, which allows more efficient control of the engines.

On the first round, the car is required to drive three laps and stop. The solution developed by us will be launched via the built-in button that also starts the wheel mechanism. The program code for this stage is written separately for each completed segment of the path. An example of the prescribed program code is below:

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

As you can see above, for convenience, 4 functions were created – for driving forward, turning right and left, and for stopping, with the corresponding names: motors, motors_right, motors_left, motors_stop.


