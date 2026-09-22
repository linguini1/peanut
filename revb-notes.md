# Revision B Notes

Notes for improvements that could be made to Revision B.

- BMP581 so far is incredibly unreliable in manufacturing. It would be good to
  pick another barometer that:
  - Is easier to solder (not LGA)
  - Has an interrupt line
  - Has an I2C interface
  - Possibly has a higher maximum altitude
  - Comparable sampling rate and reasonable precision

- Battery voltage divider might be better suited to have higher sensitivity in
  the range of 3V2 to 4V2 instead of from 0V to 4V2.
  - Connected batteries shouldn't drop below a certain minimum voltage (above
    0V)
  - The device will brown-out on the LDO before 3V3/3V2 anyways

- I2C pull-ups should be 2k2, 10k is a little high and it's not saving much cost

- Is a PWM buzzer a good idea? For playing jingles?

- Ensure manufacturer removes serial number from silkscreen
