# ATtiny13A Makefile project

This is a simple example Makefile cross compiling project for the AVR ATtiny13A
microcontroller.

## Dependencies

If you are using Archlinux, you will need to install the following
dependencies:

 - `avr-gcc`, GCC for the AVR architecture.
 - `avr-libc`, the C header files for AVR C programming.
 - `avrdude`, the flashing toolkit for AVR ICSP.

Package naming should be similar if using other GNU/Linux distros.

## Makefile rules

This Makefile is very simple and have two important rules.

### all

Compile the program in the `main.cpp` file to a `main.hex` flashable HEX file.

This rule is made for a single source code file and adjustments will be
required in order to adapt it to a multiple file project (however remember
there is only 1K flash on the chip so…).

### flash

This rule will flash the `main.hex` file to the microcontroller using the
`/dev/ttyUSB0` serial port interface, which is an Arduino with ICSP firmware
in my case but this may work with any serial USB flash tool I guess.

## Documentation

The documentation of the chip can be found [directly as a PDF file on ATMEL’s
website](http://www.atmel.com/Images/doc8126.pdf).

## Copyright

This little project is brought to you under WTFPL license, so feel free to use.
