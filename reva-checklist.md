# Review Checklist

A list of things that need to be checked for the design to sufficiently verified
for order.

## Basics

- [ ] Schematic ERC passes
- [ ] PCB DRC passes
- [ ] PCB stack-up matches what is available on JLC/PCBWay
- [ ] PCB design rules match the capabilities of JLC/PCBWay

## Components

- [ ] Each component has a BOM MPN that is in stock on Mouser/Digikey
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

## Component Ratings

- [ ] Component values are correct for their use (correct resistance,
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

- [ ] High current traces can supply sufficient current
- [ ] Via stitching around clock
- [ ] Via stitching around RF trace
- [ ] USB routed as 90ohm differential pair
- [ ] RF routed as 50ohm impedance matched
- [ ] RF trace below critical length
- [ ] RF routing matches application note suggestion (antenna/ESP32)
- [ ] All fill zones poured
- [x] Minimal 0402 sized components on back, only if hand-solderable

## Silkscreen

- [ ] Logo is visible on top side
- [ ] Revision is visible on top side
- [x] Pyro channels are clearly labelled
- [x] All LEDs are clearly labelled
- [x] Arming terminal is clearly labelled
- [x] Boot jumpers are clearly labelled
- [x] Components on back-side are sufficiently short for mounting
- [x] Mounting holes have a hole pattern with distances in whole millimeters
