+++
weight = 11
+++

{{% section %}}

{{< slide id="can-bootloader" >}}

# CAN Bootloader

_A bootloader that can reprogram chips using CAN._

[Github
link.](https://github.com/olin-electric-motorsports/olin-electric-motorsports)

<br />

<small>navigate down to learn more</small>

🔽

---

<img src="/usbasp.jpg" width="30%" />

Historically, whenever we wanted to update the firmware on our circuit boards,
we had to use an _in-system programming (ISP) dongle_ and plug into each board
manually.

This often meant opening up enclosures, and required us to have a large
programming header on each board, adding height and exposed copper.

---

As a personal project, I developed a bootloader for the ATmega16m1, the
microcontroller we use on the team, that allows us to update the firmware of
_any_ ECU on our CAN bus.

<br />

* No more programming dongles
* No more opening enclosures
* No more large programming headers

---

The bootloader runs when the chip receives power, checks EEPROM for a validity
stamp on the image, and then boots into either the image or the updater.

The updater uses a state-based approach for doing firmware updates:

---

{{< slide background-image="/btldr-state.png" background-size="contain" >}}

---

The bootloader is accompanied by a shell script that allows users to ping and
firmware-update the boards based on a preset ECU ID.

<br />

You can find the code for the project [here](https://github.com/olin-electric-motorsports/olin-electric-motorsports).

{{% /section %}}
