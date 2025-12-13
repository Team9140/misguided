# Misguided

The following are the requirements for the Misguided Pi hat (refered to henceforth as "the board"). Hard requirements that must be met will the the word SHALL. Softer requirements that denote best practices or stretch goals will use the word SHOULD.

These requirments are accureate as of December 12, 2025 AD.

The mentor responsible is: Carson Graf, cgraf498 (at) gmail (dot) com

## Design

The board SHALL be designed in KiCAD

## Mechanical

The board SHALL follow the mechanical layout specified in Secion 7 of the HAT+ Specification

## Power

The board SHALL accept input power at a nominal 12 volts

The board SHALL be operational with input power as high as 24 volts and as low as 6.5 volts

The board SHALL use a lever termial block style connector to accept the 12 volt power

The board SHALL generate a 5 volt DC rail capable of supplying at least 5 amps for the Raspberry pi

## CAN FD Subsystem

The board SHALL provide a MCP2518FD or MCP2517FD CAN controller

The board SHALL connect the aforementioned CAN controller to the PI in a way that is amenable to the existing linux kernel driver for that chip

The board SHALL use a 3 pin Molex SL compatible connector to connect to an external CAN FD bus

## GPIO Syncronization Subsystem

The board SHALL provide an 5 volt capable digital input

The board SHALL use a 3 pin Molex SL compatible connector to connect to an external 5 volt digital output

The board SHALL connect the digital input to the Raspberry pi in a way that is amenable to to the existing linux gpio kernel driver

The board SHALL connect the digital input to the Raspberry pi in a was that is consistant with the continued operation of the raspberry pi

The board SHOULD isolate the input using an optocoupler

The board SHOULD provide similar capabilities for a 5 volt digital output

## Neural Accelerator Subsystem

The board SHOULD provide facilities for operating a Hailo-8L M.2 Entry-Level Acceleration Module

The board SHOULD provide a connector to interface with the Raspberry Pi's PCIE port

## Componet Choices

All connectors SHOULD be through hole components

Components in leaded packages (e.g. SOIC) SHOULD be prefered to components in leadless packages (e.g. QFN)

Components in the the JLC basic library SHOULD be prefered to components in JLCPCBs Extended library, which SHOULD be preferred to components that will need to be procured elsewhere

## Referenced Documents

HAT+ Specification: https://datasheets.raspberrypi.com/hat/hat-plus-specification.pdf