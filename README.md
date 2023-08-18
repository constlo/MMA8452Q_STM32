# MMA8452Q_STM32
A STM32 port for the MMA8452Q three axis accelerometer.

This library was ported from arduino code to embedded C, with the STM32 HAL library functions for the I2C functionalities.
The original repository(https://github.com/RoboCore/RoboCore_MMA8452Q) is written for arduino, from which i took the functions and modified them to suit my need for the STM32 Platform.
The license of the original library was LGPL, so consider this library to be LGPL as well.

This is a work-in progress library, so there might be errors regarding the usage of this library.
Right now the only proven functionality is the MMA_read and Init functions. Other functions might not work as expected, or may not work at all.

I used the fast mode I2C (400KHz) and i2c1 to read the values. You can change the i2c handler in the .h file to support your own device. You should also change the included hal library according to your device. For example, the STM32F091 needs "stm32f0xx_hal.h" to be included.
