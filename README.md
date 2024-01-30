
In this Task we utilized three different sort of circuits, for example, Battery charger Circuit, Inverter Circuit and AC voltage regulator Circuit.

How the circuit works: Circuit (I): Circuit for a Battery Charger • A step-down transformer receives approximately 12 volts of AC voltage from the secondary side of an AC supply (220 volts). • A resistor connects the secondary site of the transformer to an indicator LED. • The 12 volt DC is produced by a bridge rectifier that is connected to the 12 volt AC. The ripple voltage is removed by the capacitor. This DC is associated with a battery-powered battery and the battery will berecharged in the event that there is a stockpile (AC) to the transformer's essential side. • We use the ARDUINO Analog Read feature to display the battery voltage on the LCD display and serial monitor. Using VDR, two resistors transfer battery voltage to the Analog Pin (A1) of the Arduino. The Arduino then reads the voltage and displays it on the LCD. The following equations were used in the Arduino program: y=x(5.0/1023.0) battVolt=y/R2/(R1+R2) Circuit (ii): DC to AC Converter/Inverter Circuit • In our country we utilize 5060 Hz AC recurrence. • • The Digital Pin number "6" on the Arduino UNO is able to produce a square wave PWM with a frequency of 62500 Hz and a cycle length of 256 (0255). However, by the assistance of a divisor, we can produce (62500/1024 = ) 61.035 Hz. The following setting must be used for this purpose: TCCR0B equals TCCR0B and 0b11111000 | 0x05 http://playground.arduino.cc/Main/TimerPWMCheatsheet Here, the Arduino code Analog Write(255*50%) 127 achieves a duty cycle of 50%. This PWM signal is perused by a computerized pin of Arduino and another two computerized pins are giving two individual heartbeats, while pulse(1) is HIGH, pulse(2) is LOW as well as the other way around. • There are two NPN semiconductors, which are constrained by the Arduino beats. • The process works as follows: because transistor (1) is biased forward, current flows from collector to emitter; transistor(2) is conversely based, so no ongoing behaviors. • Semiconductors' Authorities are associated with two N-channel Power MOSFETs. What's more, the Producers are Grounded. • We know that if the Gate voltage is higher than its threshold voltage (say, VGS = 1), the n-MOSFET is turned "ON." turned 'OFF' assuming the Door voltage is lower than its limit voltage (say, VGS = 0). • • During the first half of this cycle, when transistor(1) is forward biased, there is no MOSFET(1) Gate voltage because the MOSFET(1) goes into an OFF state and the current is directly bypassed to the ground through transistor(1). During this period transistor(2) is backward one-sided and MOSFET(2) goes ON state. • Next half time of that cycle, same yet inverse activity happens. • This permits the DC voltage to be created across the essential of the transformer at substitute spans. It is 6 volts AC. • The secondary of the transformer receives a 220v AC signal after the 6v AC signal on the primary is increased. Along these lines we get changed over 220 volt AC from 6 volt DC.

iii. Circuit: AC Voltage Regulator Circuit • The inverter's result voltage (220v AC) can be constrained by an air conditioner regulator. • An Air conditioner voltage regulator contains a DIAC, a TRIAC, a Capacitor, resistors and a Potentiometer (POT). • The DIAC is a semiconductor switch with a full wave or bidirectional operation that can be turned on in either forward or reverse polarity. Similar to a DIAC, the TRIAC conducts current but needs a Gate signal to do so.
