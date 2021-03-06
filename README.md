# Project Aelith Digital Controller
=================================

An embedded control system targeted to RC model cars which feature individual wheel drive. This controller allows for software differentials and power delivery with the aid of various sensors on the vehicle. Currently the system makes use of wheel speed sensors and a 6 axis IMU for real time processing.

Overview Video: http://youtu.be/ET1HEyqEQJQ

The controller communicates to a steering servo and four brushless DC motor controllers. It also listens to a standard RC radio receiver for user input, as well as a serial port for telemetry over wireless modules such as xbee or bluetooth.

It's hoped that this project allows for advanced features such as traction control, under/over steer detection, adaptive power delivery and real-time telemetry.

The system runs on Cortex M4 STM32F4 devices by ST microelectronics. To build this project, you will need the ARM-GCC compiler found here:

https://launchpad.net/gcc-arm-embedded

As well as the STLink driver for uploading to a development board such as the STM32F4Discovery board:

http://www.st.com/web/en/catalog/tools/FM146/CL1984/SC724/SS1677/PF251168

To enable debugging, GDB is required and can be found here:

http://www.emb4fun.de/archive/stlink/index.html

The make.bat file is able to run under Windows to compile, upload and start the debug server. Please ensure that your PATH environment variable are set up in windows for the batch commands to be recognized.


Control System
--------------
The control system for the project is designed in Simulink and can be exported as C code using the embedded coder module. Granted this is the only part of the project that requires a non free software, the exported code however is still in readable C. Useful resource: http://www.mathworks.co.uk/hardware-support/arm-cortex-m-cmsis.html and http://www.mathworks.co.uk/hardware-support/st-discovery-board.html

PCB Info
--------

The hardware used in the project is custom. To see the Schematic, Gerber and Diptrace project files, please see the PCB folder.
Bare boards are available to order at: https://oshpark.com/shared_projects/t9Uw3F4U


CAD Designs
-----------

I'll upload full documentation soon on how to modify a Schumacher Mi5 chassis to support four motors, in the meantime, the CAD files for motor mounts, couplings and suspension mounts can be found in the mechanical folder


Copyright
---------

Copyright (C) 2014 Rajesh Nakarja. All rights reserved
http://www.naklojik.com

This is free software; you can redistribute it and/or modify it under the 
terms of the GNU Lesser General Public License version 3.0.
http://opensource.org/licenses/lgpl-3.0.html