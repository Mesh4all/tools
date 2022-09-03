# Applications and Tools
Useful tools for testing networks and related applications to Mesh4all daily work.

## What's this?
This is a collection of some applications utils to analyze, recopile and send data via
a wireless or wired connection. applications). 

## What's inside?

There are some applications that implement connection over Internet IPv6.
using devices with support wireless standards, IEEE802.15.4, Zigbee and wifi.
These applications are provided by [RIOT-OS applications](https://github.com/RIOT-OS/

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
## License


 Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License

 You may obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0

  or in the [LICENSE](LICENSE) file, in the root folder of this repository.

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.

See the License for the specific language governing permissions and limitations under the License.

Copyright (c) 2022 Mesh4all <mesh4all.org>

Licensed under the Apache License Version 2.0 Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
