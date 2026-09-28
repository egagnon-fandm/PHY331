# Equation Sheet — Chapters 1–4 (Felder & Felder)

**Summary**: Quiz-ready equation sheet covering Chapter 1 (Intro to ODEs), Chapter 2 (Taylor Series & Convergence), Chapter 3 (Complex Numbers), and Chapter 4 (Partial Derivatives).

**Sources**: textbook/felder/wiki chapter-1 through chapter-4 pages and their linked concept pages; appendix-b-taylor-series-reference.

**Last updated**: 2026-09-19

---

## Chapter 1 — Introduction to Ordinary Differential Equations

**Simple harmonic oscillator (SHO) equation** — memorize this one:
```
x''(t) = -ω²x(t)
x(t) = A cos(ωt) + B sin(ωt)   =   C cos(ωt + φ)
```
Period: `T = 2π/ω`. Note `ω` is fixed by the physics, not an arbitrary constant.

**Separation of variables** (first-order ODEs of the form (fn of y)dy = (fn of x)dx):
1. Separate y's (with dy) from x's (with dx)
2. Integrate both sides, `+C` on one side only
3. Solve algebraically for the dependent variable

**Guess and check**: propose a form (often `x(t) = e^{pt}` for constant-coefficient equations), substitute, solve algebraically for the constant(s).

**Principle of linear superposition** (linear, homogeneous equations only): if `y₁, y₂` are solutions, so is `Ay₁ + By₂` for any constants A, B.
- Combine n independent guess-and-check solutions of an nth-order linear homogeneous equation: `y = A₁y₁ + A₂y₂ + ... + Aₙyₙ`.

**Complementary equation method** (linear, inhomogeneous equations):
```
y = y_particular + y_complementary
```
1. Find one particular solution `y_p` (any solution, often by inspection)
2. Solve the complementary (homogeneous) equation — right side set to 0 — via guess-and-check + superposition, giving `y_c`
3. General solution: `y = y_p + y_c`

**Equilibrium solution**: constant value where `dy/dt = 0`. Stable if nearby states move toward it, unstable if they move away.

---

## Chapter 2 — Taylor Series and Series Convergence

**Linear approximation** (tangent line at `x = x0`):
```
y = f(x0) + f'(x0)(x - x0)
```

**Maclaurin series** (Taylor series centered at `x = 0`):
```
f(x) = c0 + c1x + c2x² + c3x³ + ... = f(0) + f'(0)x + f''(0)x²/2! + f'''(0)x³/3! + ...
```

**Taylor series** (centered at `x = a`):
```
f(x) = Σ [f⁽ⁿ⁾(a)/n!] (x-a)ⁿ = f(a) + f'(a)(x-a) + f''(a)/2!·(x-a)² + f'''(a)/3!·(x-a)³ + ...
```

**Common Maclaurin series to know:**
```
eˣ      = Σ xⁿ/n!                  = 1 + x + x²/2! + x³/3! + ...
sin x   = Σ (-1)ⁿ x^(2n+1)/(2n+1)! = x - x³/3! + x⁵/5! - ...
cos x   = Σ (-1)ⁿ x^(2n)/(2n)!     = 1 - x²/2! + x⁴/4! - ...
1/(1-x) = Σ xⁿ                     = 1 + x + x² + x³ + ...          (|x| < 1)
(1+x)^p = 1 + px + p(p-1)x²/2! + p(p-1)(p-2)x³/3! + ...              (|x| < 1)
```
Ways to build new series from known ones: substitution, multiply/divide by a power of x, differentiate/integrate both sides, ordinary algebra.

**Geometric series:**
```
Finite sum:    S = a1·(1 - rⁿ)/(1 - r)
Infinite sum:  S = a1/(1 - r)     converges iff |r| < 1
```

**Convergence — definition:** series `Σaₙ` converges iff `lim(n→∞) Sₙ` (the nth partial sum) exists.

**nth-term test:** if `lim(n→∞) aₙ ≠ 0`, then `Σaₙ` diverges. (Cannot prove convergence.)

**Ratio test** (primary tool for power series): for `Σaₙ`, let `L = lim(n→∞) |a_(n+1)/aₙ|`.
- `L < 1` → converges
- `L > 1` → diverges
- `L = 1` → inconclusive (check endpoints separately)

**Other convergence tests** (used mainly to resolve interval-of-convergence endpoints):
```
p-series:            Σ 1/nᵖ            converges iff p > 1
Integral test:       Σaₙ converges iff ∫₁^∞ f(x)dx converges  (f continuous, positive, decreasing, f(n)=aₙ)
Basic comparison:    0 ≤ aₙ ≤ bₙ, Σbₙ converges ⟹ Σaₙ converges
Limit comparison:    lim(aₙ/bₙ) finite & nonzero ⟹ Σaₙ, Σbₙ share convergence behavior
Alternating series:  Σ(-1)ⁿ⁻¹bₙ converges if bₙ > 0, eventually decreasing, and bₙ → 0
```
- **Absolute convergence**: `Σ|aₙ|` converges (implies `Σaₙ` converges).
- **Conditional convergence**: `Σaₙ` converges but `Σ|aₙ|` diverges.

**Interval of convergence**: ratio test gives `|x - a| < R`; each endpoint `x = a ± R` must be checked separately with the tests above.

---

## Chapter 3 — Complex Numbers

**Basic definitions:**
```
i ≡ √(-1),   i² = -1
z = a + bi        (a = Re(z), b = Im(z))
```

**Powers of i cycle with period 4:**
```
i¹ = i,  i² = -1,  i³ = -i,  i⁴ = 1, ...
```

**Complex conjugate:**
```
z* = a - bi
zz* = a² + b² = |z|²
```

**Complex plane (modulus / phase):**
```
z = x + iy
|z| = √(x² + y²) = √(zz*)         (modulus)
tan φ = y/x                        (phase)
x = |z| cos φ,   y = |z| sin φ
```

**Multiplication rule**: moduli multiply, phases add.
```
z1·z2 has modulus |z1||z2| and phase (φ1 + φ2)
```

**Euler's Formula:**
```
e^(ix) = cos x + i sin x
```

**Exponential (polar) form of a complex number:**
```
z = a + bi = |z| e^(iφ)
```

**Complex exponentials and oscillation (a, b real):**
```
e^(at)        — pure growth (a>0) or decay (a<0)
e^(ibt)       — pure oscillation, period 2π/b
e^((a+ib)t)   — oscillation of period 2π/b with amplitude growing/decaying like e^(at)
```

**Complex exponential method for driven ODEs:**
1. Replace real forcing term (e.g. `F0 cos(ωt)`) with complex exponential `F0 e^(iωt)`
2. Solve the complex equation by guess-and-check, `X(t) = X0 e^(iωt)`
3. Take `x(t) = Re(X(t))` (or `Im(X(t))` if forcing was a sine)

---

## Chapter 4 — Partial Derivatives

**Partial derivative definition:**
```
∂y/∂x = lim(Δx→0) [y(x+Δx, t) - y(x,t)] / Δx
```

**Schwarz's Theorem (mixed partials commute):**
```
∂²z/∂x∂y = ∂²z/∂y∂x
```

**Multivariate chain rule** (single chain):
```
dz/dx = (dz/dy)(dy/dx)
```
**Multivariate chain rule** (branching dependency, e.g. S depends on c, g; both depend on t):
```
dS/dt = (∂S/∂c)(dc/dt) + (∂S/∂g)(dg/dt)
```
**Total differential:**
```
dz = (∂z/∂x)dx + (∂z/∂y)dy
```

**Implicit differentiation**: differentiate both sides of a relating equation with respect to the variable of interest (using the chain rule on unknown functions), then solve algebraically for the desired derivative.

**Directional derivative** (û a unit vector):
```
D_û f(r⃗) = lim(h→0) [f(r⃗ + h·û) - f(r⃗)] / h
D_û f = (∂f/∂x)ux + (∂f/∂y)uy + (∂f/∂z)uz  =  ∇f · û
```

**Gradient:**
```
∇f = (∂f/∂x)î + (∂f/∂y)ĵ + (∂f/∂z)k̂
```
Points in the direction of steepest increase; magnitude = rate of increase in that direction. `∇f · û = 0` ⟹ û is tangent to the contour line through that point.

**Critical points & second derivatives test** (2 variables, critical point (a,b) where ∇f = 0 or undefined):
```
D(x,y) = (∂²f/∂x²)(∂²f/∂y²) - (∂²f/∂x∂y)²
```
- `D > 0` and `∂²f/∂x² > 0` → local minimum
- `D > 0` and `∂²f/∂x² < 0` → local maximum
- `D < 0` → saddle point
- `D = 0` → inconclusive

`D` is the determinant of the Hessian matrix `[[∂²f/∂x², ∂²f/∂x∂y], [∂²f/∂y∂x, ∂²f/∂y²]]`.

**Lagrange multipliers** (optimize f subject to constraint g = k):
```
∇f = λ∇g
```
(With multiple constraints `gᵢ = kᵢ`: `∇f = Σ λᵢ∇gᵢ`.)

Sensitivity interpretation:
```
dV ≈ λ · dC     (change in optimal value ≈ λ × change in constraint level)
```

---

## Related pages

- [[chapter-1-introduction-to-odes]]
- [[chapter-2-taylor-series-and-series-convergence]]
- [[chapter-3-complex-numbers]]
- [[chapter-4-partial-derivatives]]
- [[appendix-b-taylor-series-reference]]
- [[appendix-c-series-convergence-tests]]
