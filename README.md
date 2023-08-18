# MMA8452Q_STM32
A STM32 port for the MMA8452Q three axis accelerometer.

The motivation for the creation of this library was the lack of such in the publicly available github repositories.
This library was ported from arduino code to embedded C, with the STM32 HAL library functions for the I2C functionalities.

I used the fast mode I2C (400KHz) and i2c1 to read the values. You can change the i2c handler in the .h file to support your own device. You should also change the included hal library according to your device. For example, the STM32F091 needs "stm32f0xx_hal.h" to be included. 

This is a work-in progress library, so there might be errors regarding the usage of this library.
Right now the only proven functionality is the MMA_read and Init functions. Other functions might not work as expected.
