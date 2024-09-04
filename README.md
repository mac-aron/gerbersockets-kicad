## KiCad library for MakeDevice virtual modules

This KiCad library contains both symbols and footprints for the virtual Jacdac
modules `Gerber sockets`.

`Gerber sockets` are the endpoints, at which the MakeDevice application will
route the electrical traces. As of now, there are only `Jacdac bus` sockets,
but in the future work we will follow with `Jacdac prog` sockets, as well.

A guide will follow soon to describe how to use this library, and how to
create your own MakeDevice virtual modules.

## KiCad symbol previews

#### Jacdac power Gerber socket

![Gerber socket symbol for Jacdac power bus](/svg/JD_PWR_symbol.svg)

#### Jacdac ground Gerber socket

![Gerber socket symbol for Jacdac ground](/svg/GND_symbol.svg)

#### Jacdac data Gerber socket

![Gerber socket symbol for Jacdac ground](/svg/JD_DATA_symbol.svg)
