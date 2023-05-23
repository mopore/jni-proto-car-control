JNI Proto Car Control
=====================
This is the controller project to remotely control the JNI Proto Car with an PS3 Controller.
This project rewrites the original CircuitPython code to C++ and uses the Arduino framework.

![controller](https://github.com/mopore/jni-proto-car-control/assets/56848419/0ae97fe3-98a0-4512-861e-4789006d5a53)

The project for the JNI Proto Car Base can be found [here](https://github.com/mopore/jni-proto-car-base).


# Pre-requisites
* Fully setup platformIO environment
* An ESP32 Microcontroller
* A PS3 Controller (or compatible replica)
* A Wifi network

Note that it might be hard to purchase a new original PS3 controller. Unfortunately not all replicas are compatible and will work.
The following controller worked for me:
[Link to used controller from Digitec (CH)](https://www.digitec.ch/de/s1/product/tracer-tracer-trooper-ps3-gaming-controller-15680780?supplier=406802)
I further used the [Sixaxis Pair Tool](https://www.filehorse.com/download-sixaxispairtool/) to initiate and set the targeted MAC address on the PS3 controller (not its own but the "PS3/bases' one").
Further information can be found here: https://www.youtube.com/watch?v=nctYJaDNLU0




# Setup
## Create a include/jni_config.h file
For Wifi and further network setup. Create a file called `include/jni_config.h` with the following content:

```c
#define WIFI_SSID      "your-wifi-ssid"
#define WIFI_PASS      "your-wifi-password"

#define UDP_RECEIVER_SOCKET_IP "192.168.100.102"  // Backup JNI Proto Car
#define UDP_RECEIVER_SOCKET_PORT 8080

#define ESP32_HOST_MAC "e8:9f:6d:25:49:26"  // MAC address of the ESP32 linked with PS3 Controller
```
