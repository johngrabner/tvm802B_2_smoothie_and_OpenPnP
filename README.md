# TVM802B to smoothieboard/smoothieware and OpenPnP
TVM802B is a commercial low cost pick and place machine made by QiHe. This machine has 48 feeders, a down camera, a up camera and 2 nozzles.
The PC software (V2.35) and embedded controller are proprietary.

I have encountered issues with the SW such as not supporting Windows 10, inconsistent fiducial marker recognition, random re-homing, a User interface I find confusing, and poor to non-existing documentation.

This project will replace the embedded controller and driver with [smoothieboard](https://github.com/Smoothieware/Smoothieware) and replace the control SW with [OpenPnP](https://github.com/openpnp/openpnp).  

Once complete, a comparison test will be done against the original SW.

# Current Status:

Smothieboard now controls the Stepper and Solenoids.  

Working on reading of Vacuum Sensors.

Next up will be interfacing OpenPnP.

Queued is the reading of front panel buttons.

Queued is Bake Off
