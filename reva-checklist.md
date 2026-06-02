# Review Checklist

A list of things that need to be checked for the design to sufficiently verified
for order.

## Basics

- [x] Schematic ERC passes
- [x] PCB DRC passes
- [x] PCB stack-up matches what is available on JLC/PCBWay
- [x] PCB design rules match the capabilities of JLC/PCBWay

## Components

- [x] Each component has a BOM MPN that is in stock on Mouser/Digikey
- [x] Pin assignment to component footprint is correct (check _all_
      non-passives)
  - [x] Clock
  - [x] GPIO NMOS
  - [x] Pyro NMOS
  - [x] PMOS
  - [x] MCU
  - [x] Barometer
  - [x] USB
  - [x] Regulator
  - [x] Power MUX
- [x] Connections to FETs are correct
- [x] Battery leads have right polarity

NOTE: made battery leads follow the shitty standard set out by other rocket
electronics where pin 1 is V+ and pin 2 is GND.

## Component Ratings

- [x] Component values are correct for their use (correct resistance,
      capacitance, etc.)
- [x] Components passing high power have sufficient wattage
- [x] LED circuits are properly connected for forward voltage + resistance
- [x] FETs have correct activation voltage
- [x] FETs can pass sufficient current
- [x] Max current draw can be supplied by the regulator
- [x] RF matching circuitry has correct values

## Correctness

- [x] All LEDs have resistors
- [x] All switching NMOS FETs have gate pull-downs
- [x] Voltage dividers are correct for all possible input/output ranges
- [x] Load capacitance for clock is correct
- [x] Boot/enable circuitry is correct for MCU
- [x] Pin assignments for MCU are correct
- [x] Pin assignments for barometer are correct

## Routing

- [x] High current traces can supply sufficient current
- [x] Via stitching around clock
- [x] Via stitching around RF trace
- [x] USB routed as 90ohm differential pair
- [x] RF routed as 50ohm impedance matched
- [ ] RF trace below critical length (not really but best I can do)
- [ ] RF routing matches application note suggestion (antenna/ESP32) (not really
      but best I can do)
- [x] All fill zones poured
- [x] Minimal 0402 sized components on back, only if hand-solderable

## Silkscreen

- [x] Logo is visible on top side
- [x] Revision is visible on top side
- [x] Pyro channels are clearly labelled
- [x] All LEDs are clearly labelled
- [x] Arming terminal is clearly labelled
- [x] Boot jumpers are clearly labelled
- [x] Components on back-side are sufficiently short for mounting
- [x] Mounting holes have a hole pattern with distances in whole millimeters
