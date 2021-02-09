## Adafruit AW9523 GPIO Expander and LED Driver PCB

<a href="http://www.adafruit.com/products/4886"><img src="assets/4886.jpg?raw=true" width="500px"><br/>
Click here to purchase one from the Adafruit shop</a>

PCB files for the Adafruit AW9523 GPIO Expander and LED Driver. 

Format is EagleCAD schematic and board layout
* https://www.adafruit.com/product/4886

### Description

Expand your project possibilities, with the Adafruit AW9523 GPIO Expander and LED Driver Breakout - a cute and powerful I2C expander with a lot of tricks up it's sleeve.

GPIO expanders work like this: you have a board with some number of GPIO but not enough for your project - maybe you need more buttons or LEDs. You could upgrade to a board with massive number of GPIO like the Grand Central, or you could pop on one of these boards. Connect it over I2C and then you can send/receive I2C commands to control the GPIO pins to write and read them. It's going to be slower than direct GPIO access, but maybe that doesn't matter if it takes a millisecond instead of a microsecond. You only need the two I2C pins, and you can even share the I2C port with other sensors and devices. Heck, you can even add more expanders for massive I/O control!

The AW9523 is a twist on the common I2C expander:

* First up, its very affordable - who doesn't love that?
* It has 16 I/O pins, that'll double most boards' pin count
* Four I2C address options, so you can connect 4 expanders to one bus
* Each pin can be an input or an output
* IRQ output can alert you when input pins change value
* This chip does not support internal pull-ups or pull-downs, you will need to add an external resistor if you need one
* However, it does have 8-bit linear constant-current LED dimming support so you can connect LEDs without resistors and have great looking dimming without PWM
* The first 8 pins can be configured as open drain (as a group)

The lack of internally-configurable pull's is a bit of a bummer, but we think the expander more than makes up for it with the constant-current LED drive. If you're using an expander to add lots of controllable LEDs, this board will make it very easy. Since its constant-current, you don't need resistors in line with each LED (although it won't hurt if you do): simply connect the LED anode to one of the many VIN pads, then connect the cathode to the GPIO pin.

Of course, you can control any buttons or other I/O with the pins - we just think this board is particularly suited to LED driving. There's also an interrupt output, you can enable the pin-change IRQ for any pins so you can be notified when its time to read the I/O states.

One oddity about this chip is the default I2C address determines the initial boot-state of the pins. Our libraries immediately soft-reset and configure all the pins to inputs and push-pull so you can expect the same behavior no matter what the I2C address is. However, we recommend you check the datasheet Table 1 to make sure this doesn't affect your hardware.

We've written both Arduino and CircuitPython/Python libraries for the AW9523, so you can get started whether you have an Arduino-compatible UNO or a Raspberry Pi 4 - or anything in between.

To get you going fast, we spun up a custom made PCB in the STEMMA QT form factor, making it easy to interface with. The STEMMA QT connectors on either side are compatible with the SparkFun Qwiic I2C connectors. This allows you to make solderless connections between your development board and the AW9523 or to chain it with a wide range of other sensors and accessories using a compatible cable. QT Cable is not included, but we have a variety in the shop.

### License

Adafruit invests time and resources providing this open source design, please support Adafruit and open-source hardware by purchasing products from [Adafruit](https://www.adafruit.com)!

Designed by Limor Fried/Ladyada for Adafruit Industries.

Creative Commons Attribution/Share-Alike, all text above must be included in any redistribution. 
See license.txt for additional details.
