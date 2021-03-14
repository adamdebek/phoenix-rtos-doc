# Network stack

Phoenix-RTOS network stack is based on LwIP. According to microkernel architecture philosophy it works as a server on the user level and provides socket interface. Sockets are implemented using native Phoenix-RTOS message passing mechanism. Socket are implemented in libphoenix library.

## Drivers
1. [PPPoU – uart/serial null-modem connection driver](lwip-pppou.md)

## Source code

The source code of the emulation server could be obtained using the following command

>
    git clone http://git.phoenix-rtos.com/phoenix-rtos-lwip
