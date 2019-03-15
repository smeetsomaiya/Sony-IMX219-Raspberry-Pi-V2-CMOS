# Temperature Sensor sampling attempt, Sony-IMX219-Raspberry-Pi-V2-CMOS

# Update

Stopped working on this, since the low-level driver is not open source. Hence we cannot modify the register values to enable/configure the inbuilt temperature sensor.

# Goal of the project:

I have an RPi camera with a temperature sensor on it. 

The goal is to modify firmware to sample the temperature sensor as frequently as we can, while operating the camera under different scenarios such as active mode and idle mode.

The idea is to make appropriate changes in the kernel side and possibly add a new IOCTL command to read the sensor temperature. From the user space, V4L2 is the high-level driver for camera control and configuration, which in turn has a low-level driver to directly configure the camera registers. Perhaps the first step is to find out the current low-level driver that is being used so that you can make necessary changes to add the temperature support and add more changes all the way up to the user space.



Forked Sony IMX219 Raspberry Pi V2 CMOS Datasheet and Source Code
