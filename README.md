# CS-223-Project
This is a project assignment given by Bilkent University in the CS 223 course.


A simplified UART device has registers to store both the incoming and outgoing data. The communication happens at a pre-determined frequency called the baud rate. Baud rate expresses how many bits per second are sent over when the communication is initiated. Both sides must also agree on the amount of parity bits, stop bits, and the length of the data frame for UART to work properly.


These are the specifications for the UART design:
* 8 data bits per transmission (each transmission is a byte).
* 1 parity bit.Even parity is used.
* 1 stop bit.


The uart design has first in first out (FIFO) structure. Two 4-byte memory for storing transmitted and received data is allocated. The receiver register files are designed to operate as a FIFO structure, discarding the earliest received data when the 5th byte arrives and there is no additional space. 

The datas int the receiver and transmitter memory can be seen from the seven segment display on the basys 3 board.

Also as an additional feature, pressing a specified button triggers the automatic transfer. In this process, the whole data in the transmitter will be transferred in one wire (line) and receiver takes that to its FIFO memory.
