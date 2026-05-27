# GestureFly 
### ESP32-C3 Based Gesture-Controlled Micro Drone

## Quick Links

- [Build Log](docs/build-log.md)
- [Wiring Guide](docs/wiring.md)
- [Frame Design](docs/frame-design.md)
- [Bill of Materials](hardware/bom/bom.csv)
- [Journal](JOURNAL.md)
- [Zine](docs/zine/)



## Why I decided to build this?| A custom ESP32-C3 gesture controlled drone from scratch.


I really like building stuff using microcontrollers. I have build many projects such as an Automatic  fire fighting robot which sends signal to your phone depending on the type of emergencies and also alerts the users with call alerts. I have also built a custom carbon fiber frame drone which can be mainly used in the agricultural sector. Sadly I did not document any of these projects online.

While I was looking at the pictures of my old drone which I made from a carbon fiber frane with custom softaware and agricultural pov. I thought why can't I control drones through my hand gestures like they do in movies and so I got an idea of what I wanted to make. Having prior experiences with drones I knew controlling a full sized drone through my gestures wouldn't be easy and neither cheap so I landed upon a vague idea of how I wanted this project to be. I decided that My drone will be a micro drone preferrably under 180g and first it would be able to take flights controlled through my phone then my hand gestures since I knew it was gonna be easy I decided to divide my project into three stages.

## Current State

The electronics platform is currently functional.

Completed:
- ESP32-C3 bring-up
- MPU6050 I²C communication
- DRV8833 motor testing
- Motor spin verification
- 3D frame selection

Currently working on:
- Frame printing
- Stabilization firmware
- First hover tests


# Stage 1:

Get all the components needed to make this work and get them to sync with each other while keeping 3 things in mind.
- The overall of the drone shouldnt be more than 180g after assembly
- It should be under a very strict budget (cuz I'm broke lol)
- and last but not the least it shoudl atleast have stable hovering mechanisms with its center of gravity balances itself.
  
# Stage 2:
- Get the drone connected to my phone or another esp through the ESPnow protocol to hopefully be able to control it wirelessly through my phone or another esp.
- Then after a successfull hover controlled through my phone get a black box [Note- A black box is kind of a device that can telemetry and system information in real-time and send it over to my computer] in my drone so that I can trouble shoot any problems that occur either from telemetry or flight controls.

# Stage 3:
- The last and the final most valuable, important and my favourite part about this project make a gesture glove using a module like the MPU6050 a 6 axis gyroscope which can be used to track hand movements or get the droneto stabilize itself.
- Objective is to successfully control the drones left right yaw and roll through my gesture glove and make it work.
  I know its gonna be hard but it isnt gonna be impossible I have made a gesture controlled car before so Its going to be something similiar just a bit harder.

Here are the parts I am gonna use:



<img width="1429" height="900" alt="image" src="https://github.com/user-attachments/assets/868cacb2-be04-4e0b-beb3-016d7fac3ac5" />




### Custom Gesture drone

#### Goal 

Make the drone from scratch and keep the weight under 180g with the least amout of cost 

## COMPONENTS

- ESP32-C3 
- MPU6050
- 720 coreless motors
- DRV8833 Motor drivers
- 55mm propellers
- 800 mAh Li-Po Battery
- TP4056 Charging module
- JST Connectors

## Project Status

🟡 Planning Phase

- [x] Research Completed
- [x] Componenets ordered (Prototype)
- [x] Components delivered
- [x] MPU6050 Testing
- [x] Motors and drivers testing
- [x] Frame design
- [ ] First Hover attempt
- [ ] Gesture controller

## Planned features 
- MPU6050 for stabilization
- ESP32-C3 as a flight controller
- Custom 3-d Printed frame design
- Wireless control System
- Flight data logging (using a black box)

## Next Steps (Priority order)
1. Receive ordered components -  ✔
2. TEST the equipment such as ESP32-C3 - ✔
3. Test the MPU6050 FOR stabilization - ✔
4. Test motors with DRV8833 and thrust -  ✔
5. Design a frame in FUSION360 then print it - ✔
6. Implement codes for stabilization -  ✔
7. First Hover tests throught Mobile -
8. Flight Data Logging ( Make a black box of some sort) - 


  



