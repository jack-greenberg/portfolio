+++
weight = 70
+++

{{% section %}}

{{< slide id="gauntlet" >}}

# The Gauntlet

_Gradient descent algorithm simulated for a<br />differential-drive robot._

<small>navigate down to learn more</small>

🔽

<div style="text-align: right">
<img src="/gauntlet-contour.svg" width="40%" style="border: none; box-shadow:
none; margin-bottom: -4rem; margin-top: -4em; z-index: -1; position: relative" />
</div>

---

<img src="/gauntlet.png" style="width: 50%; display: block; margin: 0 auto;"/>

For my Quantitative Engineering Analysis course (sophomore year), the goal of
the final project was to navigate a simulated Roomba-like robot through a world
called The Gauntlet, avoiding obstacles (boxes) until finally reaching the goal
(cylinder).

---

The robot was equiped with a LIDAR camera that sampled points around it. I used
a *random sample consensus (RANSAC)* algorithm to organize the individual points
from LIDAR into a series of lines and a circle (the goal).

From the lines and the circle, the code then generated a vector field and then
apply _gradient descent_ to navigate the robot towards the goal.

{{% /section %}}
