# Raptor2-UBL-LinearADV-4Corner
 FormBot Raptor Open Source Firmware

This firmware uses Unified Bed Leveling - So simply sending the printer G29 will not level the bed. To calibrate UBL, please follow the steps below: 

## UBL Calibration Process

1) Heat bed to desired temperature
2) Send G28 to printer to home. 
3) Send G29 P1 to printer to begin UBL calibration. Wait about 10-15 mins to complete.
4) Send G29 S1 to printer to save mesh in slot 1 
5) Send G29 A to printer to enable UBL
6) Send M500 to printer to save settings.

## UBL Start GCODE

To access the mesh you saved above, add the following to your start G-code after heating the bed: 

G28 
G29 L1 ; Load mesh 1
G29 A ; activate UBL
G29 J ; do a 3 point leveling.
