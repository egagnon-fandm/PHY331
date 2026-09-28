# Solution: Discovery Exercise for Conservative Vector Fields (Section 8.11)

**Summary**: Worked solutions to all eight parts of the Chapter 8 discovery exercise on conservative vector fields.

**Sources**: textbook/felder/raw/allexercises/vectorsdiscovery-conservativevectorfields.pdf; [[exercise-vectors-discovery-conservative-vector-fields]]

**Last updated**: 2026-09-23

---

All paths run from $(1,0)$ to $(0,1)$:

- **Path 1**: left along $y=0$ to the origin, then up along $x=0$.
- **Path 2**: up along $x=1$ to $(1,1)$, then left along $y=1$.
- **Path 3**: straight line, $x = 1-t,\ y = t,\ 0\le t\le 1$ (so $dx=-dt$, $dy=dt$).

In 2D, $\vec v\cdot d\vec s = v_x\,dx + v_y\,dy$.

## Field 1: $\vec v_1 = x\,\hat\imath + x\,\hat\jmath$, so $\vec v_1\cdot d\vec s = x\,dx + x\,dy$

**1. Path 1.**
- Leg $y=0$ ($dy=0$): $\int_1^0 x\,dx = -\tfrac12$.
- Leg $x=0$ ($x=0$ everywhere): integrand is $0$.
- Total: $\boxed{-\tfrac12}$

**2. Path 2.**
- Leg $x=1$ ($dx=0$): $\int_0^1 1\,dy = 1$.
- Leg $y=1$ ($dy=0$): $\int_1^0 x\,dx = -\tfrac12$.
- Total: $\boxed{+\tfrac12}$

**3. Path 3.**
$$\int_0^1 \big[(1-t)(-1) + (1-t)(1)\big]dt = \int_0^1 0\,dt = \boxed{0}$$

Three paths, three different answers: $\int_C \vec v_1\cdot d\vec s$ is **path-dependent**.

## Field 2: $\vec v_2 = 2xy\,\hat\imath + x^2\,\hat\jmath$, so $\vec v_2\cdot d\vec s = 2xy\,dx + x^2\,dy$

**4. Path 1.**
- Leg $y=0$: $2xy\,dx = 0$ (and $dy=0$). Contribution $0$.
- Leg $x=0$: $x^2\,dy = 0$ (and $dx=0$). Contribution $0$.
- Total: $\boxed{0}$

**5. Path 2.**
- Leg $x=1$ ($dx=0$): $\int_0^1 (1)^2\,dy = 1$.
- Leg $y=1$ ($dy=0$): $\int_1^0 2x\,dx = \big[x^2\big]_1^0 = -1$.
- Total: $1 - 1 = \boxed{0}$

**6. Path 3.**
$$\int_0^1 \big[2(1-t)t(-1) + (1-t)^2(1)\big]dt = \int_0^1 (1-t)(1-3t)\,dt = \int_0^1 (1 - 4t + 3t^2)\,dt$$
$$= \big[t - 2t^2 + t^3\big]_0^1 = 1 - 2 + 1 = \boxed{0}$$

All three paths agree: $\int_C \vec v_2\cdot d\vec s$ is **path-independent**, so $\vec v_2$ is **conservative**.

## The gradient theorem check

**7. Show $\vec\nabla f = \vec v_2$ for $f(x,y)=x^2y$.**
$$\vec\nabla f = \frac{\partial f}{\partial x}\hat\imath + \frac{\partial f}{\partial y}\hat\jmath = 2xy\,\hat\imath + x^2\,\hat\jmath = \vec v_2 \ \checkmark$$

**8. Compare with $f(0,1) - f(1,0)$.**
$$f(0,1) - f(1,0) = (0^2\cdot 1) - (1^2\cdot 0) = 0 - 0 = 0$$
This matches all three line integrals in parts 4–6. By the [[gradient-theorem]], $\int_C \vec\nabla f\cdot d\vec s = f(\text{end}) - f(\text{start})$ for any path, so no path computation was ever needed.

## Take-away

- $\vec v_1$ is not a gradient field (its curl $\partial_x v_y - \partial_y v_x = 1 \ne 0$), so its integrals depend on the path.
- $\vec v_2$ is a gradient field (curl $= 2x - 2x = 0$), so its integrals depend only on the endpoints.

## Related pages

- [[exercise-vectors-discovery-conservative-vector-fields]]
- [[conservative-vector-fields]]
- [[gradient-theorem]]
