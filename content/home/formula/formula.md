+++
weight = 5
outputs = ["Reveal"]
+++

{{% section %}}

<div style="text-align: right">
<img src="/mkv.png" width="60%" style="border: none; box-shadow:
none; margin-bottom: -4rem; margin-bottom: -5em;" />
</div>

<div style="text-align: left">

<img style="border: none; box-shadow: none; margin: 0;" src="/oem-logo.png"
width="30%"/>

At Olin, I'm a member of [**Olin Electric
Motorsports**](https://www.olinelectricmotorsports.com), our Formula SAE electric
race car team.

Below you can learn more about what I worked on each year on the team!

</div>

<br />
<br />
<br />

<small>navigate down to learn more</small>

🔽

---

<div style="text-align: right">
<img src="/bspd.svg" width="40%" style="border: none; box-shadow:
none; margin-bottom: -7rem; margin-top: -7em;" />
</div>

# Year 1

As a first-year on the electrical subteam, I designed, fabricated, and tested a
PCB called the _Brake System Plausibility Device_, or BSPD.

This is a safety-critical board that will shutdown the car if power is being
delivered to the motor while the brake pedal is pressed for longer than half a
second. The throttle system should prevent torque requests during braking, but
this circuit acts as a fail-safe.

---

<div style="text-align: right">
<img src="/telemetry-radio.png" width="40%" style="border: none; box-shadow:
none; margin-bottom: -7em; margin-top: -7em;" />
</div>

# Year 2

As a sophomore, I founded and led the telemetry subteam. We worked on a system
to stream data from our vehicle's CAN bus to an off-board computer in real-time.
I led the system design and worked with other senior engineers to execute
testing and an initial implementation of the system.

This was during a remote year (due to the Covid-19 pandemic), so keeping members
engaged proved to be the biggest challenge. But through team bonding events,
regular meetings and 1:1s, we were able to lay a solid foundation for the
following year.

---

<div style="text-align: right">
<img src="/air-minus.jpg" width="30%" style="border: none; box-shadow:
none; margin-bottom: -6em; margin-top: -6em;" />
</div>

# Year 3

As a junior, I decided to revamp our entire system for writing firmware and
designing PCBs. This included a lot of projects:

* I moved the team to a [monorepo] that has all of our electrical and software
  work.

* I collaborated with teammates on a system to describe our CAN bus using a YAML
  spec that would be compiled into a DBC file as well as generated into a C
  library.

* I worked on revamping our entire firmware system, including writing libraries
  for SPI, UART, CAN, ADC, timers, and more for our microcontroller, and rewrote
  most of our firmware images to use these libraries.

[monorepo]: https://github.com/olin-electric-motorsports/olin-electric-motorsports

This was a busy year...

---

# Year 4

As a senior, I decided to scale back my technical contributions to the team in
favor of engaging in _knowledge transfer_. Over the summer, I led a series of
sessions in which I taught the incoming electrical subteam leads about the
fundementals of embedded systems and how to write low-level code. I also led
talks on the systems of our car including high-voltage power distribution.

I also took on the role of financial manager on the team, organizing a $65,000
budget. My goal is to be as transparent as possible with the rest of the team as
well as with Olin College, and I achieved this by organizing regular financial
updates and keeping in close contact with the Olin finance offices.
