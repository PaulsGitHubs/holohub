# Basic Networking Ping

This application takes the existing ping example that runs over Holoscan ports and instead uses the basic
network operator to run over a UDP socket.

The basic network operator allows users to send and receive UDP messages over a standard Linux socket.
Separate transmit and receive operators are provided so they can run independently and better suit
the needs of the application.

### Configuration

The application is configured using the file basic_networking_ping.yaml. Depending on how the machine
is configured, the IP and UDP port likely need to be configured. All other settings do not need to be
changed.

Please refer to the basic network operator documentation for more configuration information

### Requirements

This application requires:
1. Linux

### Build Instructions

Please refer to the top level Holohub README.md file for information on how to build this application.

### Run Instructions

First, go in your `build` or `install` directory. Then, run the commands of your choice:


```bash
./build/applications/basic_networking_ping/cpp/basic_networking_ping
```
