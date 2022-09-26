+++
weight = 13
+++

{{% section %}}

{{< slide id="air-control" >}}

# AIR Control

_High-voltage power distribution for an EV._

[Code repository](https://github.com/olin-electric-motorsports/olin-electric-motorsports/tree/main/vehicle/mkv/software/air_control).
[Documentation](https://coda.io/d/Documentation_dbuFnC2EA_e/AIR-Control_sudaq#_luEBo).

<br />

<small>navigate down to learn more</small>

🔽

<div style="text-align: right">
<img src="/service-section.jpg" width="50%" style="border: none; box-shadow:
none; margin-bottom: -4rem; margin-top: -7em;" />
</div>

---

In an electric vehicle, we need to safely connect our high voltage battery and
motor controller. However, connecting it directly is dangerous for the system—we
can end up with a massive surge of current and potentially weld our contactors
shut.

<div style="text-align: right">
<img src="/air-minus.jpg" width="50%" style="border: none; box-shadow:
none; margin-bottom: -4rem; margin-top: -4em; z-index: -1; position: relative" />
</div>

---

On our Formula team, I rewrote the firmware for the contactor control system
(which we call _AIR Control_ <small>1</small>). Because it is a safety-critical
system, I put a lot of focus on simplicity and robustness.

The system is implemented as a state machine and goes through precharging the
capacitance in the motor controller and handles fourteen possible faults.

<br />

<small>1: AIR stands for **accumulator isolation relay**</small>

---

I also designed a test rig that simulates the inputs to the microcontroller and
reads outputs over both GPIO and CAN. Tests are written in Python and fully
exercise the state machine.

The code is highly organized and commented so as to be simple to read and
straightforward to understand. This is important because safety-critical systems
need to be auditable and easily parseable by a human.
