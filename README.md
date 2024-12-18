## KiCad library for `GerberSockets` & virtual modules (VMs)

This repository contains KiCad libraries with both symbols and footprints for the various types of devices/annotations that can be done using `GerberSockets`.

`GerberSockets` are the endpoints, at which an application can extract information about the design, and perform actions with that data. For example, the MakeDevice project will find the location of the Jacdac nets (`JD_PWR`, `JD_DATA`, and `GND`) and route the electrical traces between all modules on a circuit baord. 

A guide will follow soon to describe how to use this library, and how to create your own annotations using `GerberSockets`