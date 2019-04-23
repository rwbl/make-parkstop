# make_project_parkstop

# Objectives
* To build a parkSTOP device to visually indicate via LED if parking position is reached.
* In addition, indicate via Android App, comunicating via Bluetooth, the actual distance and if parking position reached.
* Usage f.e. to park in the garage for cars without parking distance sensors or park at an exact position.

![parkstop-f](https://user-images.githubusercontent.com/47274144/52939989-bdc49000-3365-11e9-8c03-9f629d3784af.png)

## Functionality
* ParkSTOP Device: Indicate position LED RED = reached Stop distance, YELLOW = reached Warning distance (=1.5 times stop distance), GREEN = reached between notify distance and warning distance.
* ParkSTOP Device: Alarm (via Buzzer) when reaching warning or stop distance.
* ParkSTOP Device: Store settings (in EEPROM).
* Android App: Show distance, indicator meter with bar to see position, indicate to stop, set stop-/ notify distance and if buzzer on.
* Communication via Bluetooth between the devices e.g. ParkSTOP device and Android App.
* Open to connect other Bluetooth devices (but only one at the time).

## Creation Rules
* Use as microcontroller an Arduino UNO.
* Use standard LEGO bricks.
* Minimize LEGO brick modifications.
* LEGO Case with modular components.
* Build code with B4R and B4A.

## Hardware Parts (approx cost EUR)
* 1x Arduino UNO (8 EUR)
* 1x HC-05 Bluetooth Adapter (7 EUR)
* 1x HC-SR04 Ultrasonic Distance Sensor (2 EUR)
* 1x Buzzer (1.75 EUR)
* 3x LED (0.75 EUR)
* In addition for the prototype: Breadboard (2 EUR)
* LEGO bricks [LEGO is a trademark of the LEGO Group] (10 EUR)

## Software
* Arduino IDE 1.8.0
* B4R v1.80
* B4A v6.50
(Min software versions required)

## Wiring
![parkstop_bb](https://user-images.githubusercontent.com/47274144/52939987-bdc49000-3365-11e9-8f78-1e7b41147569.png)

```
#Arduino = Buttons (WireColors)
#Bluetooth
HC-05 = Arduino
VCC = 5v (red)
GND = GND (black)
TX = 10 Receive Pin (green)
RX = 11 Transmit Pin (yellow)

#Distance
[CODE]HC-SR04 = Arduino
VCC = 5v (red)
Trigger = D8 (blue)
Echo = D7 (white)
GND = GND (black)

#Indicators
LED RED = STOP
LED = Arduino
Anode (+) = D4
Cathode (-) = GND
LED YELLOW = WARNING
LED = Arduino
Anode (+) = D5
Cathode (-) = GND
LED GREEN = OK
LED = Arduino
Anode (+) = D6
Cathode (-) = GND

#Buzzer
Signal = D12 (red)
GND = GND (black)
```
## Soure Code
The [B4R](https://www.b4x.com/b4r.html) source code and required libraries can be found in archive __parkstop.zip__. The code is well documented.
