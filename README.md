# DIY 9-Bay NAS Backplane

> A simple and compact 9-Bay Backplance for a compact NAS application.

## Overview

This backplane is designed for connectivity for up to 8 SATA 3.0 storage drives connected to a PCIE HBA, as well as one slot for a SATA 3.0 boot drive connected to a motherboard SATA header. This board was specifically designed to be used in a Fractal Terra with an HDPLEX 250w GaN PSU, but should work for any small form factor NAS.

## Specifications

Dimensions: 115mmx58mm
Power Connector: 4-pin peripheral
Supply Voltage: 5v
Hot Swap: Hardware Supported (HBA must also support)

## Project Status

We've reached version 1.2 of this project. It took longer than I hoped, but I've built and tested this version and am currently running it in my NAS.

## Changes

Changes since version 1.0 include the following

- updated power connector to 4-pin peripheral (goodbye screw terminal)
- updated bulk capacitors to an appropriate size
- removed the 12v rail (only 5v is needed for SSDs)
- added full ground plane
- fixed SATA Data differential pair balancing
- added large isolation zone

## Making

Actually making one of these backplanes is very tedious. I can only recommend this if you have fine soldering skills.

If you do decide to make this, this is how I assembeled it.

- solder the SMD capacitors and resistors first. It is recommended that you use a solder reflow station. 
- for SATA interfaces, start on the end of the board that is furthest away from the power through holes
- use two 22-pin SATA connectors (one on J901 and one on J101, for balance), solder J901
- flip the board over and use three 7-pin SATA connectors (one on J902, J102, and the edge of the board where its falling over), solder J902
- flip the board over and repeat for all slots in descending order.
- once all the slots are soldered, solder the bulk capacitors, and 4-pin power. order doesnt matter here
