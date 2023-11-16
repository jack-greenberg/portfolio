+++
weight = 50
+++

{{% section %}}

{{< slide id="scope-pcb" >}}

# SCOPE PCB

_PCB for a single-watt scale electrical generator._

<p style="font-weight: bold; background-color: black; color: white;
display:inline-block; padding: 0.2em .4em">
Partially redacted due to NDA.
</p>

See the public-facing presentation [here].

[here]: https://www.youtube.com/live/s60-3mz0-UQ?feature=share&t=7825

<br />

<small>navigate down to learn more</small>

🔽

<div style="text-align: right">
<img src="/scope-pcb.png" width="50%" style="border: none; box-shadow:
none; margin-bottom: -4rem; margin-top: -12em;" />
</div>

---

For my senior capstone (SCOPE), I worked with a company to develop a single-watt
scale electrical generator. The motor is driven externally and the
microcontroller (STM32F3) uses PWM commutation to control the motor driver to
generate the optimal amount of energy to reduce startup torque.

<img src="/scope-pcb2.png" style="width: 150%" />

---

On board, there is a motor driver IC, a battery charging IC and battery
management system, a 5V buck converter, and a microcontroller. I developed the
entire board from scratch and testing will happen in Spring 2023.

I collaborated with a classmate on the firmware image for the microcontroller.
The code, written in **Rust**, implements a trapezoidal commutation for power
generation as well battery management for the two LiPo batteries used as energy
storage.

---

<img src="/scope-schematic.png" />

I developed the schematic and layout in KiCad, following best practices with
lots of review from professors and subject matter experts.

{{% /section %}}
