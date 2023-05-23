JNI Proto Car Control
=====================
This is the controller project for to remotely control the JNI Proto Car with an PS3 Controller.
The project for the JNI Proto Car can be found [here](https://github.com/mopore/jni-proto-car-base).


# Pre-requisites
* Fully setup platformIO environment
* An ESP32 Microcontroller
* A PS3 Controller (or compatible replica)
* A Wifi network


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