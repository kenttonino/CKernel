# Reference

> - https://github.com/bluez/bluez/blob/master/doc/assigned-numbers.rst

<br />
<br />
<br />



# Radio Frequency Communication (RFCOMM)

> - A bluetooth protol that emulates serial ports over Bluetooth.
> - It pretends a Bluetooth connection in a serial cable.
> - If you have two devices, like a laptop and a headset, RFCOMM lets them talk as if they where connected physical serial port, even though its wireless.
> - RFCOMM exists to trick old software and devices into thinking there's a cable, so everything works over wireless without rewriting decades of code.

<br />
<br />
<br />



# Channel

> - In RFCOMM, it's like a port number for your virtual serial cable.
> - A Bluetooth device can offer multiple services over RFCOMM.
> - Each service gets its own channel number (1-31).
> - When you connect, you pick a channel to say, “I want to talk to this service, not that one.”.
> - Each of those channels is basically a slot that a specific Bluetooth service lives in, so devices know where to talk to each other.

<br />

`RFCOMM Channels`
> __Channel 1__: __Dial-up Networking__ (DUN)
> - Old-school “connect to the internet over your phone modem.”.
> - It’s literally serial data over Bluetooth to act like a modem cable.

> __Channel 3__: __Serial Port Profile__ (SPP)
> - Generic serial communication over Bluetooth.
> - Anything that wants a simple "wireless COM port" uses this.
> - Think sensors, arduino boards, industrial machines.

> __Channel 6__: __Headset Profile (Headset Role)__ (HSP HS)
> - For simple mono headsets.
> - HS is the Headset (the earpiece).
> - Handles audio control (volume, answer/hangup) and basic audio streaming.

> __Channel 7__: __Hands-Free Profile (Hands-Free Role)__ (HFP HF)
> - Designed for car kits and hands-free devices.
> - HF meands Hands-Free device.
> - Provides richer call control than HSP: call lists, voice dialing, battery indicators.

> __Channel 9__: __Object Push Profile__ (OPP)
> - Send simple objects like business cards (vCards) or files.
> - Very basic file transfer, often used by phones.
