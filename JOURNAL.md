# JOURNAL

## May 21, 2026

Got the project idea and started researching how micro drones work and how I can control them through a gesture based command.

### Research
- Learned about brushed micro drone architecture
- Compared motor options (614, 615, 716, 720)
- Compared motor specifications and selected 720 coreless motors
- Selected 55mm propellers

### Electronics Chosen
- ESP32-C3 (lightweight and compact, with integrated Wi-Fi support suitable for future wireless control)
- MPU6050 (6-axis IMU providing accelerometer and gyroscope data for stabilization and orientation estimation)
- DRV8833 motor drivers (used to drive the brushed motors, with each driver controlling two motors)
- TP4056 charging module (used for charging and protecting the single-cell LiPo battery)
- 800mAh LiPo battery (sweet spot between weight and efficiency of power for an esp based micro drone)

### Decisions
- Drone will use brushed motors
- Gesture controller will be developed after achieving stable flight
- Frame will be custom designed and 3D printed

### Progress
- Components researched
- Components ordered

**Total time spent:** ~6 hours


## May 22, 2026

Started learning GitHub and project documentation.

### GitHub
- Created first repository
- Learned commits
- Created README
- Created documentation folder
- Added BOM file
- Added wiring documentation
- Added frame design notes

### Electronics Practice
- Practiced soldering
- Tested ESP modules
- Established an Esp Now connection for testing
- Built a Wi-Fi control webpage
- Debugged an old arduino nano for future projects

### Progress
- Repository structure established
- Project documentation started

**Total time spent:** ~4 hours

### Next Steps

- Receive ordered components
- Verify MPU6050 communication
- Test DRV8833 motor control
- Design the first drone frame concept
- Begin stabilization software research
