## Troubleshooting Voice Chess
Here, we involve debugging of my voice chess model. Find [here](https://github.com/prateekagrawalgithub/Electronics-Club-Mini-Task-2/blob/master/Voice%20Chess.md) the full description of the model first.

**Sequence:** Voice to Text Convertor => Arduino => Motor Driver

**Basic debugging:** So, if the circuit is built and it doesnt work, check these little error possibilities first:
1. Check if power supply is on, whether you are able to understand the schematic and have built the circuit correctly. More 'arranged' circuit should help.
2. If any of the above devices doesn't light up or find it very hot, then it's probably a short-circuit. Buy a new one, check the resource section.
3. Else, if all devices glow and everything looks fine, check out debugging for individual devices!
4. Make sure you perform debugging in sequential manner so that it can be easy to find out the error.

**Testing Convertor:**
* Simply check on the output and the time taken to generate it. If we are getting accurate output text in considerable time, then you are good to go to test next device.
* Else, there maybe some ambiguity with the database. To get best speech synthesis rate, database of system should be modified so that our speech recognition engines suits our requirements. Check on it!
* Greater details about the problem can be found [here](http://www.ijceronline.com/papers/Vol2_issue2/AX022512515.pdf)
* If the problem still persists, we can easily change to the older model of using google voice app in android, perhaps the easiest way.

**Testing Arduino:**
* A likely case of arduino not working is if you bump into any limitation given in [Arduino datasheet](https://datasheet.octopart.com/A000066-Arduino-datasheet-38879526.pdf). So check out the specifications and join back!
* While arduino has inbuilt mechanisms to prevent it from breaking/shorting, we can still check if it is hot or unable to upload the code then probably it has burned.
* If it has burnt, check the resource section; else move on to the motor driver testing!

**Testing Motor Driver:**
* As per the process, we should first learn about working of driver used - L298N. Go through [this](http://www.handsontec.com/dataspecs/L298N%20Motor%20Driver.pdf) and then check out your connections.
* Additionally, you can check the driver individually by taking it out of circuit and testing individual pins with a motor connected to it.
* Loose connection or improper metal-wire contact can be a common error too. Check that out also.
* Motors and motor drivers are easily destroyed and problems are seen usually with them only, so use it properly even while debugging (especially with power connections)

### Resources:
1. Arduino UNO -> [from Amazon](https://www.amazon.in/Uno-ATmega328P-Compatible-ATMEGA16U2-Arduino/dp/B015C7SC5U/ref=sr_1_2?crid=3NM0XG50EOCYF&keywords=arduino+uno+r3+board&qid=1568454839&s=gateway&sprefix=Arduino%2Caps%2C739&sr=8-2) OR [from robu.in](https://robu.in/product/arduino-uno-r3-ch340g-atmega328p-devlopment-board/?gclid=EAIaIQobChMI5J3S8Mi26QIVyxErCh2nhAUzEAQYASABEgJDK_D_BwE)
2. Motor Driver L298N -> [from robu.in](https://robu.in/product/l298n-2a-based-motor-driver-module-good-quality/?gclid=EAIaIQobChMImurg-Mm26QIVGyUrCh121QMNEAQYASABEgLYIPD_BwE)
3. Example of a useful conversion app -> [Arduino Voice Control](https://play.google.com/store/apps/details?id=appinventor.ai_cempehlivan92.Arduino_Sesli_Kontrol&hl=en)
