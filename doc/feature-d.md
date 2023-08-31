

# **Pendulum With Drag**

In a simple pendulum we have a periodic movement, that is, a movement that goes and returns. If we drew the force diagram of the movement, we would have something like this:

![](pendulum1.jpg)

When we talk about a simple pendulum, we mean that the angle {math}`\theta` is never greater than {math}`sin(15°)`, so this implies that {math}`sin(\theta) ≈ \theta` so we do not have a chaotic movement, as we will see a case later. If we wrote Newton's equations for this movement we would have:

```{math}
\sum F_{x} = -Tsen(\theta) = m \frac {d^2x}{dt^2}

\sum F_{y} = Tcos(\theta) - mg = m \frac {d^2y}{dt^2}
```

As we see here, we have two equations to solve a system with three unknowns. This system becomes very ineffective and complex to solve, so the easiest solution is to **translate the system to polar coordinates**. To take a good look at how the movement would be described in polar coordinates, let's look at the following image:

![](pendulum2.jpg)

If we were to write Newton's equations for this "new system", we would have:

```{math}
\sum F_{r} = T - mgcos(\theta) = m\frac {d^2 r}{dt^2}

\sum F_{\theta} = -mg sin(\theta) = m \frac {dv_{\theta}}{dt}
```

If we look at the image we can see that {math}`r` is the length of the string, so its derivative is a constant so it is {math}`0`. In addition, the equation of the sum of forces in {math}`\theta` can be described in a different way since the speed in this movement would be given by: {math}`r \frac {d\theta}{dt}`
then the equations are described as follows:

---
```{math}
T-mgcos(\theta) = 0

T = mgcos(\theta)

\frac {d^2\theta}{dt^2} = \frac {-g}{l} sen(\theta)
```
---

And these would be the equations that we must solve numerically.


