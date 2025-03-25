# Assignment-H5-Control-Aircraft-pitch-control

You need to design a control system for the pitch of an aircraft. The system is illustrated in Figure 1.
The manipulated input is the elevator deflection angle, $$\delta$$; changing the deflection rate affects the pitch
of the aircraft. In Figure 1, $$\alpha$$ denotes the angle of attack, which is the angle between the longitudinal
axis of the aircraft and its velocity vector. The pitch angle of the aircraft is denoted by $$\theta$$. The pitch
rate is denoted by $$r$$.

![image](https://github.com/user-attachments/assets/8d175db8-09d2-4563-a051-fd28ca65e91c)

Figure 1: Illustration of an aircraft with its pitch angle, $$\theta$$, the angle of attack, $$\alpha$$, and the deflection
angle of the elevators, $$\delta$$. The angle $$γ = \theta − \alpha$$ is known as the slope.

The system dynamics is described by the following system of differential equations 

$$
\dot{\alpha} = -0.31\alpha + 57.4r + 0.232\delta,
$$

$$
\dot{r} = -0.016\alpha - 0.425r + 0.0203\delta,
$$

$$
\dot{\theta} = 56.7r.
$$

where all quantities are in SI units1. In addition, the deflection angle of the elevators is controlled by
an actuator whose dynamics has been found to be of the first order with unit static gain and a time
constant of 14.5 ms. The sensor has the transfer function

$$Gm(s) = \frac{exp(−0.0063s)}{0.0021s + 1}$$

(In Equation (1), $$\alpha$$, $$\theta$$ and, $$\delta$$ are measured in radians — not degrees — and q is measured in radians per second.)

The task of your team is to:

1 - Present a complete analysis of the given dynamics: Your report should include a detailed
study of the properties of the open-loop dynamics and your results should be accompanied by
appropriate plots. Your report must also include a block digram of the control system.

2 - Design an appropriate controller for the system: Your controller needs to satisfy the stan-
dard requirements for a closed-loop control system. You need to make sure that the controlled
system is BIBO-stable and that there is zero offset. Additionally, you may want to check how
your closed-loop system will behave in presence of disturbances. You need to consider what sort
of possible disturbances may be present. You should tune your controller to achieve reasonable
stability margins and of course to exhibit a desirable (not highly oscillatory, not overly slow, not
too aggressive) closed-loop behaviour.
