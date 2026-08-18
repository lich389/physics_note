
We construct an action for a relativistic perfect fluid in flat spacetime using Lagrange multipliers to enforce the conservation of particle number, the advection of entropy, and the normalization of the four-velocity. Varying the action yields the equations of motion, which are shown to be equivalent to the conservation of the energy-momentum tensor for a perfect fluid.

 ### Action
Consider a fluid with particle number density $n$, four-velocity $u^\mu$ (satisfying $u_\mu u^\mu = -1$), and entropy per particle $s$. The energy density $\rho(n,s)$ obeys the thermodynamic relations  
$$
d\rho = \mu \, dn + nT \, ds , \qquad \mu = \frac{\partial \rho}{\partial n}, \quad T = \frac{1}{n}\frac{\partial \rho}{\partial s},
$$  
and the pressure is $p = n\mu - \rho$. 
<!--In flat spacetime (signature $-+++$), the action is  
$$
S = \int d^4x \left[ -\rho(n,s) + \phi \,\partial_\mu (n u^\mu) + \psi \, u^\mu \partial_\mu s + \lambda (u_\mu u^\mu + 1) \right],
$$  
where $\phi$, $\psi$, and $\lambda$ are Lagrange multiplier fields.

### Variation
Treat $n$, $u^\mu$, $s$, $\phi$, $\psi$, and $\lambda$ as independent fields. The variation $\delta S = 0$ gives:

- From $\delta\phi$:  
  $$
  \partial_\mu (n u^\mu) = 0 \quad \text{(particle conservation)}. \tag{1}
  $$
- From $\delta\psi$:  
  $$
  u^\mu \partial_\mu s = 0 \quad \text{(entropy advection)}. \tag{2}
  $$
- From $\delta\lambda$:  
  $$
  u_\mu u^\mu = -1. \tag{3}
  $$
- From $\delta n$:  
  $$
  -\mu - u^\mu \partial_\mu \phi = 0 \quad \Rightarrow \quad u^\mu \partial_\mu \phi = -\mu. \tag{4}
  $$
- From $\delta u^\mu$:  
  $$
  -n \partial_\mu \phi + \psi \partial_\mu s + 2\lambda u_\mu = 0. \tag{5}
  $$
- From $\delta s$:  
  $$
  -nT - \partial_\mu (\psi u^\mu) = 0 \quad \Rightarrow \quad \partial_\mu (\psi u^\mu) = -nT. \tag{6}
  $$

Contract (5) with $u^\mu$ and use (3) and (4):  
$$
2\lambda u_\mu u^\mu = -2\lambda = n u^\mu \partial_\mu \phi - \psi u^\mu \partial_\mu s = -n\mu \quad \Rightarrow \quad \lambda = \frac{n\mu}{2}.
$$  
Substituting back into (5) yields  
$$
n \partial_\mu \phi = \psi \partial_\mu s + n\mu u_\mu. \tag{7}
$$

### Energy-Momentum Tensor
The perfect-fluid energy-momentum tensor is  
$$
T^{\mu\nu} = (\rho + p) u^\mu u^\nu + p \eta^{\mu\nu} = n\mu u^\mu u^\nu + p \eta^{\mu\nu}.
$$  
We aim to show that $\partial_\mu T^{\mu\nu} = 0$ follows from (1)–(7). Compute the divergence:  
$$
\partial_\mu T^{\mu\nu} = \partial_\mu (n\mu u^\mu u^\nu) + \partial^\nu p.
$$  
Using $\partial_\mu (n u^\mu)=0$ from (1),  
$$
\partial_\mu (n\mu u^\mu u^\nu) = n u^\mu \partial_\mu (\mu u^\nu) = n u^\mu (u^\nu \partial_\mu \mu + \mu \partial_\mu u^\nu).
$$  
The pressure gradient is $\partial^\nu p = n \partial^\nu \mu - nT \partial^\nu s$ (from $dp = n d\mu - nT ds$). Hence,  
$$
\partial_\mu T^{\mu\nu} = n u^\mu u^\nu \partial_\mu \mu + n\mu u^\mu \partial_\mu u^\nu + n \partial^\nu \mu - nT \partial^\nu s. \tag{8}
$$

To eliminate $u^\mu \partial_\mu u^\nu$, differentiate (4): $\partial_\nu (u^\mu \partial_\mu \phi) = -\partial_\nu \mu$. Expanding and using (7) leads after some algebra to  
$$
\mu u^\mu \partial_\mu u^\nu = -\partial^\nu \mu - u^\nu u^\mu \partial_\mu \mu - u^\mu \partial_\mu\!\left(\frac{\psi}{n}\right) \partial^\nu s. \tag{9}
$$  
Substitute (9) into (8):  
$$
\partial_\mu T^{\mu\nu} = n u^\mu u^\nu \partial_\mu \mu - n\left(\partial^\nu \mu + u^\nu u^\mu \partial_\mu \mu + u^\mu \partial_\mu\!\left(\frac{\psi}{n}\right) \partial^\nu s\right) + n \partial^\nu \mu - nT \partial^\nu s = -n u^\mu \partial_\mu\!\left(\frac{\psi}{n}\right) \partial^\nu s - nT \partial^\nu s.
$$  
Now use (6) to evaluate $u^\mu \partial_\mu (\psi/n)$. From (6),  
$$
\partial_\mu (\psi u^\mu) = u^\mu \partial_\mu \psi + \psi \partial_\mu u^\mu = -nT.
$$  
Using $\partial_\mu u^\mu = -\frac{1}{n} u^\mu \partial_\mu n$ from (1), we find  
$$
u^\mu \partial_\mu \psi = -nT + \frac{\psi}{n} u^\mu \partial_\mu n.
$$  
Then  
$$
u^\mu \partial_\mu\!\left(\frac{\psi}{n}\right) = \frac{1}{n} u^\mu \partial_\mu \psi - \frac{\psi}{n^2} u^\mu \partial_\mu n = -T.
$$  
Inserting this into the expression for $\partial_\mu T^{\mu\nu}$ gives  
$$
\partial_\mu T^{\mu\nu} = -n(-T) \partial^\nu s - nT \partial^\nu s = 0.
$$  
Thus, $\partial_\mu T^{\mu\nu} = 0$ holds identically.

### Conclusion
The action principle with Lagrange multipliers yields the equations of relativistic fluid dynamics: particle conservation (1), entropy advection (2), and the conservation of the perfect-fluid energy-momentum tensor. The latter is equivalent to the relativistic Euler equations.


--------------------------- -->

Here is a complete, step-by-step derivation of the perfect fluid energy-momentum tensor using an action principle with Lagrange multipliers. This method, developed by Schutz (1970) and later by Brown (1993), is the cleanest way to handle the constraints inherent in a fluid (particle number conservation and the normalization of the 4-velocity).

We will work in units where $c = 1$ and use the metric signature $(-, +, +, +)$.

---

## 1. The Fluid Variables and Constraints

A perfect fluid is characterized by:
- **Particle number density** $n$ (measured in the rest frame).
- **4-velocity** $u^\mu$ satisfying $u^\mu u_\mu = -1$.
- An **equation of state** relating the energy density $\rho$ to $n$ (and possibly entropy $s$, but we consider a barotropic fluid $\rho = \rho(n)$ for simplicity).
- **Particle number conservation**: $\nabla_\mu (n u^\mu) = 0$.

To construct an action, we introduce:
- A **scalar field** $\varphi$ (a "velocity potential") that will be used to enforce particle conservation.
- A **Lagrange multiplier** $\lambda$ to enforce the normalization $u^\mu u_\mu = -1$.

The fundamental variables are:
- The metric $g_{\mu\nu}$ (dynamical).
- The 4-velocity $u^\mu$ (treated as an independent vector field, but subject to constraints).
- The particle number density $n$ (or equivalently, a scalar field whose gradient gives $u^\mu$).
- The scalar field $\varphi$ (the "potential" for the particle current).
- The Lagrange multiplier $\lambda$.

---

## 2. The Action

We start with the matter action:
$$
S_m = \int d^4x \, \sqrt{-g} \, \mathcal{L},
$$
where the Lagrangian density $\mathcal{L}$ is chosen to be the **energy density** $-\rho(n)$ (the minus sign is conventional to ensure positive energy). We then add the constraints via Lagrange multipliers:

<!-- - **Particle number conservation:** We write $n u^\mu$ as the gradient of a scalar field $\varphi$:
  $$
  n u^\mu = \nabla^\mu \varphi.
  $$
  This automatically ensures that the particle current is a gradient, hence irrotational (no vorticity). For a general fluid with vorticity, one needs more potentials (e.g., three scalars), but for simplicity we assume irrotational flow here. The conservation $\nabla_\mu (n u^\mu) = 0$ is then identically satisfied because $\nabla_\mu \nabla^\mu \varphi = 0$ (the d'Alembertian) – but careful: this is not automatically zero; it's the equation of motion for $\varphi$. Actually, we will instead impose the constraint via a separate Lagrange multiplier. A better approach is to introduce a Lagrange multiplier $\mu$ (sometimes called the "chemical potential" in the action formalism) to enforce that $n u^\mu$ is the gradient of $\varphi$. However, the standard Schutz method uses the following:

We introduce a **scalar field** $\varphi$ and a **Lagrange multiplier** $J^\mu$ (a vector density) to enforce that $J^\mu$ is the particle current. But that's getting messy. Instead, I'll present the cleanest version from Brown (1993), which uses a **Lagrange multiplier** $\mu$ to enforce the relation between $u^\mu$ and the gradient of $\varphi$.

The action is:
$$
S_m = \int d^4x \, \sqrt{-g} \left[ -\rho(n) + \mu \left( \nabla_\mu \varphi \, u^\mu + 1 \right) + \lambda \left( u^\mu u_\mu + 1 \right) \right].
$$
Wait – that's not right. Let's do it systematically.

---

### 2.1 Correct Action (Schutz formalism for irrotational flow)

For an irrotational fluid, we can represent the 4-velocity as:
$$
u_\mu = \frac{\nabla_\mu \varphi}{\sqrt{-\nabla^\alpha \varphi \nabla_\alpha \varphi}}.
$$
This automatically satisfies $u^\mu u_\mu = -1$. Then the particle number density is given by $n = n(\varphi)$ from the equation of state? No, we need to introduce $n$ independently.

A better approach is to use the **velocity potential** $\varphi$ and a **Lagrange multiplier** $\alpha$ to enforce that the particle current is proportional to $\nabla^\mu \varphi$. The action is:
$$
S_m = \int d^4x \, \sqrt{-g} \left[ -\rho(n) + \alpha \left( n u^\mu \nabla_\mu \varphi + 1 \right) + \lambda \left( u^\mu u_\mu + 1 \right) \right].
$$
But the "+1" terms are arbitrary constants to ensure correct equations.

Actually, the standard form (see Hawking & Ellis, or the paper by Brown) is:
$$
S_m = \int d^4x \, \sqrt{-g} \left[ -\rho(n) + J^\mu \left( \nabla_\mu \varphi + \theta \nabla_\mu s \right) + \lambda \left( u^\mu u_\mu + 1 \right) + \beta \left( n \sqrt{-g} - \sqrt{-J_\mu J^\mu} \right) \right],
$$
where $J^\mu$ is the particle number current density (a vector density), $s$ is entropy, and $\theta$ and $\beta$ are Lagrange multipliers. This is too complex for a brief derivation.

I'll present a **simplified but complete** version that captures the essence and yields the correct $T^{\mu\nu}$.

--- -->

## 3. Simplified Action with Lagrange Multipliers

We treat $u^\mu$ and $n$ as independent fields, with constraints:
1. **Normalization:** $u^\mu u_\mu = -1$.
2. **Particle conservation:** $\nabla_\mu (n u^\mu) = 0$.

We introduce Lagrange multipliers:
- $\lambda(x)$ for the normalization constraint.
- $\mu(x)$ for the conservation constraint (but conservation is a differential constraint, so we integrate by parts).

The action is:
$$
S_m = \int d^4x \, \sqrt{-g} \left[ -\rho(n) + \lambda (u^\mu u_\mu + 1) + \mu \nabla_\mu (n u^\mu) \right].
$$
The last term is a total derivative if we integrate by parts, but we will keep it as is for now.

Integrate the last term by parts to move the derivative onto $\mu$:
$$
\int d^4x \, \sqrt{-g} \, \mu \nabla_\mu (n u^\mu) = \int d^4x \, \partial_\mu \left( \sqrt{-g} \, \mu n u^\mu \right) - \int d^4x \, \sqrt{-g} \, n u^\mu \nabla_\mu \mu.
$$
The first term is a boundary term and can be discarded if we assume $\mu$ vanishes at the boundary. Thus:
$$
S_m = \int d^4x \, \sqrt{-g} \left[ -\rho(n) + \lambda (u^\mu u_\mu + 1) - n u^\mu \nabla_\mu \mu \right].
$$

Now our independent variables are:
- The metric $g_{\mu\nu}$.
- The 4-velocity $u^\mu$.
- The particle density $n$.
- The Lagrange multiplier $\lambda$.
- The scalar field $\mu$ (which will turn out to be the **chemical potential**).

---

## 4. Equations of Motion

We vary the action with respect to each variable.

### 4.1 Variation with respect to $\lambda$
$$
\frac{\delta S_m}{\delta \lambda} = 0 \quad \Rightarrow \quad u^\mu u_\mu + 1 = 0,
$$
which enforces the normalization.

### 4.2 Variation with respect to $\mu$
$$
\frac{\delta S_m}{\delta \mu} = 0 \quad \Rightarrow \quad \nabla_\mu (n u^\mu) = 0,
$$
which is the particle conservation equation. (We get this from the original form before integration by parts; our integrated form gives a different equation? Let's be careful: We integrated by parts, so varying $\mu$ in the integrated action gives:
$$
\delta S_m = \int d^4x \, \sqrt{-g} \left[ - n u^\mu \nabla_\mu (\delta \mu) \right] = \int d^4x \, \sqrt{-g} \, \nabla_\mu (n u^\mu) \delta \mu - \text{boundary terms}.
$$
Thus $\nabla_\mu (n u^\mu) = 0$. Good.)

### 4.3 Variation with respect to $n$
$$
\frac{\delta S_m}{\delta n} = 0 \quad \Rightarrow \quad -\rho'(n) - u^\mu \nabla_\mu \mu = 0.
$$
So:
$$
u^\mu \nabla_\mu \mu = -\rho'(n).
$$

### 4.4 Variation with respect to $u^\mu$
$$
\frac{\delta S_m}{\delta u^\mu} = 0 \quad \Rightarrow \quad 2\lambda u_\mu - n \nabla_\mu \mu = 0.
$$
Thus:
$$
\lambda u_\mu = \frac{n}{2} \nabla_\mu \mu.
$$

### 4.5 Interpretation of $\mu$
From the $u^\mu$ equation, we see that $\nabla_\mu \mu$ is proportional to $u_\mu$, meaning $\mu$ is constant along fluid worldlines. In fact, $\mu$ is the **chemical potential** (per particle). From thermodynamics, for a barotropic fluid, the chemical potential $\mu_{\text{chem}}$ satisfies $\mu_{\text{chem}} = (\rho + p)/n$. We will confirm this later.

From the $n$ equation: $u^\mu \nabla_\mu \mu = -\rho'(n)$. But using the thermodynamic relation $\rho'(n) = (\rho + p)/n$, we get:
$$
u^\mu \nabla_\mu \mu = -\frac{\rho + p}{n}.
$$
Since $\mu$ is constant along flow lines (from the $u^\mu$ equation, $\nabla_\mu \mu = (2\lambda / n) u_\mu$), we have $u^\mu \nabla_\mu \mu = -2\lambda / n$ (because $u^\mu u_\mu = -1$, careful with signs). Let's solve for $\lambda$.

From the $u^\mu$ equation: $\nabla_\mu \mu = \frac{2\lambda}{n} u_\mu$. Then:
$$
u^\mu \nabla_\mu \mu = \frac{2\lambda}{n} u^\mu u_\mu = \frac{2\lambda}{n} (-1) = -\frac{2\lambda}{n}.
$$
But from the $n$ equation, $u^\mu \nabla_\mu \mu = -\rho'(n) = -\frac{\rho + p}{n}$. Equating:
$$
-\frac{2\lambda}{n} = -\frac{\rho + p}{n} \quad \Rightarrow \quad \lambda = \frac{\rho + p}{2}.
$$
Thus:
$$
\nabla_\mu \mu = \frac{\rho + p}{n} u_\mu.
$$
This shows that the chemical potential $\mu$ (our Lagrange multiplier) satisfies $d\mu = \frac{\rho + p}{n} u_\mu dx^\mu$, consistent with thermodynamics.

---

## 5. Variation with Respect to the Metric – Obtaining $T^{\mu\nu}$

Now we vary the action with respect to $g^{\mu\nu}$ (or $g_{\mu\nu}$). Recall the action after integration by parts:
$$
S_m = \int d^4x \, \sqrt{-g} \left[ -\rho(n) + \lambda (u^\mu u_\mu + 1) - n u^\mu \nabla_\mu \mu \right].
$$

We treat $u^\mu$ and $n$ as independent of the metric? No, they are not – they have geometric meaning. But when varying the metric, we must consider how $\sqrt{-g}$, $u^\mu$, and covariant derivatives depend on $g^{\mu\nu}$. However, in the action, $u^\mu$ is an independent field, so we do not vary it when varying the metric – we treat it as fixed. Similarly, $n$ and $\mu$ are scalar fields independent of the metric. The only explicit metric dependence is in:
- $\sqrt{-g}$
- The contraction $u^\mu u_\mu = g_{\mu\nu} u^\mu u^\nu$
- The term $\nabla_\mu \mu$ – but this is just $\partial_\mu \mu$, independent of the metric, because the covariant derivative of a scalar is just the partial derivative. So no metric dependence there.

Thus, for the purpose of metric variation, we can write:
$$
S_m = \int d^4x \, \sqrt{-g} \left[ -\rho(n) + \lambda (g_{\mu\nu} u^\mu u^\nu + 1) - n u^\mu \partial_\mu \mu \right].
$$

Now compute $\delta S_m$ with respect to $g^{\mu\nu}$ (or $g_{\mu\nu}$). We'll use $g_{\mu\nu}$ for clarity. Recall:
$$
\delta \sqrt{-g} = \frac12 \sqrt{-g} \, g^{\mu\nu} \delta g_{\mu\nu}.
$$
Also, $g_{\mu\nu} u^\mu u^\nu$ varies as $\delta (g_{\mu\nu} u^\mu u^\nu) = u^\mu u^\nu \delta g_{\mu\nu}$.

Thus:
$$
\delta S_m = \int d^4x \left[ \delta \sqrt{-g} \left( -\rho + \lambda (g_{\alpha\beta} u^\alpha u^\beta + 1) - n u^\alpha \partial_\alpha \mu \right) + \sqrt{-g} \, \lambda \, u^\mu u^\nu \delta g_{\mu\nu} \right].
$$

But note that the term in parentheses is the Lagrangian density $\mathcal{L}$. However, when we vary the metric, we also vary the implicit metric in the contraction $g_{\alpha\beta} u^\alpha u^\beta$ inside the $\lambda$ term. So it's easier to write:

$$
\delta S_m = \int d^4x \left[ \delta \sqrt{-g} \, \mathcal{L} + \sqrt{-g} \, \lambda \, u^\mu u^\nu \delta g_{\mu\nu} \right],
$$
where $\mathcal{L} = -\rho + \lambda (g_{\alpha\beta} u^\alpha u^\beta + 1) - n u^\alpha \partial_\alpha \mu$.

But $\mathcal{L}$ itself contains $g_{\alpha\beta} u^\alpha u^\beta$, so we must include that variation. Actually, we already included it in the second term. Let's do it carefully:

$$
\mathcal{L} = -\rho + \lambda (g_{\alpha\beta} u^\alpha u^\beta + 1) - n u^\alpha \partial_\alpha \mu.
$$
The variation of $\mathcal{L}$ with respect to $g_{\mu\nu}$ (keeping $u^\alpha$ fixed) is:
$$
\delta_{g} \mathcal{L} = \lambda u^\alpha u^\beta \delta g_{\alpha\beta}.
$$
Thus:
$$
\delta S_m = \int d^4x \left[ \delta \sqrt{-g} \, \mathcal{L} + \sqrt{-g} \, \delta_{g} \mathcal{L} \right] = \int d^4x \left[ \frac12 \sqrt{-g} g^{\mu\nu} \delta g_{\mu\nu} \, \mathcal{L} + \sqrt{-g} \, \lambda u^\mu u^\nu \delta g_{\mu\nu} \right].
$$

Therefore:
$$
\frac{\delta S_m}{\delta g_{\mu\nu}} = \sqrt{-g} \left( \frac12 g^{\mu\nu} \mathcal{L} + \lambda u^\mu u^\nu \right).
$$

Now the energy-momentum tensor is defined by:
$$
T^{\mu\nu} = \frac{2}{\sqrt{-g}} \frac{\delta S_m}{\delta g_{\mu\nu}}.
$$
So:
$$
T^{\mu\nu} = g^{\mu\nu} \mathcal{L} + 2\lambda u^\mu u^\nu.
$$

---

## 6. Simplifying Using the Equations of Motion

We now use the equations of motion to eliminate $\mathcal{L}$ and $\lambda$.

First, from the $\lambda$ equation (normalization), $g_{\alpha\beta} u^\alpha u^\beta = -1$. So:
$$
\mathcal{L} = -\rho + \lambda (-1 + 1) - n u^\alpha \partial_\alpha \mu = -\rho - n u^\alpha \partial_\alpha \mu.
$$
But from the $u^\mu$ equation, $\partial_\alpha \mu = \frac{2\lambda}{n} u_\alpha$. Thus:
$$
u^\alpha \partial_\alpha \mu = \frac{2\lambda}{n} u^\alpha u_\alpha = \frac{2\lambda}{n} (-1) = -\frac{2\lambda}{n}.
$$
Therefore:
$$
\mathcal{L} = -\rho - n \left( -\frac{2\lambda}{n} \right) = -\rho + 2\lambda.
$$

Now from the $n$ equation and the relation between $\lambda$ and $\rho+p$, we found $\lambda = (\rho + p)/2$. So:
$$
\mathcal{L} = -\rho + 2 \cdot \frac{\rho + p}{2} = -\rho + (\rho + p) = p.
$$
Thus the Lagrangian density $\mathcal{L}$ evaluated on-shell is simply the **pressure** $p$! This is a key result: the on-shell action for a perfect fluid is $S_m = \int d^4x \sqrt{-g} \, p$.

Now plug $\mathcal{L} = p$ and $\lambda = (\rho + p)/2$ into $T^{\mu\nu}$:
$$
T^{\mu\nu} = g^{\mu\nu} p + 2 \cdot \frac{\rho + p}{2} u^\mu u^\nu = p g^{\mu\nu} + (\rho + p) u^\mu u^\nu.
$$

This is the desired perfect fluid energy-momentum tensor.

---

## 7. Summary of the Derivation

1. **Action:** Start with $S_m = \int d^4x \sqrt{-g} [-\rho(n) + \lambda(u^\mu u_\mu + 1) - n u^\mu \nabla_\mu \mu]$, where $\lambda$ and $\mu$ are Lagrange multipliers enforcing normalization and particle conservation.
2. **Vary $u^\mu$:** Get $\lambda u_\mu = \frac{n}{2} \nabla_\mu \mu$.
3. **Vary $n$:** Get $u^\mu \nabla_\mu \mu = -\rho'(n)$.
4. **Combine:** Use thermodynamic relation $\rho'(n) = (\rho + p)/n$ to find $\lambda = (\rho + p)/2$ and $\nabla_\mu \mu = \frac{\rho + p}{n} u_\mu$.
5. **Vary metric:** Obtain $T^{\mu\nu} = g^{\mu\nu} \mathcal{L} + 2\lambda u^\mu u^\nu$.
6. **On-shell:** Show $\mathcal{L} = p$ using the equations of motion.
7. **Result:** $T^{\mu\nu} = (\rho + p) u^\mu u^\nu + p g^{\mu\nu}$.

This derivation explicitly shows how the pressure emerges from the Lagrange multiplier $\mu$ (the chemical potential) and why the on-shell Lagrangian equals $p$. It also confirms that the perfect fluid tensor is the unique result of an action principle consistent with the constraints.

---------------------

Relativistic hydrodynamics is essential for describing cosmic fluids in regimes where velocities approach the speed of light or where gravitational fields are strong—such as in the early universe, during inflation, or in the vicinity of compact objects. Here we derive the basic equations for a perfect fluid in general relativity, focusing on the conservation laws and their interpretation.

---

## 1. Perfect Fluid Energy‑Momentum Tensor

A perfect fluid is characterized by the absence of viscosity and heat conduction. In a local inertial frame, its stress‑energy tensor takes the diagonal form $T^{\mu\nu} = \mathrm{diag}(\rho, p, p, p)$, where $\rho$ is the energy density and $p$ is the isotropic pressure. In a general coordinate system, this is expressed covariantly as:

$$
T^{\mu\nu} = (\rho + p)\, u^\mu u^\nu + p\, g^{\mu\nu},
$$

where:
- $u^\mu$ is the **4‑velocity** of the fluid, satisfying $g_{\mu\nu} u^\mu u^\nu = -1$ (signature $-+++$).
- $\rho$ and $p$ are measured in the **comoving (local rest) frame** of the fluid.
- $g^{\mu\nu}$ is the metric tensor.

The tensor is symmetric and its trace is $T = g_{\mu\nu} T^{\mu\nu} = -\rho + 3p$.

---

## 2. Conservation Equations: $\nabla_\mu T^{\mu\nu} = 0$

In general relativity, the equations of motion follow from the **covariant conservation** of the energy‑momentum tensor:

$$
\nabla_\mu T^{\mu\nu} = 0,
$$

where $\nabla_\mu$ denotes the covariant derivative compatible with the metric. This represents four equations (one for each $\nu$) that govern the dynamics of the fluid.

### 2.1 Projection Along the 4‑Velocity

To extract the energy conservation (continuity) equation, project $\nabla_\mu T^{\mu\nu} = 0$ onto the direction of $u_\nu$:

$$
u_\nu \nabla_\mu T^{\mu\nu} = 0.
$$

Insert the expression for $T^{\mu\nu}$:

$$
u_\nu \nabla_\mu \big[ (\rho + p) u^\mu u^\nu + p g^{\mu\nu} \big] = 0.
$$

Expand using the product rule:

$$
u_\nu \nabla_\mu\big[(\rho + p) u^\mu u^\nu\big] + u_\nu \nabla_\mu (p g^{\mu\nu}) = 0.
$$

For the first term, note that $\nabla_\mu$ acts on the product, and $u_\nu u^\nu = -1$ implies $u_\nu \nabla_\mu u^\nu = 0$ (since $\nabla_\mu (u_\nu u^\nu) = 0$). Using this:

$$
\begin{aligned}
u_\nu \nabla_\mu\big[(\rho + p) u^\mu u^\nu\big] &= \nabla_\mu\big[(\rho + p) u^\mu\big] \underbrace{u_\nu u^\nu}_{-1} + (\rho + p) u^\mu \, u_\nu \nabla_\mu u^\nu \\
&= -\nabla_\mu\big[(\rho + p) u^\mu\big] + (\rho + p) u^\mu \cdot 0 \\
&= -\nabla_\mu\big[(\rho + p) u^\mu\big].
\end{aligned}
$$

The second term:

$$
u_\nu \nabla_\mu (p g^{\mu\nu}) = \nabla_\mu (p \, g^{\mu\nu} u_\nu) - p \, g^{\mu\nu} \nabla_\mu u_\nu.
$$

But $g^{\mu\nu} u_\nu = u^\mu$. Also, $\nabla_\mu u_\nu$ is not necessarily symmetric, but we can use the metric compatibility $\nabla_\mu g^{\alpha\beta}=0$. However, it is simpler to compute directly:

$$
u_\nu \nabla_\mu (p g^{\mu\nu}) = u_\nu g^{\mu\nu} \nabla_\mu p + p \, u_\nu \nabla_\mu g^{\mu\nu}.
$$

Since $\nabla_\mu g^{\mu\nu}=0$ (metric compatibility), the second term vanishes. And $u_\nu g^{\mu\nu} = u^\mu$. Hence:

$$
u_\nu \nabla_\mu (p g^{\mu\nu}) = u^\mu \nabla_\mu p.
$$

Putting both terms together:

$$
-\nabla_\mu\big[(\rho + p) u^\mu\big] + u^\mu \nabla_\mu p = 0.
$$

Rearrange:

$$
\nabla_\mu\big[(\rho + p) u^\mu\big] - u^\mu \nabla_\mu p = 0.
$$

Expand the first divergence:

$$
\nabla_\mu (\rho u^\mu) + \nabla_\mu (p u^\mu) - u^\mu \nabla_\mu p = 0.
$$

But $\nabla_\mu (p u^\mu) = u^\mu \nabla_\mu p + p \nabla_\mu u^\mu$. So:

$$
\nabla_\mu (\rho u^\mu) + u^\mu \nabla_\mu p + p \nabla_\mu u^\mu - u^\mu \nabla_\mu p = 0.
$$

The terms $u^\mu \nabla_\mu p$ cancel, leaving:

$$
\nabla_\mu (\rho u^\mu) + p \nabla_\mu u^\mu = 0.
$$

This is the **relativistic continuity equation** (energy conservation):

$$
\boxed{ \nabla_\mu (\rho u^\mu) + p \nabla_\mu u^\mu = 0 } \quad \text{or} \quad \nabla_\mu (\rho u^\mu) = -p \nabla_\mu u^\mu.
$$

Often it is written using the projection tensor (see below) or in terms of proper time derivative. Let $D \equiv u^\mu \nabla_\mu$ be the **convective derivative** along the fluid worldline. Then $\nabla_\mu u^\mu = \Theta$ is the **expansion scalar**. Also, $\nabla_\mu (\rho u^\mu) = D\rho + \rho \Theta$. Thus the equation becomes:

$$
D\rho + (\rho + p) \Theta = 0.
$$

### 2.2 Projection Orthogonal to the 4‑Velocity

To obtain the relativistic Euler equation (momentum conservation), we project $\nabla_\mu T^{\mu\nu}=0$ onto the hypersurface orthogonal to $u^\nu$. The projection tensor is:

$$
h^{\alpha}_{\ \nu} = g^{\alpha}_{\ \nu} + u^\alpha u_\nu,
$$

which satisfies $h^{\alpha}_{\ \nu} u^\nu = 0$. We apply $h^{\alpha}_{\ \nu}$ to $\nabla_\mu T^{\mu\nu}=0$:

$$
h^{\alpha}_{\ \nu} \nabla_\mu T^{\mu\nu} = 0.
$$

Insert $T^{\mu\nu}$:

$$
h^{\alpha}_{\ \nu} \nabla_\mu \big[ (\rho + p) u^\mu u^\nu + p g^{\mu\nu} \big] = 0.
$$

Expand:

$$
h^{\alpha}_{\ \nu} \nabla_\mu \big[ (\rho + p) u^\mu u^\nu \big] + h^{\alpha}_{\ \nu} \nabla_\mu (p g^{\mu\nu}) = 0.
$$

**First term:** Use the product rule:

$$
h^{\alpha}_{\ \nu} \nabla_\mu \big[ (\rho + p) u^\mu u^\nu \big] = h^{\alpha}_{\ \nu} \left[ \nabla_\mu ((\rho + p) u^\mu) u^\nu + (\rho + p) u^\mu \nabla_\mu u^\nu \right].
$$

Now, $h^{\alpha}_{\ \nu} u^\nu = 0$ by definition, so the first subterm vanishes. We are left with:

$$
h^{\alpha}_{\ \nu} (\rho + p) u^\mu \nabla_\mu u^\nu = (\rho + p) u^\mu \, h^{\alpha}_{\ \nu} \nabla_\mu u^\nu.
$$

Note that $h^{\alpha}_{\ \nu} \nabla_\mu u^\nu$ is the part of the covariant derivative of $u$ orthogonal to $u$. This term will give the acceleration.

**Second term:** Compute $h^{\alpha}_{\ \nu} \nabla_\mu (p g^{\mu\nu})$:

$$
h^{\alpha}_{\ \nu} \nabla_\mu (p g^{\mu\nu}) = h^{\alpha}_{\ \nu} g^{\mu\nu} \nabla_\mu p + p \, h^{\alpha}_{\ \nu} \nabla_\mu g^{\mu\nu}.
$$

The second term vanishes due to metric compatibility. And $h^{\alpha}_{\ \nu} g^{\mu\nu} = h^{\alpha\mu}$. So:

$$
= h^{\alpha\mu} \nabla_\mu p.
$$

Thus the projected equation becomes:

$$
(\rho + p) u^\mu \, h^{\alpha}_{\ \nu} \nabla_\mu u^\nu + h^{\alpha\mu} \nabla_\mu p = 0.
$$

Define the **acceleration** $a^\alpha \equiv u^\mu \nabla_\mu u^\alpha$. Its projection orthogonal to $u$ is $h^{\alpha}_{\ \nu} a^\nu = a^\alpha$ because $a^\alpha$ is orthogonal to $u$ (since $u_\alpha a^\alpha = 0$ from $u_\alpha u^\alpha = -1$). Then the first term becomes $(\rho + p) a^\alpha$. So:

$$
(\rho + p) a^\alpha + h^{\alpha\mu} \nabla_\mu p = 0.
$$

This is the **relativistic Euler equation**:

$$
\boxed{ (\rho + p) \, u^\mu \nabla_\mu u^\alpha = - (g^{\alpha\mu} + u^\alpha u^\mu) \nabla_\mu p } \quad \text{or} \quad (\rho + p) a^\alpha = - h^{\alpha\mu} \nabla_\mu p.
$$

It states that the acceleration of the fluid is driven by pressure gradients orthogonal to the flow.

---

## 3. Interpretation and Special Cases

### 3.1 Non‑Relativistic Limit

In the non‑relativistic limit, $p \ll \rho$, and velocities are small: $u^\mu \approx (1, \vec{v})$ (with $c=1$). The proper time derivative $u^\mu \nabla_\mu \approx \partial_t + \vec{v}\cdot \nabla$ becomes the convective derivative. The acceleration $a^i \approx \partial_t v^i + (\vec{v}\cdot\nabla) v^i + \Gamma^i_{00}$ where $\Gamma^i_{00} \approx \partial_i \phi$ (in a weak field). The Euler equation reduces to the standard form:

$$
\rho \left( \frac{\partial \vec{v}}{\partial t} + (\vec{v}\cdot\nabla)\vec{v} + \nabla\phi \right) = -\nabla p.
$$

### 3.2 Cosmological Background

For a homogeneous and isotropic universe (FLRW metric), the fluid 4‑velocity is $u^\mu = (1,0,0,0)$ in comoving coordinates. The expansion scalar $\Theta = \nabla_\mu u^\mu = 3H$ where $H = \dot{a}/a$. The continuity equation becomes:

$$
\dot{\rho} + 3H (\rho + p) = 0,
$$

which is the familiar energy conservation for a cosmic fluid. The Euler equation is identically satisfied due to homogeneity (no pressure gradients).

### 3.3 Equation of State

To close the system, an **equation of state** relating $p$ and $\rho$ (and possibly entropy) is needed. Common examples in cosmology:
- **Dust** (cold dark matter, baryons after recombination): $p = 0$.
- **Radiation** (photons, relativistic neutrinos): $p = \rho/3$.
- **Vacuum energy** (cosmological constant): $p = -\rho$.
- **Scalar field** (inflation, dark energy): effective $p$ and $\rho$ derived from the field Lagrangian.

---

## 4. Inclusion of Other Forces and Dissipation

The perfect fluid equations can be extended to include:
- **Electromagnetic fields**: additional terms in $T^{\mu\nu}$ and Lorentz force.
- **Viscosity and heat conduction**: described by the Israel–Stewart formalism for relativistic dissipative fluids.
- **Gravitational source**: The fluid equations are coupled to Einstein’s field equations $G_{\mu\nu} = 8\pi G T_{\mu\nu}$ (with $c=1$), making the dynamics fully self‑consistent.

---

## 5. Application to Cosmological Perturbations

In linear perturbation theory around an FLRW background, the relativistic hydrodynamic equations (continuity and Euler) are expanded to first order. They combine with the perturbed Einstein equations to yield the evolution of density and velocity perturbations. For a single fluid with constant equation of state $w = p/\rho$, the perturbation equations reduce to the **relativistic growth equation**:

$$
\ddot{\delta} + (2 + 3c_s^2 - 6w) H \dot{\delta} - \left[ 4\pi G \rho (1 + w)(1 + 3c_s^2) - \frac{c_s^2 k^2}{a^2} \right] \delta = 0,
$$

where $c_s^2 = \partial p / \partial \rho$ is the adiabatic sound speed squared. This governs the growth of structure and acoustic oscillations in the early universe.

---

## 6. Summary

The relativistic hydrodynamics of a perfect fluid is encapsulated in two conservation laws derived from $\nabla_\mu T^{\mu\nu}=0$:

- **Energy conservation**: $\nabla_\mu (\rho u^\mu) + p \nabla_\mu u^\mu = 0$  (or $D\rho + (\rho + p)\Theta = 0$).
- **Euler equation**: $(\rho + p) a^\alpha = - h^{\alpha\mu} \nabla_\mu p$.

These equations, together with an equation of state and Einstein’s equations, form the foundation for studying the dynamics of cosmic fluids from the early universe to the formation of large‑scale structure.




---------------------------
-------------------------

Yes, absolutely. The action principle can be used to derive the classical (non-relativistic) perfect fluid equations, such as the **Euler equation** and the **continuity equation**.

To get the classical case, we usually take the **non-relativistic limit** ($c \to \infty$) of the relativistic action, or we construct an action specifically for Newtonian fluids using **Lagrangian variables** (comoving coordinates) or **Clebsch potentials**.

Here is how you derive the classical perfect fluid equations from an action principle, starting from the relativistic action shown previously and taking the classical limit.

---

### 1. Starting Point: The Relativistic Action
We begin with the relativistic action we just discussed, which is built on the conservation of particle number:
$$
S = \int d^4x \sqrt{-g} \left[ -\rho(n) \right] \quad \text{(with constraints)}
$$
(Note: The sign convention is adjusted to yield positive energy density in the classical limit).

In flat spacetime (Minkowski metric, $\sqrt{-g} = 1$), and using the current $J^a = n u^a$, the action is:
$$
S = \int dt d^3x \left[ -\rho(n) + \lambda (\partial_t n + \partial_i (n v^i)) \right]
$$
where we set $c=1$ for now, and $v^i$ is the 3-velocity.

### 2. Taking the Non-Relativistic Limit
To get classical physics, we must restore $c$ and take $c \rightarrow \infty$.

1.  **Energy Density:** In the non-relativistic limit, the energy density $\rho$ is dominated by the rest mass energy ($mn$) plus the internal energy ($U$):
    $$
    \rho(n) = m n c^2 + U(n)
    $$
    Here, $m$ is the particle mass, and $U(n)$ is the classical internal energy density (which leads to pressure).

2.  **Four-velocity:** The four-velocity components become:
    $$
    u^0 = \frac{1}{\sqrt{1 - v^2/c^2}} \approx 1 + \frac{v^2}{2c^2}, \quad u^i = \frac{v^i}{c\sqrt{1 - v^2/c^2}} \approx \frac{v^i}{c}
    $$

3.  **Action:** Plugging these into the action, we keep terms up to order $c^0$ (i.e., we subtract the huge constant rest mass term, which is akin to subtracting the ground state energy in quantum field theory). The action becomes:
    $$
    S \approx \int dt d^3x \left[ \frac{1}{2} m n v^2 - U(n) + \lambda (\partial_t n + \nabla \cdot (n \mathbf{v})) \right]
    $$
    Here, $\lambda$ now acts as a Lagrange multiplier enforcing the classical continuity equation.

### 3. Variation in the Classical Case
We now treat $n$, $\mathbf{v}$, and $\lambda$ as independent fields in flat spacetime.

#### Variation with respect to $\lambda$:
This immediately yields the **Classical Continuity Equation**:
$$
\partial_t n + \nabla \cdot (n \mathbf{v}) = 0
$$

#### Variation with respect to $n$:
We vary the number density $n$.
$$
\delta_n S = \int dt d^3x \left[ \left( \frac{1}{2} m v^2 - \mu(n) \right) \delta n + \lambda \partial_t (\delta n) + \lambda \nabla \cdot (\delta n \mathbf{v}) \right]
$$
where we define the classical chemical potential $\mu(n) \equiv \frac{dU}{dn}$.
Integrating the $\lambda$ terms by parts (assuming boundary terms vanish) gives:
$$
\delta_n S = \int dt d^3x \left[ \frac{1}{2} m v^2 - \mu(n) - \partial_t \lambda - \mathbf{v} \cdot \nabla \lambda \right] \delta n = 0
$$
Thus, we get the equation:
$$
\partial_t \lambda + \mathbf{v} \cdot \nabla \lambda = \frac{1}{2} m v^2 - \mu(n) \quad \text{(This is Bernoulli's equation in potential form)}
$$

#### Variation with respect to $v^i$:
We vary the velocity field. The relevant terms in the action are $\frac{1}{2} m n v^2$ and the constraint term $\lambda \nabla \cdot (n \mathbf{v})$.
$$
\delta_{\mathbf{v}} S = \int dt d^3x \left[ m n \mathbf{v} \cdot \delta \mathbf{v} - (n \nabla \lambda) \cdot \delta \mathbf{v} \right] = 0
$$
(We got the $-\nabla \lambda$ term by integrating the constraint by parts spatially).
This gives us a direct relation between velocity and the Lagrange multiplier:
$$
m \mathbf{v} = \nabla \lambda
$$
This is the key result: In the classical limit, the gradient of the Lagrange multiplier $\lambda$ is proportional to the velocity field. This implies the flow is **irrotational** ($\nabla \times \mathbf{v} = 0$).

### 4. Recovering the Euler Equation
Now we combine these results to get the standard Euler equation.

1.  From the $v^i$ variation, we have $\mathbf{v} = \frac{1}{m} \nabla \lambda$.
2.  Take the gradient of the equation we got from the $n$ variation:
    $$
    \nabla (\partial_t \lambda) + \nabla (\mathbf{v} \cdot \nabla \lambda) = \nabla \left( \frac{1}{2} m v^2 \right) - \nabla \mu(n)
    $$
3.  Substitute $\nabla \lambda = m \mathbf{v}$:
    $$
    \partial_t (m \mathbf{v}) + \nabla (\mathbf{v} \cdot (m \mathbf{v})) = \nabla \left( \frac{1}{2} m v^2 \right) - \nabla \mu(n)
    $$
4.  Using the vector identity $\nabla (\mathbf{v} \cdot \mathbf{v}) = 2 (\mathbf{v} \cdot \nabla) \mathbf{v} + 2 \mathbf{v} \times (\nabla \times \mathbf{v})$, and noting our flow is irrotational ($\nabla \times \mathbf{v}=0$), we simplify $\nabla (\mathbf{v} \cdot \mathbf{v}) = 2 (\mathbf{v} \cdot \nabla) \mathbf{v}$.
5.  This yields:
    $$
    m (\partial_t \mathbf{v} + (\mathbf{v} \cdot \nabla) \mathbf{v}) = -\nabla \mu(n)
    $$

Finally, we use thermodynamics. The pressure $p$ is related to the internal energy $U$ via the Gibbs relation. For a fluid at zero temperature (or ignoring entropy variations in this simplified model), we have $dp = n d\mu$. Therefore, $\nabla \mu = \frac{1}{n} \nabla p$.

Substituting this in gives the **Classical Euler Equation** for an irrotational, barotropic fluid:
$$
\boxed{ \partial_t \mathbf{v} + (\mathbf{v} \cdot \nabla) \mathbf{v} = -\frac{1}{mn} \nabla p }
$$

### Summary
To derive the classical perfect fluid equations from an action:

1.  **Start** with the relativistic action for a barotropic fluid.
2.  **Expand** in powers of $1/c$, separating the rest mass energy from the internal energy.
3.  **Vary** the resulting classical action with respect to density $n$, velocity $\mathbf{v}$, and the Lagrange multiplier $\lambda$.
4.  **Result:** You obtain the continuity equation, and the Euler equation (specifically for potential flow).

**Note on Vorticity:** This specific derivation yields irrotational flow ($\nabla \times \mathbf{v}=0$). To derive the equations for general rotational flow from an action, you need to introduce additional fields (usually **Clebsch potentials**) to represent the velocity degrees of freedom. However, the physical equations (Euler + Continuity) remain the same.

Excellent question. You've picked up on a crucial point in the mathematical structure of fluids.

In our earlier derivation using the Lagrange multiplier $\lambda$, we ended up with the condition $m\mathbf{v} = \nabla \lambda$. This forces the flow to be **irrotational** ($\nabla \times \mathbf{v} = 0$). But what if we want to describe a fluid with **vorticity** (like a tornado, or a stirring cup of coffee)?

This is where **Clebsch potentials** come in. They are a mathematical way to represent a general velocity field (which has 3 components) using a set of scalar fields.

### 1. The Problem: Degrees of Freedom
- The velocity field $\mathbf{v}(\mathbf{x}, t)$ has **3 components** (at every point in space).
- In our action, we varied $\lambda$, which gave us one equation, and $\mathbf{v}$, which gave us one vector equation. That was fine mathematically, but the result ($\mathbf{v} = \nabla \lambda$) was too restrictive.
- To represent a general flow with vorticity ($\nabla \times \mathbf{v} \neq 0$), we need more scalar fields in our action.

### 2. The Clebsch Representation
In the 19th century, Alfred Clebsch showed that any vector field (in 3D) can be represented (at least locally) as:
$$ \mathbf{v} = \nabla \phi + \alpha \nabla \beta $$
where $\phi$, $\alpha$, and $\beta$ are scalar fields.

Let's check the vorticity (curl) of this:
$$ \nabla \times \mathbf{v} = \nabla \times (\nabla \phi) + \nabla \times (\alpha \nabla \beta) $$
The first term is zero (curl of gradient). Using a vector identity, the second term becomes:
$$ \nabla \times (\alpha \nabla \beta) = \nabla \alpha \times \nabla \beta $$
So, the vorticity is:
$$ \boldsymbol{\omega} = \nabla \times \mathbf{v} = \nabla \alpha \times \nabla \beta $$

**Key Insight:** As long as the gradients of $\alpha$ and $\beta$ are not parallel, you get non-zero vorticity. The "amount" of vorticity is encoded in the spatial variation of these two new fields.

### 3. The Action with Clebsch Potentials
Now, let's build an action for a perfect fluid using these potentials. We'll work in the non-relativistic limit for clarity. We have three dynamical fields: $\phi$, $\alpha$, and $\beta$.

We also need to enforce mass conservation. The mass density is $\rho = m n$, and the current is $\mathbf{J} = \rho \mathbf{v}$.

We write the action as:
$$ S = \int dt d^3x \left[ \frac{1}{2} \rho v^2 - U(\rho) + \phi \left( \partial_t \rho + \nabla \cdot (\rho \mathbf{v}) \right) + \alpha \left( \partial_t \beta + \mathbf{v} \cdot \nabla \beta \right) \right] $$
where $\mathbf{v} = \nabla \phi + \alpha \nabla \beta$.

Let's break down the terms:
1.  **$\frac{1}{2} \rho v^2 - U(\rho)$:** The kinetic minus internal energy density (the Lagrangian).
2.  **$\phi \left( \partial_t \rho + \nabla \cdot (\rho \mathbf{v}) \right)$:** This enforces mass conservation. $\phi$ is a Lagrange multiplier (like our old $\lambda$), but it now also contributes to the velocity.
3.  **$\alpha \left( \partial_t \beta + \mathbf{v} \cdot \nabla \beta \right)$:** This is the new term. It enforces that $\beta$ is **advected** with the flow (its value is constant along a fluid element's path). $\alpha$ is a Lagrange multiplier enforcing this, and it becomes the other Clebsch potential.

### 4. Varying the Action
Let's see what equations we get. We vary with respect to $\rho$, $\phi$, $\alpha$, and $\beta$.

- **Variation w.r.t. $\phi$:** This gives back the continuity equation:
    $$ \partial_t \rho + \nabla \cdot (\rho \mathbf{v}) = 0 $$

- **Variation w.r.t. $\alpha$:** This gives the advection equation for $\beta$:
    $$ \partial_t \beta + \mathbf{v} \cdot \nabla \beta = 0 $$
    This means $\beta$ is a label that moves with the fluid.

- **Variation w.r.t. $\beta$:** This gives an equation for $\alpha$:
    $$ \partial_t \alpha + \nabla \cdot (\alpha \mathbf{v}) = 0 $$
    (This comes from integrating by parts in time and space). This is a conservation equation for $\alpha$.

- **Variation w.r.t. $\rho$:** This gives a Bernoulli-like equation (similar to before):
    $$ \partial_t \phi + \frac{1}{2} v^2 + \mu(\rho) + \alpha \partial_t \beta + \alpha \mathbf{v} \cdot \nabla \beta = 0 $$
    Using the advection equation for $\beta$, $\partial_t \beta = -\mathbf{v} \cdot \nabla \beta$, the last two terms cancel! So we get:
    $$ \partial_t \phi + \frac{1}{2} v^2 + \mu(\rho) = 0 $$
    This is exactly the Bernoulli equation we had before, but now $\phi$ is just one part of the velocity.

### 5. Recovering the Euler Equation (with Vorticity!)
Now, we take the gradient of the Bernoulli equation:
$$ \nabla (\partial_t \phi) + \nabla \left( \frac{1}{2} v^2 \right) + \nabla \mu = 0 $$
We want to express this in terms of $\mathbf{v} = \nabla \phi + \alpha \nabla \beta$.

First, compute the material derivative of $\mathbf{v}$:
$$ \frac{D\mathbf{v}}{Dt} = \partial_t \mathbf{v} + (\mathbf{v} \cdot \nabla) \mathbf{v} $$
We can use the vector identity: $(\mathbf{v} \cdot \nabla) \mathbf{v} = \nabla (\frac{1}{2} v^2) - \mathbf{v} \times \boldsymbol{\omega}$.

Now, compute $\partial_t \mathbf{v}$ using the Clebsch representation:
$$ \partial_t \mathbf{v} = \partial_t (\nabla \phi) + (\partial_t \alpha) \nabla \beta + \alpha \nabla (\partial_t \beta) $$
Using the equations we derived ($\partial_t \beta = -\mathbf{v} \cdot \nabla \beta$ and the equation for $\partial_t \alpha$), and after some vector calculus (which is a bit lengthy), you can show that:
$$ \partial_t \mathbf{v} + (\mathbf{v} \cdot \nabla) \mathbf{v} = -\nabla \left( \partial_t \phi + \frac{1}{2} v^2 \right) $$
Substituting this into the gradient of the Bernoulli equation ($\nabla (\partial_t \phi + \frac{1}{2} v^2) = -\nabla \mu$) gives:
$$ \partial_t \mathbf{v} + (\mathbf{v} \cdot \nabla) \mathbf{v} = -\nabla \mu $$
And since $\nabla \mu = \frac{1}{\rho} \nabla p$, we finally get:
$$ \rho \left( \partial_t \mathbf{v} + (\mathbf{v} \cdot \nabla) \mathbf{v} \right) = -\nabla p $$

**This is the Euler equation, valid for flows with vorticity!**

### 6. What's the Physical Meaning of $\alpha$ and $\beta$?
These fields have a beautiful physical interpretation:
- **$\beta$:** This is a **material label**. It is constant along a fluid worldline ($D\beta/Dt = 0$). It could represent, for example, the initial position of a fluid element in one direction.
- **$\alpha$:** This is also advected with the flow ($D\alpha/Dt = 0$ from its conservation equation). It is another material label.

The vorticity is $\boldsymbol{\omega} = \nabla \alpha \times \nabla \beta$. This means that **vorticity lines are the intersections of surfaces of constant $\alpha$ and constant $\beta$**. This is a fundamental result in fluid dynamics: vortex lines are "frozen" into the fluid and are the intersections of two material surfaces.

### Summary
- **Without Clebsch ($\mathbf{v} = \nabla \lambda$):** Action yields $\nabla \times \mathbf{v} = 0$. (Irrotational flow).
- **With Clebsch ($\mathbf{v} = \nabla \phi + \alpha \nabla \beta$):** Action yields $\nabla \times \mathbf{v} = \nabla \alpha \times \nabla \beta$. (General flow with vorticity).

The Clebsch potentials allow the action principle to describe **any** perfect fluid flow by introducing additional scalar fields that track the frozen-in vortex lines. This is the standard way to derive the full Euler equation from a variational principle.

---

**In the relativistic 4D formalism** (special or general relativity, applied to cosmological hydrodynamics in a 4-dimensional spacetime), viscosity is added by **modifying the energy-momentum tensor** $T^{\mu\nu}$ with dissipative terms. The perfect-fluid part is replaced by a viscous version, and the equations of motion follow from the covariant conservation law

$$
\nabla_\mu T^{\mu\nu} = 0
$$

(together with Einstein’s equations $G^{\mu\nu} = 8\pi T^{\mu\nu}$ if full GR is used, or particle-number conservation $\nabla_\mu (n u^\mu) = 0$).

The general viscous energy-momentum tensor (Landau frame, first-order formulation) reads

$$
T^{\mu\nu} = (\epsilon + p) u^\mu u^\nu + p\, g^{\mu\nu} + \pi^{\mu\nu},
$$

where $\epsilon$ is the energy density, $p$ the equilibrium pressure, $u^\mu$ the four-velocity ($u^\mu u_\mu = -1$), and $g^{\mu\nu}$ the metric. The viscous (dissipative) part $\pi^{\mu\nu}$ (orthogonal to $u^\mu$, traceless for shear) is

$$
\pi^{\mu\nu} = -2\eta\,\sigma^{\mu\nu} - \zeta\,\theta\,\Delta^{\mu\nu}.
$$

Here:
- $\eta$ = shear viscosity,
- $\zeta$ = bulk viscosity,
- $\Delta^{\mu\nu} = g^{\mu\nu} + u^\mu u^\nu$ (projector),
- $\theta = \nabla_\alpha u^\alpha$ (expansion scalar),
- $\sigma^{\mu\nu} = \Delta^{\mu\alpha}\Delta^{\nu\beta}\nabla_{(\alpha} u_{\beta)} - \frac13\Delta^{\mu\nu}\theta$ (shear tensor).

**This is the direct relativistic analogue of the non-relativistic viscous stress tensor** $\boldsymbol{\sigma}$ you had in the Navier-Stokes equations. In the first-order theories that are causal and stable in 4D (e.g., Lichnerowicz-type or modern BDNK formulations), the viscous corrections can also appear as out-of-equilibrium contributions $A$ and $\Pi$ to the effective energy density and pressure:

$$
T^{\mu\nu} = (\rho + A) u^\mu u^\nu + (P + \Pi) \Delta^{\mu\nu} + \pi^{\mu\nu} + \dots
$$

with transport coefficients $\chi_i$ (functions of $\rho$) that encode $\zeta$ and $\eta$.

The conservation $\nabla_\mu T^{\mu\nu} = 0$ automatically gives the relativistic Euler and continuity equations with viscous heating/dissipation. Projecting parallel and orthogonal to $u^\mu$ yields the energy and momentum equations (exactly analogous to the non-relativistic $\rho(\partial_t + \mathbf{v}\cdot\nabla)\mathbf{v} = -\nabla p + \nabla\cdot\boldsymbol{\sigma}$).

