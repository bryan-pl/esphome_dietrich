# Dietrich MCX PLUS (Remeha) Boiler connectivity using ESP8266 with ESPHOME

!Warning! This will not work in ESPHOME 2025.2.0 as the service of custom components were withdrawed. Module needs to be rewritten to external component. 

!Forked from kakaki/esphome_dietrich to provide full compatibility with my instance of HA and DeDietrich MCX PLUS.

The board used - Adafruit Huzzach - due to smaller current draw (no usb interface on board) and +5v compatible uart RX pin.


Library for reading data from De Dietrich (or Remeha) PC interface, tested with model mcr3.
For this we use an ESP8266 (Wemos D1) with ESPHOME software - sample YAML files are in English and Polish.

It connects to the boiler using a 4P4C (RJ10) connector with the following pinouts:
```
 Heater Board from top       ESP8266
    4P4C RJ connector
    
       +---------+
GND 4  ---       +--+        GND
TXD 3  ---          |        RX
RXD 2  ---          |        TX
5V  1  ---       +--+        5V
       +---------+
```

I have connected ESP to prototype board with pins, on board there was simple voltage divider (1kΩ / 2kΩ) to change power from 5V to 3V, but on my board it was not needed and i have connected pins directly to Dietich MCR33, .
Cable is simple phone cord, cut and added pin connector to it.

Screenshot of board connected to boiler.

![Screenshot](board.jpg)

And in printed box.

![Screenshot](box.jpg)

Thanks to great work from https://github.com/rjblake/remeha - for creating maping of data in excel file.

