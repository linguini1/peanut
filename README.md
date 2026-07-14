# Peanut

<p align="center">
    <img style="align:center" width="70%" src="./docs/assets/fingers-for-scale.jpg" />
    <br/>
    Peanut Altimeter with my fingers for scale
</p>

<p align="center">
    <img style="align:center" width="70%" src="./docs/assets/usb-for-scale.jpg" />
    <br/>
    Peanut Altimeter powered up and operational
</p>

<p align="center">
    <img style="align:center" width="70%" src="./docs/assets/peanut_render.png" />
    <br/>
    Peanut Altimeter KiCAD render
</p>

A modern, tiny, and hackable altimeter for hobby rocketry. Features include:

* Fits in a min-diameter 29mm rocket
* High accuracy barometric pressure sensor (up to ~9km)
* Dual deploy capable (two pyro channels)
* Visual continuity LEDs
* On-board 2MB storage (4MB, 2MB for program, 2MB for logs)
  * Altitude measurements
  * Flight events (ascent, apogee, landing, etc.)
  * Deployment events
* Mach dip filtering (works on flights that break Mach)
* Audio arming indicator
* Bluetooth connection
  * Deployment testing with flight simulations over BLE
  * Configuration over BLE
  * Continuity & other telemetry over BLE
* WiFi capable

**Thank you to [PCBWay][pcbway] for sponsoring the manufacture of this project's
PCBs!**

## Firmware

The firmware for this board is made using the [Apache NuttX RTOS][nuttx-site],
an open-source embedded RTOS with an incredible community and an excellent
feature set.

Firmware is spread across a few repositories. If you are compiling yourself,
you'll need:
- [The NuttX kernel source][nuttx]
- [The NuttX application library][nuttx-apps]
- [The Peanut board support package][peanut-bsp]
- [My application-level altimeter software][rocket-altimeter]

## Hackability

All hardware designs & firmware for Peanut are open-sourced and available under
permissive licensing.

The device itself is programmable over the USB-C interface, so users can tweak
the firmware or write their own and re-program the device. Want the buzzer to
play custom audio? Want to change the meaning of the "START" LED? Want to add
more features to the Bluetooth interface, or make the altimeter operate over
WiFi instead? You can program whatever you want into it.

## Make Your Own

If you want to make your own Peanut Altimeter, the component cost for the board
is roughly $30 CAD. You can get PCB blanks from a manufacturer of your choice
(i.e. PCBWay). You should only need to verify the trace widths of the
Bluetooth RF trace depending on the differences between your manufacturer's
PCB stackup and mine.

**NOTE:** This board was not designed with hand-soldering in mind (aside from
the backside). My manufacture process is to use solder paste, a stencil and a
hot plate to do the top-side components. There are 0402 components which are
manageable with steady hands and tweezers.

## On PCBWay

My experience using PCBWay could not have been easier. They provide a plugin for
KiCAD that directly exports your manufacturing files for order to their web
quote interface. I only hand to click the button and choose some parameters for
my board to get everything ordered.

My designs arrived on time, well package and the stencil was really high quality
with a large aluminum frame. I had no issues with the fine details (in copper
and on silkscreen) with such a small board, PCBWay nailed it.

[nuttx]: https://github.com/apache/nuttx
[nuttx-apps]: https://github.com/apache/nuttx-apps
[nuttx-site]: https://nuttx.apache.org/
[rocket-altimeter]: https://github.com/linguini1/rocket-altimeter
[peanut-bsp]: https://github.com/linguini1/peanut-bsp
[pcbway]: https://www.pcbway.com/
