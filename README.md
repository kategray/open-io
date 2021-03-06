Open-IO
=======


A drop-in replacement for the EXT-IO. If you're not sure what the EXT-IO is, you probably don't need a replacement.

> **Required Parts:**

> - Arduino Mega 2560
> - Max232 - To convert rs232 12v from BemaniPC/Python 2 to 5v for Arduino
> - Hookup pins/wires
> - 5v power source for Arduino

---

Connector & Cable Identification
------------

To install the Open-IO, we first need to identify a few connectors inside of your DDR cabinet - Pad connectors, Neon Light connector, and Serial Communication connector.

**Pad Connectors**

There are 2 pad connectors (P1 - White; P2 - Orange) that each have 7 cables.

Pin Name    | JP Cab Color | Kor Cab Color
----------- | ------------ | -------------
Ground      | Black        | Black
FL1         | Green        | Blue
FL2         | Blue         | Green
FL3         | Purple       | Yellow
FL4         | Grey         | Orange
FL5         | White        | Red
TEST        | Brown        | Brown

**Neon Connector**

There is a Neon light connector (White) that has 2 cables (Red & Black).

**Serial Communication Connector**

Lastly we need to identify the serial communication cable from COM1 on your BemaniPC or Python2. This connector has 3 cables.

Pin Name | Color
-------- | -----
GND      | Black
RX       | Grey
TX       | Purple

Installation
---

Connect your Arduino using this pin-out:

Arduino Pin | Destination
----------- | -----------
2			| P2 TEST
3			| P2 FL5
4			| P2 FL4
5			| P2 FL3
6			| P2 FL2
7			| P2 FL1
8			| P1 TEST
9			| P1 FL5
10			| P1 FL4
11			| P1 FL3
12			| P1 FL2
13			| P1 FL1
16			| RX on TTL side of Max232
17			| TX on TTL side of Max232
22          | Neon Red
5v          | Max232 5v
GND         | P1 GND
GND         | P2 GND
GND         | Neon GND
GND         | Max232 GND

And connect your Max232 with this pin-out:
> **Note**
> 
> All of these Max232 pins are on the RS232 side
> 
> If your Max232 has a db9 port, refer to the db9 pin column.

Max232 Pin | db9 Pin | Serial Data Connector Pin
---------- | ------- | -------------------------
RX         | 2       | RX
TX         | 3       | TX
GND        | 5       | GND

You'll also need a 5v power source inside of the cabinet for your Arduino.
