# This is a ESP32 Micropython library for the MPL3115A2 Altimeter

## HOW TO USE THIS LIBRARY
---

On the ESP32 pin 21 is SDA and pin 22 is SCL

Create the MPL object in altitude mode (mode 0)

    mpl = MPL3115A2(sda=Pin(21), scl=Pin(22), mode=0)

to read the altitude and temperature

    altitude = mpl.altitude()
    temperature = mpl.temperature()
    
Create the MPL object in pressure mode (mode 1)

    mpl = MPL3115A2(sda=Pin(21), scl=Pin(22), mode=1)

to read the pressure and temperature

    pressure = mpl.pressure()
    temperature = mpl.temperature()

