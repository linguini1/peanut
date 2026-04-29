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
- [ ] Pin assignment to component footprint is correct (check _all_
      non-passives)
- [ ] Connections to FETs are correct

## Component Ratings

- [ ] Component values are correct for their use (correct resistance,
      capacitance, etc.)
- [ ] Components passing high power have sufficient wattage
- [ ] LED circuits are properly connected for forward voltage + resistance
- [ ] FETs have correct activation voltage
- [ ] FETs can pass sufficient current
- [ ] Max current draw can be supplied by the regulator
- [ ] RF matching circuitry has correct values

## Correctness

- [ ] All LEDs have resistors
- [ ] All switching NMOS FETs have gate pull-downs
- [ ] Voltage dividers are correct for all possible input/output ranges
- [ ] Load capacitance for clock is correct
- [ ] Boot/enable circuitry is correct for MCU
- [ ] Pin assignments for MCU are correct

## Routing

- [ ] High current traces can supply sufficient current
- [ ] Via stitching around clock
- [ ] Via stitching around RF trace
- [ ] USB routed as 90ohm differential pair
- [ ] RF routed as 50ohm impedance matched
- [ ] RF trace below critical length
- [ ] RF routing matches application note suggestion (antenna/ESP32)
- [ ] All fill zones poured
- [ ] Minimal 0402 sized components on back, only if hand-solderable

## Silkscreen

- [ ] Logo is visible on top side
- [ ] Revision is visible on top side
- [ ] Pyro channels are clearly labelled
- [ ] All LEDs are clearly labelled
- [ ] Arming terminal is clearly labelled
- [ ] Boot jumpers are clearly labelled
- [ ] Components on back-side are sufficiently short for mounting
- [ ] Mounting holes have a hole pattern with distances in whole millimeters
