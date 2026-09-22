# Peanut Models

This directory contains a collection of 3D models of Peanut if you want to
include it in your rocket.

* `peanut-board.step`: Just the board and mounting holes, no components
* `peanut-board.stl`: Same as above, but as an STL
* `peanut.step`: Board, mounting holes and components
* `peanut.stl`: Same as above, but as an STL

**NOTE:** It is recommended to check clearances using the models with components
populated. The buzzer is non-negligibly tall, and there are also components on
the underside of Peanut that prevent it from being seated completely flush to a
flat surface. Certainly don't mount it flush against anything conductive.

## Peanut Dimensions

* The board for Peanut is 24.5mm x 48.25mm with rounded corners
* Mounting holes are placed at opposite diagonals
* Mounting holes are centred on a rectangle of dimensions 18mm x 41mm
* Mounting holes are designed for M3 socket cap screws

Note that although the mounting holes are plated, they are electrically isolated
(not grounded, nor powered).
