# This is a MicroPython library for the MPL3115A2 Altimeter

## How to use this library

E.g. on the ESP32 pin 21 is SDA and pin 22 is SCL

Create a I2C object with the pins according to your design.

   from machine import I2C
   i2cbus = I2C(sda=Pin(21), scl=Pin(22))

Create the MPL object in altitude mode (mode 0)

    from mpl3115a2 import MPL3115A2
    mpl = MPL3115A2(i2cbus, mode=MPL3115A2.ALTITUDE)

to read the altitude and temperature

    altitude = mpl.altitude()
    temperature = mpl.temperature()
    
Create the MPL object in pressure mode (mode 1)

    from mpl3115a2 import MPL3115A2
    mpl = MPL3115A2(i2cbus, mode=MPL3115A2.PRESSURE)

to read the pressure and temperature

    pressure = mpl.pressure()
    temperature = mpl.temperature()

