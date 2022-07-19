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

<div style="text-align: left; margin: -2em -5em 0 0">

<img style="border: none; box-shadow: none; margin: 0;" src="/oem-logo.png"
width="30%"/>

At Olin, I'm a member of [**Olin Electric
Motorsports**](https://www.olinelectricmotorsports.com), our Formula SAE electric
race car team.

I work on firmware, mostly for _high voltage power distribution_ and _network
management_.

</div>

<br />
<br />

<small>navigate down to learn more</small>

🔽

---

{{< slide
  background-image = "/mkv.png"
  background-size = "65%"
  background-repeat = "no-repeat"
  background-position = "left bottom"
>}}

<div style="text-align: left">

### High Voltage Power Distribution

I worked on the firmware for the [battery management system](#mkv-bms) and the
battery contactor controller.

I designed the firmware to be robust and _readable_. I believe that
safety-critical code should be easy to understand and as simple as possible.

</div>

---

{{< slide
  background-image = "/mkv.png"
  background-size = "65%"
  background-repeat = "no-repeat"
  background-position = "left bottom"
>}}

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
[Documentation](https://docs.olinelectricmotorsports.com/share/13fffae6-b6f3-4f28-8fd8-b853e9c5ab8c).

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
