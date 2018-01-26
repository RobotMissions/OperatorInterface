# Operator Interface v1.0

![Robot Missions logo, a green leaf on a white diamond situated within a purple circle](http://robotmissions.org/images/github/robot_missions_colour_500px.png)

The Operator Interface library allows control via a custom hardware interface for the [Robot Missions](http://robotmissions.org) robot platform.

### More information about our robot platform at the [Robot Missions Website ➞](http://robotmissions.org)

Compatible with [Teensy 3.2](https://www.pjrc.com/store/teensy32.html), and [Teensy LC]([Teensy 3.2](https://www.pjrc.com/store/teensy32.html)) (with an external 3.3V regulator).

![Two of the Operator Interfaces, with the LEDs glowing, and display showing 'Robot Missions Hero!'](http://robotmissions.org/images/github/robot_missions_operator_interface.jpg)

## Required Libraries

You will need to have these libraries installed:

* [Bounce2](https://github.com/thomasfredericks/Bounce2)
* [Adafruit_GFX](https://github.com/adafruit/Adafruit_GFX)
* [Adafruit_SSD1306](https://github.com/adafruit/Adafruit_SSD1306)
* [Streaming](http://arduiniana.org/libraries/streaming/)
* [PromulgateBig](https://github.com/RobotGrrl/PromulgateBig)
* [Xbee](https://github.com/andrewrapp/xbee-arduino)
* SPI _Included with Arduino_
* Wire _Included with Arduino_

## Display

You need to make modifications in order for the display to work. The Operator Interface uses the [Adafruit 128x64 OLED display](https://www.adafruit.com/product/938).

**Solder jumpers**

The Operator Interface uses I2C to communicate with the display. On the back of the display, you will need to solder `SJ1` and `SJ2`. (See [this photo](https://cdn-shop.adafruit.com/1200x900/938-13.jpg)) 

**Fix library**

The `Adafruit_SSD1306` library hard codes in the dimensions of the display. By default, it will stretch what we are displaying because of the incorrect dimensions. 

1. On line `73` of `Adafruit_SSD1306.h`, uncomment `#define SSD1306_128_64`
2. Comment out line `74` and `75`

Now the display should be good to go.

## Bill of Materials

For assembling the Operator Interface, you can find the [BOM here](https://github.com/RobotMissions/OperatorElectronics/blob/master/pcb/operator-interface-bom-r1.1.md).

## License

Code is released under the [MIT license](https://opensource.org/licenses/MIT).

## Bug Reports / Feature Requests

Found a bug? Looking for a feature? Let us know by opening an Issue report. Further questions can be posted to our [forum](http://forum.robotmissions.org).

---

🤖✌️🌎

**Robot Missions - Helping the planet with robots**
