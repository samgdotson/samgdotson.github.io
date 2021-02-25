---
layout: post
title: Powering a Mars Colony - Wind
tags:
- energy
- nuclear
- wind
- solar
- space
- Mars
---

<!-- Adds MathJax -->
<script type="text/javascript" async
src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

# Could Wind Power a Mars Colony?

I started reading _Red Mars_ by Kim Stanley Robinson last week and was struck
by Robinson's description of nuclear energy on Mars. The first reactor on Mars
is a "Rickover" reactor. These reactors are a type of pressurized-water reactor
used in nuclear powered submarines. This choice makes sense to me, yet there
was one character in the book that claimed

> [They] were not reassured by Arkady sending radio messages down from Phobos
> insisting that they did not need such a dangerous technology, that they could
> get all the power they needed from wind generation. -- Kim Stanley Robinson, Red Mars

Of course I stopped reading to figure out if this could actually work. First, I needed
to answer some basic questions:

1. How can we calculate the power produced by a wind turbine?
2. What is the air density on Mars?
3. What is the average wind speed on Mars?

By answering these questions, we can figure out if a Mars colony could reasonably
be powered by wind energy.

### Deriving the Function for Wind Powering

Wind turbines essentially convert the kinetic energy of air (wind) into electricity.
The equation for kinetic energy is simply,

$$ KE = \frac{1}{2}mv^2 \text{    [J]},$$

where _m_ is the mass of air flowing and _v_ is the velocity of that air.
But we want to know how much _power_ this kinetic energy will produce over a
certain period of time. To do that we simply change _m_ into $$\dot{m}$$ to indicate
the _flow_ of mass through the turbine blades.

$$ P_{turbine} = \frac{1}{2}\dot{m}v^2 \text{    [J/s]}.$$

We're not quite done yet, though. Without measuring the total mass of air
passing through the blades at each moment, we can't know how much power it
produces. Fortunately, we can rewrite _mass_ in terms of density and a volume
of flow, $$\dot{V}$$. We can further rewrite this volume flow as a cross-section
area times a flow velocity, _v_. So we have

$$ P_{turbine} = \frac{1}{2}\rho \dot{V} v^2  \text{    [J/s]},  $$

and finally,

$$ P_{turbine} = \frac{1}{2}\rho \pi L^2 v^3  \text{    [J/s]}.  $$

Where _L_ is the length of the turbine blade. From this we can see that
wind power is proportional to the cube of wind speed and only linearly
related to the density of the air. This is potentially good news since Mars, despite
having 1/100th the atmosphere of Earth, is known for its dust storms. Does this
mean it's windy enough to sustain a Mars colony?

### Best Case Scenario
It turns out that wind is not
much faster on Mars than it is on Earth, with average speeds around 10 m/s. The
[fastest recorded wind speed](https://sciencing.com/average-wind-speed-mars-3805.html)
on Mars is 30 m/s, during a dust storm. The average wind speed in the United
States is around 5 m/s. This is good news for Mars, but there is a competing
effect from Mars' thin atmosphere. The greatest density for Mars' atmosphere is
roughly equal to the density of [Earth's atmosphere at 35 km](https://en.wikipedia.org/wiki/Atmosphere_of_Mars).
That density is approximately $$ \rho_{Mars} \approx \rho_{Earth}|_{35km} \approx
0.0112 $$, calculated with linear interpolation of [data](https://www.engineeringtoolbox.com/standard-atmosphere-d_604.html).

Now we can calculate the ratio of wind power on Mars to wind power on Earth,
and we can plug in some numbers ($$ \rho_{E} \approx 1.225 kg/m^3 $$ at sea level)

$$ \frac{P_{M}}{P_{E}} = \frac{\frac{1}{2}\rho_{M} \pi L^2 v_{M}^3}{\frac{1}{2}\rho_{E} \pi L^2 v_{E}^3} $$

$$ \frac{P_{M}}{P_{E}} = \frac{\rho_{M} v_{M}^3}{\rho_{E} v_{E}^3}
= \frac{(0.0112)(30)^3}{(1.225)(5)^3} \approx 1.975$$

So, at _best_ placing a wind turbine on Mars will generate twice as much power
as an identical turbine on Earth (roughly speaking). But that was calculated using
the highest recorded wind speed on mars. What if we use the average wind speeds
for both?

### Average Windspeeds

The [average wind speed on mars](https://sciencing.com/average-wind-speed-mars-3805.html)
ranges from 2 m/s to 7 m/s in the Martian summer and 5 m/s to 10 m/s in the Martian fall.

Let's take the highest value, once again.

$$ \frac{P_{M}}{P_{E}} = \frac{\rho_{M} v_{M}^3}{\rho_{E} v_{E}^3}
= \frac{(0.0112)(10)^3}{(1.225)(5)^3} \approx 0.073$$

Even if the wind speed averaged 10 m/s year round, at best a wind turbine on
Mars would generate just 7% of the energy an identical turbine on Earth would
produce. I also neglected that fact that wind turbines have an ideal operating
range and a "cut off" speed. The turbine produces the same power throughout
its ideal range and the turbine is stopped beyond its cut off speed for safety
reasons. If we applied the ideal range of velocities to our above equation,
air density becomes the dominant factor.

_The lesson here is that 1/100th of the air density means 1/100th of the power output_.


### Final Thoughts

Not only do wind turbines produce far less energy on Mars than they do on Earth,
but they also have an exceptionally low power density. This means it would be
impossibly expensive to launch all of the necessary materials to build wind
turbines on Mars.

The answer in _Red Mars_ is that nuclear power is required. "_Shikata na gai_,
_there is no other choice_."
