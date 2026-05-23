
###May 20, 2026

I got the idea of building a drone while I was viewing some photographs of mysdelf at an Ideathon from last year where I won the first prize for my custom carbon fiber frame drone which could be used for surveillance in agriculture and providing fertilizers to the plants from above. I thought I could control a drone using my hand gestures and So I got to work

I researched a little bit and found about the components I would need for the build and the technology I could add to it etc 

May 21, 2026

I decided I would Order all the required parts for the projects today and therefore I got to work. I first compared which motors would be the best for my drone and so I shortlisted 4 models 614,615,716 and 720 mm motors these are like  the dimesnions of the motors such as a 720 motor is 7*20 mm. And since I wanted to make a micro drone under a budget I decided to choose 720 motors for this build as they were in the sweet spot for power consumption and thrust generation required for this aircraft.

Then I moved onto choosing the perfect flight controller for my drone and since I wanted it to be a micro drone from scratch I did not get a pre coded flight controller rather I chose the ESP32-C2 Super Mini Development Board as the mini version is very compact and is perfer for my custom micro drone build since it has Wi-Fi capabilities.

I Also chose a 3.7 V 800 mAh Lithium-Polymer Rechargeable Battery since it is very comapct and yet perfect for this build due to its light weight and 800 mAh capabilities.

I also included two MPU6050 3-Axis gyroscopes since they would help the drone to stabilize and take readings and one of them would be at my gesture controller glove which I would use to control my drone.



Till now the electronics chosen are as follows:
 - ESP32-C3 (Lightweight and compac, with integrated Wi-Fi support suitable for futur wireless control)
 - MPU6050 (6 Axis IMU providing accelerometer and gyroscpe data for stabilization and orientation estimation)
 - DRV8822 Motor drivers  (will be used to drive the brushed motors, with each driver controlling two motors)
 - 800 mAh LiPo battery (sweet spot between efficiency and power for a micro esp drone)


Final outcomes of this research:

- The drone will use brushed motors (720) with 55 mm props
- First a stable flight will be achieved then will develop the gestrue based control.
- Frame will also be custom designed and 3-d printed
- weight of the drone would be under 180 grams.

Components have been ordered and the total time spent doing all this was ~6 hours.



May 22, 2026 

Started Learning Githun and project documentation 

###GitHub
- Created first repository
- learned committs
- Created a readme
- Created a documentation folder
- Added a Bom file
- Added wiring documentation
- Added frame design notes

### Electronics Practices 

- Practiced soldering on some pcb boards
- Tested ESP modules
- Established and Esp Now connection for testing
- Built a Wi-Fi control webpage
- Debugged an old arduino for future projects

### Todays's Progress 
- Created Repository and made some folder ( did not write anything yet)
- Started documentaion

**Total time spent: ~ 2 hours 

### Next steps 

- Receive ordered components
- verify MPU6050 communication
- Test DRV8833 MOTOR drivers
- Design first drone frame concept in CAD
- do some research ont he stabilization softwares required for this drone like Ardupilot.

