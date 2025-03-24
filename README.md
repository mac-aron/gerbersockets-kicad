## KiCad symbol and footprint library for `GerberSockets`

This repository contains KiCad symbol and footprint library for `GerberSockets`.

`GerberSockets` are the endpoints, at which an application can extract information about the design, and perform actions with that data. For example, the MakeDevice application will find the location of the Jacdac nets (`JD_PWR`, `JD_DATA`, and `GND`) and route the electrical traces between all modules on a circuit board.

I recently added additional nets for chip flashing, and USB support.

## GerberSockets in this library

Symbols and footprint were created for the following nets.

- [x] `JD_PWR`: diameter of 0.11 mm
- [x] `GND`: diameter of 0.12 mm
- [x] `JD_DATA`: diameter of 0.13 mm
- [x] `SWCLK`: diameter of 0.14 mm
- [x] `SWDIO~`: diameter of 0.15 mm - see below
- [x] `SWDIO~^`: diameter of 0.16 mm - see below
- [x] `RESET`: diameter of 0.17 mm
- [x] `USB_D_P`: diameter of 0.18 mm
- [x] `USB_D_N`: diameter of 0.19 mm

`~` and `~^` are special characters used as placeholders in the routing process. These placeholders will be replaced with numbers (like 1, 2, 3, etc.) during the routing calculations. The purpose of these placeholders is to create pairs of connecting points.

Specifically, for the SWDIO (Serial Wire Debug Input/Output) line, the trace (the physical path of the connection) must run directly from the flasher (a device used to program the target chip) to the target chip itself.

By using `~` and `~^`, you can define these pairs of points that need to be connected in the routing process.

For example, the autorouter will recognize pairs of `SWDIO~` and `SWDIO~^` and convert them to `SWDIO1` and `SWDIO1` respectively, forming a connection point.