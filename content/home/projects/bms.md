+++
weight = 12
+++

{{% section %}}

{{< slide id="mkv-bms" >}}

# MKV BMS

_A battery management system for a 400V EV battery._

[Code repository](https://github.com/olin-electric-motorsports/olin-electric-motorsports/tree/main/vehicle/mkv/software/bms).
[Documentation](https://docs.olinelectricmotorsports.com/share/0ba70c22-4849-4f85-b3be-6f090aa76141).

<br />

<small>navigate down to learn more</small>

🔽

---

For the Olin Electric Motorsports MKV vehicle, we had a 400V battery pack built
with 864 _18650_ lithium batteries.

In order to ensure safe operation, we built a custom BMS. A few of my teammates
worked on the electrical systems and PCBs, and I wrote the firmware.

---

The BMS core uses isoSPI to communicate with peripheral boards, each containing
two LTC6811 battery management integrated chips.

I adapted Linear Technology's (now Analog Devices) drivers to fit our
microcontrollers, and implemented a 100 Hz loop that monitors the temperatures
and voltages.

---

In the future, I'm planning on taking things to the next level.

I'm planning to integrate state-of-charge estimation using an extended Kalman
filter algorithm, and integrate control loops to dynamically limit torque as a
function of battery temperature.
