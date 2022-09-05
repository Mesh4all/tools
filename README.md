# Applications and Tools
Useful tools for testing networks and related applications to Mesh4all daily work.

## What's this?
This is a collection of some applications utils to analyze, recopile and send data via
a wireless or wired connection. applications). 

## What's inside?

There are some applications that implement connection over Internet IPv6.
using devices with support wireless standards, IEEE802.15.4, Zigbee and wifi.
These applications are provided by [RIOT-OS applications](https://github.com/RIOT-OS/applications)

### 802.15.4 Wireless sniffer

This is a simple way to monitorize an IPV6 network, creating a listening node that will receive and check
all the sent packets in the wireless network.

the only it need is:
- enter to applications/sniffer directory:
```sh
cd applications/sniffer
```
- build & flash
```
make flash BOARD=<Enter_model_of_your_board>
``` 
for example:
```
make flash BOARD=samr21-xpro
```
- Open sniffer with Wireshark.
```
python3 ./tools/sniffer.py -b 115200 /dev/ttyUSB1 26 | wireshark -k -i -
```
[for more information about sniffer...](https://github.com/RIOT-OS/applications/tree/master/sniffer)

## CoAP chat

provides a chat over (g)CoAP as transport. It allows to send (short) messages to any (IPv6) address reachable between nodes.

using gcoap module and the command `chat`.

```
chat <Ipv6_dest> <Nickname> <Message>
```

The maximun buffer size is 63 bytes to send and receive messages. see more about coap-chat in [RIOT-OS/applications](https://github.com/RIOT-OS/applications/tree/master/coap-chat).

## License

  Copyright (C)  2022  Mesh4all <contact@mesh4all.org>

  This library is free software; you can redistribute it and/or
  modify it under the terms of the GNU Lesser General Public
  License as published by the Free Software Foundation; either
  version 2.1 of the License, or (at your option) any later version.

  This library is distributed in the hope that it will be useful,
  but WITHOUT ANY WARRANTY; without even the implied warranty of
  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
  Lesser General Public License for more details.