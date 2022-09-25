+++
weight = 12
+++

{{% section %}}

{{< slide id="bms" >}}

# MKV BMS

_A battery management system for a 400V EV battery._

[Code repository](https://github.com/olin-electric-motorsports/olin-electric-motorsports/tree/main/vehicle/mkv/software/bms).
[Documentation](https://coda.io/d/Documentation_dbuFnC2EA_e/BMS_suuXG#_luh8U).

<br />

<small>navigate down to learn more</small>

🔽

<div style="text-align: right">
<img src="/accumulator.jpg" width="50%" style="border: none; box-shadow:
none; margin-bottom: -4rem; margin-top: -7em;" />
</div>

---

<div style="display: flex; flex-direction: row; align-items: top">
<div style="flex: 1 0 60%">
For the Olin Electric Motorsports MKV vehicle, we had a 400V battery pack built
with 864 <em>18650</em> lithium-ion batteries.

In order to ensure safe operation, we built a custom BMS. A few of my teammates
worked on the electrical systems and PCBs, and I wrote the firmware.
</div>
<div style="flex: 1 0 40%">
<img src="/segment.png" style="margin-top: -3em; height: 100%; border: none; box-shadow: none;" />
</div>
</div>

---

The BMS core uses isoSPI to communicate with peripheral boards, each containing
two LTC6811 battery management integrated chips.

I adapted Linear Technology's (now Analog Devices) drivers to fit our
microcontrollers, and implemented a 100 Hz loop that monitors the temperatures
and voltages.
