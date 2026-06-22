
For your **RF-Based Wireless Control System**, you can put this under **Circuit Explanation** in GitHub README:

## Circuit Explanation

The system consists of a **433 MHz RF Transmitter** and **433 MHz RF Receiver** pair used for wireless control of electrical loads.

### Transmitter Section

* Push buttons are connected to the **HT12E Encoder IC**.
* When a button is pressed, HT12E converts the command into encoded digital data.
* The encoded data is transmitted wirelessly through the **433 MHz RF Transmitter** module.
* A battery supply powers the transmitter circuit.

### Receiver Section

* The **433 MHz RF Receiver** receives the transmitted signal.
* The received data is decoded by the **HT12D Decoder IC**.
* The decoder output drives a **relay driver circuit** (transistor + relay).
* The relay switches ON/OFF the connected AC or DC load according to the received command.

### Relay Driver Circuit

* Since the decoder IC cannot directly drive the relay, a transistor is used as a switch.
* When the decoder output becomes HIGH, the transistor energizes the relay coil.
* The relay contacts then connect or disconnect the AC bulb or DC LED load.
* A flyback diode is connected across the relay coil to protect the transistor from back EMF.

Push Button
     ↓
HT12E Encoder
     ↓
433 MHz RF Transmitter
     ↓ ~~~ Wireless Link ~~~
433 MHz RF Receiver
     ↓
HT12D Decoder
     ↓
Relay Driver
     ↓
AC/DC Load

