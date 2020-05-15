## Troubleshooting Automated Greenhouse
Here, we involve debugging of my automated greenhouse model. Find [here](https://github.com/prateekagrawalgithub/Electronics-Club-Mini-Task-2/blob/master/Automated%20Greenhouse.md) the full description of the model first.

**Sequence:** Sensors => Microcontroller (Arduino+Raspberry Pi3) => Actuators

**Basic Debugging:** So, if the model with the circuit is built and it fails somewhere, check these little error possibilities first:
1. Understand the full schematics and check the circuitry with basic connections like the power supply. Neat circuit should help understand the situation better.
2. An overview will help find if every device glows and gets power, checking voltage at different points and if any device is getting heated up.
3. While such minor problems can directly say it's short circuited and we need to buy a new one. Check resources below for it.
4. Else, if all devices glow and everything looks fine, check out debugging for individual devices. Make sure you perform debugging in sequential manner so that it can be easy to find out the error.

**Testing sensors:**
* Sensors may malfunction - maybe it only works occasionally, maybe there’s too much noise to establish a strong connection, or maybe we just don’t know what is wrong with it.
* We separate out the sensors which is showing up likely errors and test it with a multimeter.
* *Continuity Test* - Disconnect sensor from power source. Plug the black probe into the COM (common) port on your multimeter. Plug the red probe into the VΩ port. Set multimeter to continuity (symbol looks like •))). Connect the red probe to the + wire going to the sensor, and connect the black probe to the ground wire going to the sensor. Connect the red probe to the + wire going to the sensor, and connect the black probe to the ground wire going to the sensor.
  1. If the multimeter registers a reading, your circuit wiring is intact. Move onto the next sensor's test or directly to the microcontroller testing.
  2. If the multimeter does not register a reading, then there is something wrong with the wiring. Repeat the above steps along the various sections of the circuit between the source and sensor to isolate the problem.
* *Voltage Test* - After continuity test, check the source voltage, but not at the source. Reconnect the sensor’s power source and disconnect the power wires at the sensor or connection point closest to the sensor. With the same probe – multimeter connections, connect the red probe to the incoming + wire, pin, or terminal, and the black probe to the ground wire/pin/terminal. Using multimeter, verify that the voltage at the sensor is within the range suggested in the user manual.
  1. If so, we’ve eliminated source voltage as the problem. Move on to the next test below!
  2. If not, the voltage source is at least a problem, if not the problem. Check out power connections properly and try again!
* *Resistance Test* - we’ll check circuit impedance or resistance. Reconnect the power wires at the sensor and disconnect the communication wires for the sensor at the source. With the same probe – multimeter connections, connect the red probe to the + wire going to the sensor and connect the black probe to the ground wire going to the sensor as done before.
  1. Many sensors that use communication protocols require a minimum of 150Ω to 180Ω, so choose the Ohm value on the multimeter that is closest to, yet bigger than, 200Ω. If the circuit impedance is less than that recommended by your user manual, then add an appropriate amount of resistance to the circuit.
  2. If the multimeter doesn’t register the impedance, select the next highest denomination of Ohms. If the circuit’s impedance is too high (and not infinite), something will need to be removed from the circuit (switch to a smaller wire size, too many intermediate junctions, etc).
* If these steps have not helped you identify and isolate the problem, there may well be a problem with your sensor. Buy a new high-quality sensor, check the resource section below. (More detailed description of tests with diagrams can be found [here](https://www.apgsensors.com/about-us/blog/how-to-use-a-multimeter-to-troubleshoot-your-sensor))

**Testing Microcontroller:**
* As per process, catch up with the microcontroller's datasheets ([Arduino](https://datasheet.octopart.com/A000066-Arduino-datasheet-38879526.pdf) and [Raspberry Pi 3](https://components101.com/microcontrollers/raspberry-pi-3-pinout-features-datasheet)) and see if you are bumping into any limitation given there. Check out the specifications and get back!
* While these microcontrollers have inbuilt mechanisms to prevent them from breaking/shorting, we can still check if they are hot or unable to upload the code then probably it has burnt. Check this too.
* So, if it has burnt and become disfunctional, pls check out the resource section below and buy a new one!

**Testing Actuators:**
* Again, get to the datasheet first and check the specifications and working of each actuators along with the required pin connections. This will give a quick overview to what can go wrong.
* Next, individually check the troubling actuator and testing its individual pins and actuation points.
* The common errors arise due to loose connections, improper metal-wire connections, obstructions and especially high power/torque.
* This actuator part has a high chance of error because they easily burn down especially due to power issues, so handle it properly even while debugging it separately.

### Resources:
1. Humidity & temperature sensor -> [DHT-11](https://robu.in/product/dht-11-digital-temperature-humidity-sensor/?gclid=EAIaIQobChMIkYeh1N226QIV2nwrCh0uMQHMEAQYASABEgI3AvD_BwE)
2. soil moisture sensor -> [YL-38 & YL-69](https://robu.in/product/soil-moisture-meter-soil-humidity-sensor-water-sensor-soil-hygrometer-ardunio/?gclid=EAIaIQobChMInPjIit626QIVxX0rCh21owgREAYYASABEgKl3PD_BwE)
3. Arduino -> [from Amazon](https://www.amazon.in/Uno-ATmega328P-Compatible-ATMEGA16U2-Arduino/dp/B015C7SC5U/ref=sr_1_2?crid=3NM0XG50EOCYF&keywords=arduino+uno+r3+board&qid=1568454839&s=gateway&sprefix=Arduino%2Caps%2C739&sr=8-2) OR [from robu.in](https://robu.in/product/arduino-uno-r3-ch340g-atmega328p-devlopment-board/?gclid=EAIaIQobChMI5J3S8Mi26QIVyxErCh2nhAUzEAQYASABEgJDK_D_BwE)
4. Raspberry Pi3 -> [from robu.in](https://robu.in/product/raspberry-pi-3-model-b-bcm2837b0-soc-iot-poe-enabled/?gclid=EAIaIQobChMI2JzG2t626QIViCQrCh3QYgjZEAQYASABEgI8WvD_BwE)
5. DC Water Pump -> [from Amazon](https://www.amazon.in/BESTVECH-Ultra-quiet-Brushless-Submersible-Fountain/dp/B079L6GFVG?ref_=fsclp_pl_dp_7)
