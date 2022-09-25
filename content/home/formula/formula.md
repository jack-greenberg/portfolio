+++
weight = 5
outputs = ["Reveal"]
+++

{{% section %}}

{{< slide
  background-image = "/mkv.png"
  background-size = "65%"
  background-repeat = "no-repeat"
  background-position = "left bottom"
>}}

<div style="text-align: left">

<img style="border: none; box-shadow: none; margin: 0;" src="/oem-logo.png"
width="30%"/>

At Olin, I'm a member of [**Olin Electric
Motorsports**](https://www.olinelectricmotorsports.com), our Formula SAE electric
race car team.

I work on firmware, mostly for high voltage systems and tooling infrastructure.

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

---

<div style="text-align: right">
<img src="/service-section.jpg" width="50%" style="border: none; box-shadow:
none; margin-bottom: -4rem; margin-top: -4em;" />
</div>

<div style="text-align: left">

### High Voltage Power Distribution

I worked on the firmware for the [battery management system](#mkv-bms) and the
battery contactor controller.

I designed the firmware to be robust and _readable_. I believe that
safety-critical code should be easy to understand and as simple as possible.

</div>

---

<div style="text-align: left">

#### Battery Contactor Control

I implemented a state machine for controlling the battery contactors (also
called AIRs, or _accumulator isolation relays_). The firmware ensures safe
operation of the motor controller (precharge, discharge).

The entire state machine was fully tested using a pieced-together
hardware-in-the-loop test setup with a CAN dongle, an Arduino, and a **lot** of
jumper cables.

The state machine is diagrammed below.

[Code repository](https://github.com/olin-electric-motorsports/olin-electric-motorsports/tree/main/vehicle/mkv/software/air_control).
[Documentation](https://coda.io/d/Documentation_dbuFnC2EA_e/AIR-Control_sudaq#_luEBo).

</div>

<div style="text-align: right">
<img src="/air-minus.jpg" width="50%" style="border: none; box-shadow:
none; margin-bottom: -4rem; margin-top: -4em; z-index: -1; position: relative" />
</div>

---

{{< slide background-image="/air-control.png" background-size="contain" >}}

---

{{< slide
  background-image = "/mkv.png"
  background-size = "65%"
  background-repeat = "no-repeat"
  background-position = "left bottom"
>}}

<div style="text-align: left">

### Network Management

Along with another member of the team, I developed a new system for managing our
CAN bus.

We are able to descibe the CAN messages sent to and received from our ECUs in a
YAML format. These YAML files are used as inputs to a DBC generator, as well as
a C-source generator that provides us an API for sending and receiving the
messages.

</div>

---

{{< slide
  background-image = "/mkv.png"
  background-size = "65%"
  background-repeat = "no-repeat"
  background-position = "left bottom"
>}}

<div style="text-align: left">

### Tooling and Infrastructure

When I joined the team, our build system for compiling and flashing code
consisted of a Python file that invoked shell commands.

I introduced the Bazel build system to our team to make our code more
professional. We are able to build and flash any code from our monorepo using
Bazel.

</div>

{{% /section %}}
