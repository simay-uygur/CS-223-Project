# CS-223-Project
This is a project assignment given by Bilkent University in the CS 223 course.


A simplified UART device has registers to store both the incoming and outgoing data. The communication happens at a pre-determined frequency called the baud rate. Baud rate expresses how many bits per second are sent over when the communication is initiated. Both sides must also agree on the amount of parity bits, stop bits, and the length of the data frame for UART to work properly.

At the end of stage 1, your board design can transmit and receive 1-byte of data. Important points to note:
 You can load according to the rightmost 8 switches by pressing BTND button.
 You display the 8-bit wide register on the rightmost 8 LEDs.
 You signal the start of the tranmission by the press of BTNC button.
 Your receiver automatically detects the incoming transmission and stores it in the register.
 You display the 8-bit wide register on the leftmost 8 LEDs.


These are the specifications for the UART design:
*8 data bits per transmission (each transmission is a byte).
* 1 parity bit.Even parity is used.
* 1 stop bit.


Also the uart design has first in first out (FIFO) structure. Two 4-byte memory for storing transmitted and received data is allocated. The receiver register files are designed to operate as a FIFO structure, discarding the earliest received data when the 5th byte arrives and there is no additional space. 

The datas can be seen from the seven segment display on the basys 3 board.

Also as an additional feature, pressing a specified button triggers the automatic transfer. In this process, the whole data in the transmitter will be transferred in one wire (line) and receiver takes that to its FIFO memory.
