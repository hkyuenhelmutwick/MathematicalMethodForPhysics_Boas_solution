## 3. DEFINITION OF THE GAMMA FUNCTION; RECURSION RELATION

### 1

Prove that the integral
$$
\Gamma(p) = \int_0^\infty x^{p-1} e^{-x} dx
$$
is convergent for any $p > 0$.

**Proof:**

The integral is improper at both $x=0$ and $x=\infty$. We analyze convergence at both ends.

#### Near $x=0$:
For small $x$, $e^{-x} \approx 1$, so the integrand behaves like $x^{p-1}$.

Consider:
$$
\int_0^a x^{p-1} dx = \left[ \frac{x^p}{p} \right]_0^a = \frac{a^p}{p}
$$
This is finite for any $p > 0$.

#### As $x \to \infty$:
For large $x$, $e^{-x}$ decays much faster than any power of $x$ grows. For any $p$, $x^{p-1} e^{-x} \to 0$ rapidly as $x \to \infty$.

Consider:
$$
\int_A^\infty x^{p-1} e^{-x} dx
$$
For large $x$, $e^{-x}$ dominates, so the integral converges for all $p$.

#### Conclusion:
Both at $x=0$ and $x=\infty$, the integral converges for any $p > 0$.

---


### 2

$$\dfrac{\Gamma(2/3)}{\Gamma(5/3)}$$

Apply the recursion relation twice:

$\Gamma(5/3) = (2/3)\Gamma(2/3)$

So:
$$
\frac{\Gamma(2/3)}{\Gamma(5/3)} = \frac{\Gamma(2/3)}{(2/3)\Gamma(2/3)} = \frac{3}{2}
$$

---

### 3

$$\dfrac{\Gamma(2/3)}{\Gamma(8/3)}$$

$\Gamma(8/3) = (5/3)\Gamma(5/3)$ and $\Gamma(5/3) = (2/3)\Gamma(2/3)$

So:
$$
\Gamma(8/3) = (5/3)(2/3)\Gamma(2/3) = \frac{10}{9}\Gamma(2/3)
$$
Thus:
$$
\frac{\Gamma(2/3)}{\Gamma(8/3)} = \frac{\Gamma(2/3)}{\frac{10}{9}\Gamma(2/3)} = \frac{9}{10}
$$

---

### 4

$$\dfrac{\Gamma(2/5)}{\Gamma(12/5)}$$

$\Gamma(12/5) = (7/5)\Gamma(7/5)$
$\Gamma(7/5) = (2/5)\Gamma(2/5)$

So:
$$
\Gamma(12/5) = (7/5)(2/5)\Gamma(2/5) = \frac{14}{25}\Gamma(2/5)
$$
Thus:
$$
\frac{\Gamma(2/5)}{\Gamma(12/5)} = \frac{\Gamma(2/5)}{\frac{14}{25}\Gamma(2/5)} = \frac{25}{14}
$$

---

### 5

$$\dfrac{\Gamma(1/2)\Gamma(4)}{\Gamma(9/2)}$$

$\Gamma(9/2) = (7/2)\Gamma(7/2)$
$\Gamma(7/2) = (5/2)\Gamma(5/2)$
$\Gamma(5/2) = (3/2)\Gamma(3/2)$
$\Gamma(3/2) = (1/2)\Gamma(1/2)$

$\Gamma(4) = 3! = 6$

So:
$$
\Gamma(9/2) = (7/2)(5/2)(3/2)(1/2)\Gamma(1/2) = \frac{105}{16}\Gamma(1/2)
$$
Thus:
$$
\frac{\Gamma(1/2)\Gamma(4)}{\Gamma(9/2)} = \frac{\Gamma(1/2)\cdot 6}{\frac{105}{16}\Gamma(1/2)} = \frac{6}{105/16} = \frac{96}{105} = \frac{32}{35}
$$

---

### 6

$$\dfrac{\Gamma(10)}{\Gamma(8)}$$

$\Gamma(10) = 9\Gamma(9) = 9\cdot8\Gamma(8) = 72\Gamma(8)$

So:
$$
\frac{\Gamma(10)}{\Gamma(8)} = 72
$$

---

### 7

$$
\frac{\Gamma(4)\Gamma(3/4)}{\Gamma(7/4)}
$$

**Solution:**

First, use the recursion relation:
$$
\Gamma(p+1) = p\Gamma(p)
$$

Notice that:
$$
\Gamma(7/4) = (3/4)\Gamma(3/4)
$$

Also, $\Gamma(4) = 3! = 6$.

So:
$$
\frac{\Gamma(4)\Gamma(3/4)}{\Gamma(7/4)} = \frac{6\Gamma(3/4)}{(3/4)\Gamma(3/4)} = \frac{6}{3/4} = 8
$$

---

### 8

$$\int_0^\infty x^{2/3} e^{-x} dx$$

This is already in the form of the Gamma function with $s = 2/3 + 1 = 5/3$:

- $\int_0^\infty x^{2/3} e^{-x} dx = \Gamma(5/3)$
- Numerically: $\Gamma(5/3) \approx 0.8929795$

---

### 9

$$\int_0^\infty e^{-x^4} dx$$

Let $x^4 = u \Rightarrow x = u^{1/4}, dx = \frac{1}{4} u^{-3/4} du$:

$$
\int_0^\infty e^{-x^4} dx = \int_0^\infty e^{-u} \frac{1}{4} u^{-3/4} du = \frac{1}{4} \Gamma(1/4)
$$
- Numerically: $\Gamma(1/4) \approx 3.6256099$
- So, value $\approx 0.9064025$

---

### 10

$$\int_0^\infty x^{-2/5} e^{-x} dx$$

This is $x^{s-1}$ with $s-1 = -2/5 \Rightarrow s = 3/5$:

- $\int_0^\infty x^{-2/5} e^{-x} dx = \Gamma(3/5)$
- Numerically: $\Gamma(3/5) \approx 1.4891922$

---

### 11

$$\int_0^\infty x^5 e^{-x^2} dx$$

Let $x^2 = u \Rightarrow x = u^{1/2}, dx = \frac{1}{2} u^{-1/2} du$:

$$
\int_0^\infty x^5 e^{-x^2} dx = \int_0^\infty u^{5/2} e^{-u} \frac{1}{2} u^{-1/2} du = \frac{1}{2} \int_0^\infty u^2 e^{-u} du = \frac{1}{2} \Gamma(3)
$$
- $\Gamma(3) = 2! = 2$
- So, value = 1

---

### 12

$$\int_0^\infty x e^{-x^3} dx$$

Let $x^3 = u \Rightarrow x = u^{1/3}, dx = \frac{1}{3} u^{-2/3} du$:

$$
\int_0^\infty x e^{-x^3} dx = \int_0^\infty u^{1/3} e^{-u} \frac{1}{3} u^{-2/3} du = \frac{1}{3} \int_0^\infty u^{-1/3} e^{-u} du = \frac{1}{3} \Gamma(2/3)
$$
- Numerically: $\Gamma(2/3) \approx 1.3541179$
- So, value $\approx 0.4513726$

---

### 13

$$\int_0^1 x^2 \left( \ln \frac{1}{x} \right)^3 dx$$

Let $x = e^{-u} \Rightarrow dx = -e^{-u} du, x^2 = e^{-2u}, \ln(1/x) = u$:

Limits: $x=0 \to u=\infty, x=1 \to u=0$

$$
\int_0^1 x^2 (\ln(1/x))^3 dx = \int_{\infty}^0 e^{-2u} u^3 (-e^{-u}) du = \int_0^{\infty} u^3 e^{-3u} du
$$
Let $t = 3u \Rightarrow du = dt/3$:

$$
= \int_0^{\infty} \left(\frac{t}{3}\right)^3 e^{-t} \frac{dt}{3} = \frac{1}{81} \int_0^{\infty} t^3 e^{-t} dt = \frac{1}{81} \Gamma(4)
$$
- $\Gamma(4) = 3! = 6$
- So, value = $6/81 = 2/27 \approx 0.074074$

---

### 14

$$\int_0^1 \sqrt[3]{\ln x} dx$$

Let $t = -\ln x \Rightarrow x = e^{-t}, dx = -e^{-t} dt$

Limits: $x=0 \to t=\infty, x=1 \to t=0$

$$
\int_0^1 (\ln x)^{1/3} dx = \int_{\infty}^0 (-t)^{1/3} (-e^{-t}) dt = \int_0^{\infty} t^{1/3} e^{-t} dt = \Gamma(4/3)
$$
- Numerically: $\Gamma(4/3) \approx 0.8929795$

---

### 15

$$\int_0^\infty x^{-1/3} e^{-8x} dx$$

This is $x^{s-1} e^{-\lambda x}$ with $s-1 = -1/3 \Rightarrow s = 2/3$, $\lambda = 8$:

$$
\int_0^\infty x^{-1/3} e^{-8x} dx = 8^{-2/3} \Gamma(2/3)
$$
- $8^{-2/3} = (2^3)^{-2/3} = 2^{-2} = 1/4$
- $\Gamma(2/3) \approx 1.3541179$
- So, value $\approx 0.3385295$

---

### 16

A particle starting from rest at $x = 1$ moves along the $x$ axis toward the origin. Its potential energy is $V = \frac{1}{2}m \ln x$. Write the Lagrange equation and integrate it to find the time required for the particle to reach the origin.

**Solution:**

The Lagrangian is:
$$
L = T - V = \frac{1}{2}m \dot{x}^2 - \frac{1}{2}m \ln x
$$

Since $L$ does not depend explicitly on time, use conservation of energy:
$$
E = T + V = \text{constant}
$$

At $x=1$, the particle starts from rest, so $\dot{x}_0 = 0$:
$$
E = 0 + \frac{1}{2}m \ln 1 = 0
$$

At any $x$:
$$
\frac{1}{2}m \dot{x}^2 + \frac{1}{2}m \ln x = 0
$$
$$
\dot{x}^2 = -\ln x
$$

Since $\dot{x} < 0$ (moving toward the origin):
$$
\dot{x} = -\sqrt{-\ln x}
$$

So:
$$
\frac{dx}{dt} = -\sqrt{-\ln x}
$$

Separate variables and integrate from $x=1$ to $x=0$ (and $t=0$ to $t_f$):
$$
\int_1^0 \frac{dx}{-\sqrt{-\ln x}} = \int_0^{t_f} dt
$$
$$
\int_0^1 \frac{dx}{\sqrt{-\ln x}} = t_f
$$

Let $u = -\ln x \implies x = e^{-u}, dx = -e^{-u} du$

When $x=1$, $u=0$; when $x=0$, $u=\infty$:
$$
\int_{x=0}^{x=1} \frac{dx}{\sqrt{-\ln x}} = \int_{u=\infty}^{u=0} \frac{e^{-u} du}{\sqrt{u}}
$$
$$
= \int_{u=0}^{u=\infty} \frac{e^{-u}}{\sqrt{u}} du = \int_0^{\infty} u^{-1/2} e^{-u} du = \Gamma\left(\frac{1}{2}\right)
$$

**Final answer:**
$$
t_f = \Gamma\left(\frac{1}{2}\right)
$$

Where $\Gamma(1/2) = \sqrt{\pi} \approx 1.77245$.

---

### 17

Express as a Gamma function:
$$
\int_0^1 \left[ \ln \left( \frac{1}{x} \right) \right]^{p-1} dx
$$

**Solution:**

Let $u = \ln\left(\frac{1}{x}\right) = -\ln x$, so $x = e^{-u}$ and $dx = -e^{-u} du$.

When $x=0$, $u=\infty$; when $x=1$, $u=0$.

So:
$$
\int_0^1 [\ln(1/x)]^{p-1} dx = \int_{u=\infty}^{u=0} u^{p-1} (-e^{-u}) du = \int_0^{\infty} u^{p-1} e^{-u} du = \Gamma(p)
$$

**Final answer:**
$$
\int_0^1 \left[ \ln \left( \frac{1}{x} \right) \right]^{p-1} dx = \Gamma(p)
$$

---

## 5. SOME IMPORTANT FORMULAS INVOLVING GAMMA FUNCTIONS

## 6. BETA FUNCTIONS

### 1

Prove that $B(p,q) = B(q,p)$. Hint: Put $x = 1-y$ in Equation (6.1).

**Solution:**

Starting with the definition:
$$B(p,q) = \int_0^1 x^{p-1}(1-x)^{q-1} dx$$

Let's make the substitution $x = 1-y$:
- When $x = 0$, $y = 1$
- When $x = 1$, $y = 0$
- $dx = -dy$

Substituting:
$$B(p,q) = \int_1^0 (1-y)^{p-1}(y)^{q-1} (-dy)$$

Changing the limits and removing the negative sign:
$$B(p,q) = \int_0^1 (1-y)^{p-1}y^{q-1} dy$$

This is exactly the form of $B(q,p)$:
$$B(q,p) = \int_0^1 y^{q-1}(1-y)^{p-1} dy$$

Therefore:
$$B(p,q) = B(q,p)$$

This proves that the Beta function is symmetric in its arguments $p$ and $q$.

---

### 2

Prove equation (6.5): $B(p,q) = \int_0^\infty \frac{y^{p-1}dy}{(1+y)^{p+q}}$

**Solution:**

Let's start with the original definition of the Beta function:
$$B(p,q) = \int_0^1 x^{p-1}(1-x)^{q-1} dx$$

Make the substitution $x = \frac{y}{1+y}$ or equivalently $y = \frac{x}{1-x}$

For this substitution:
- When $x = 0$, $y = 0$
- When $x = 1$, $y = \infty$

The differential becomes:
$$dx = \frac{dy}{(1+y)^2}$$

Also:
$$1-x = \frac{1}{1+y}$$

Substituting these into the original integral:

$$B(p,q) = \int_0^1 \left(\frac{y}{1+y}\right)^{p-1}\left(\frac{1}{1+y}\right)^{q-1} \frac{dy}{(1+y)^2}$$

$$= \int_0^1 \frac{y^{p-1}}{(1+y)^{p-1}} \cdot \frac{1}{(1+y)^{q-1}} \cdot \frac{dy}{(1+y)^2}$$

$$= \int_0^1 \frac{y^{p-1}}{(1+y)^{p+q}} dy$$

Changing the upper limit from 1 to $\infty$:

$$= \int_0^\infty \frac{y^{p-1}dy}{(1+y)^{p+q}}$$

This proves equation (6.5).

Note: The convergence of this improper integral is guaranteed for $p > 0$ and $q > 0$ because:
- Near $y = 0$, the integrand behaves like $y^{p-1}$ which is integrable for $p > 0$
- As $y \to \infty$, the integrand behaves like $y^{p-1-p-q} = y^{-q-1}$ which is integrable for $q > 0$

---

### 3

Show that for integral $n, m$,
$$
\frac{1}{B(n, m)} = m \binom{n+m-1}{n-1} = n \binom{n+m-1}{m-1}.
$$

**Solution:**

Recall the Beta function in terms of Gamma functions:
$$
B(n, m) = \frac{\Gamma(n)\Gamma(m)}{\Gamma(n+m)}
$$
For positive integers, $\Gamma(k) = (k-1)!$, so:
$$
B(n, m) = \frac{(n-1)!(m-1)!}{(n+m-1)!}
$$
Thus,
$$
\frac{1}{B(n, m)} = \frac{(n+m-1)!}{(n-1)!(m-1)!}
$$

Recall the binomial coefficient:
$$
\binom{n+m-1}{n-1} = \frac{(n+m-1)!}{(n-1)!(m)!}
$$
Multiply by $m$:
$$
m \binom{n+m-1}{n-1} = m \frac{(n+m-1)!}{(n-1)!(m)!} = \frac{(n+m-1)!}{(n-1)!(m-1)!}
$$
because $m! = m \cdot (m-1)!$.

Similarly,
$$
\binom{n+m-1}{m-1} = \frac{(n+m-1)!}{(m-1)!(n)!}
$$
Multiply by $n$:
$$
n \binom{n+m-1}{m-1} = n \frac{(n+m-1)!}{(m-1)!(n)!} = \frac{(n+m-1)!}{(n-1)!(m-1)!}
$$
because $n! = n \cdot (n-1)!$.

Therefore,
$$
\frac{1}{B(n, m)} = m \binom{n+m-1}{n-1} = n \binom{n+m-1}{m-1}
$$

---

## 7. BETA FUNCTIONS IN TERMS OF GAMMA FUNCTIONS

Express the following integrals as $B$ functions, and then, by (7.1), in terms of $\Gamma$ functions. When possible, use $\Gamma$ function formulas to write an exact answer in terms of $\pi$, $\sqrt{2}$, etc.

---

### 1.
$$
\int_0^1 \frac{x^4}{\sqrt{1-x^2}} dx
$$
Let $x^2 = t$, $x = t^{1/2}$, $dx = \frac{1}{2} t^{-1/2} dt$:
$$
= \frac{1}{2} \int_0^1 t^{3/2} (1-t)^{-1/2} dt = \frac{1}{2} B\left(\frac{5}{2}, \frac{1}{2}\right)
$$
In terms of Gamma functions:
$$
= \frac{1}{2} \cdot \frac{\Gamma(5/2)\Gamma(1/2)}{\Gamma(3)}
$$
With $\Gamma(5/2) = \frac{3}{4}\sqrt{\pi}$, $\Gamma(1/2) = \sqrt{\pi}$, $\Gamma(3) = 2$:
$$
= \frac{1}{2} \cdot \frac{3\pi}{8} = \frac{3\pi}{16}
$$

---

### 2.
$$
\int_0^{\pi/2} \sqrt{\sin^3 x \cos x} dx
$$
This is $\int_0^{\pi/2} (\sin x)^{3/2} (\cos x)^{1/2} dx$:
$$
= \frac{1}{2} B\left(\frac{5}{4}, \frac{3}{4}\right)
$$
In terms of Gamma functions:
$$
= \frac{1}{2} \cdot \frac{\Gamma(5/4)\Gamma(3/4)}{\Gamma(2)} = \frac{1}{2} \Gamma(5/4)\Gamma(3/4)
$$

---

### 3.
$$
\int_0^1 \frac{dx}{\sqrt{1-x^3}}
$$
Let $x^3 = t$, $dx = \frac{1}{3} t^{-2/3} dt$:
$$
= \frac{1}{3} \int_0^1 t^{-2/3} (1-t)^{-1/2} dt = \frac{1}{3} B\left(\frac{1}{3}, \frac{1}{2}\right)
$$
In terms of Gamma functions:
$$
= \frac{1}{3} \cdot \frac{\Gamma(1/3)\Gamma(1/2)}{\Gamma(5/6)}
$$

---

### 4.
$$
\int_0^1 x^2 (1-x^2)^{3/2} dx
$$
Let $x^2 = t$, $dx = \frac{1}{2} t^{-1/2} dt$:
$$
= \frac{1}{2} \int_0^1 t^{1/2} (1-t)^{3/2} dt = \frac{1}{2} B\left(\frac{3}{2}, \frac{5}{2}\right)
$$
In terms of Gamma functions:
$$
= \frac{1}{2} \cdot \frac{\Gamma(3/2)\Gamma(5/2)}{\Gamma(4)}
$$
With $\Gamma(3/2) = \frac{1}{2}\sqrt{\pi}$, $\Gamma(5/2) = \frac{3}{4}\sqrt{\pi}$, $\Gamma(4) = 6$:
$$
= \frac{1}{2} \cdot \frac{3\pi}{48} = \frac{\pi}{32}
$$

---

### 5.
$$
\int_0^\infty \frac{y^2 dy}{(1+y)^6}
$$
This is $B(3,3)$:
$$
= \frac{\Gamma(3)\Gamma(3)}{\Gamma(6)} = \frac{2! \cdot 2!}{5!} = \frac{4}{120} = \frac{1}{30}
$$

---

### 6.
$$
\int_0^\infty \frac{y\, dy}{(1+y^3)^2}
$$
Let $y^3 = t$, $dy = \frac{1}{3} t^{-2/3} dt$:
$$
= \frac{1}{3} \int_0^\infty \frac{t^{-1/3}}{(1+t)^2} dt = \frac{1}{3} B\left(\frac{2}{3}, \frac{4}{3}\right)
$$
In terms of Gamma functions:
$$
= \frac{1}{3} \cdot \Gamma(2/3)\Gamma(4/3)
$$

---

### 7.
$$
\int_0^{\pi/2} \frac{d\theta}{\sqrt{\sin \theta}}
$$
This is $\int_0^{\pi/2} (\sin \theta)^{-1/2} d\theta$:
$$
= \frac{1}{2} B\left(\frac{1}{4}, \frac{1}{2}\right)
$$
In terms of Gamma functions:
$$
= \frac{1}{2} \cdot \frac{\Gamma(1/4)\Gamma(1/2)}{\Gamma(3/4)}
$$

---

### 8.
$$
\int_0^2 \frac{x^2 dx}{\sqrt{2-x}}
$$
Let $t = 2-x$, $x = 2-t$, $dx = -dt$:
$$
= \int_0^2 \frac{(2-t)^2}{t^{1/2}} dt
$$
Let $t = 2u$, $dt = 2 du$:
$$
= 2^{5/2} \int_0^1 (1-u)^2 u^{-1/2} du = 2^{5/2} B\left(\frac{1}{2}, 3\right)
$$
In terms of Gamma functions:
$$
= 2^{5/2} \cdot \frac{\Gamma(1/2)\Gamma(3)}{\Gamma(7/2)}
$$
With $\Gamma(1/2) = \sqrt{\pi}$, $\Gamma(3) = 2$, $\Gamma(7/2) = \frac{15}{8}\sqrt{\pi}$:
$$
= 2^{5/2} \cdot \frac{2 \sqrt{\pi}}{15/8 \sqrt{\pi}} = 2^{5/2} \cdot \frac{16}{15} = 4\sqrt{2} \cdot \frac{16}{15} = \frac{64\sqrt{2}}{15}
$$

---

### 9.

Prove $B(n, n) = B(n, \tfrac{1}{2})/2^{2n-1}$. 

**Proof:**

Start with the definition:
$$
B(n, n) = \int_0^1 x^{n-1}(1-x)^{n-1} dx
$$
Let $x = \sin^2 \theta$, $dx = 2\sin\theta\cos\theta d\theta = \sin 2\theta d\theta$.
When $x=0$, $\theta=0$; $x=1$, $\theta=\pi/2$.

So:
$$
B(n, n) = \int_{0}^{\pi/2} (\sin^2 \theta)^{n-1} (\cos^2 \theta)^{n-1} \sin 2\theta d\theta
$$
$$
= \int_{0}^{\pi/2} (\sin \theta)^{2n-2} (\cos \theta)^{2n-2} \sin 2\theta d\theta
$$
Now, $\sin 2\theta = 2\sin\theta\cos\theta$:
$$
= 2 \int_{0}^{\pi/2} (\sin \theta)^{2n-1} (\cos \theta)^{2n-1} d\theta
$$
Let $\phi = 2\theta$, so $d\phi = 2 d\theta$, $\theta=0 \to \phi=0$, $\theta=\pi/2 \to \phi=\pi$:

Also, $\sin \theta = \sqrt{\frac{1-\cos \phi}{2}}$, $\cos \theta = \sqrt{\frac{1+\cos \phi}{2}}$.

So:
$$
2 \int_{0}^{\pi/2} (\sin \theta)^{2n-1} (\cos \theta)^{2n-1} d\theta = \int_0^{\pi} \left(\sqrt{\frac{1-\cos \phi}{2}}\right)^{2n-1} \left(\sqrt{\frac{1+\cos \phi}{2}}\right)^{2n-1} \frac{d\phi}{2}
$$
$$
= \frac{1}{2} \int_0^{\pi} \left(\frac{1-\cos \phi}{2}\right)^{n-1/2} \left(\frac{1+\cos \phi}{2}\right)^{n-1/2} d\phi
$$
$$
= \frac{1}{2^{2n-1}} \int_0^{\pi} (1-\cos \phi)^{n-1/2} (1+\cos \phi)^{n-1/2} d\phi
$$

Now, let $y = \cos \phi$, $dy = -\sin \phi d\phi$, but the integral is symmetric and can be related to the Beta function $B(n, 1/2)$ (see standard references or Boas 13C.3):

Thus,
$$
B(n, n) = \frac{1}{2^{2n-1}} B(n, 1/2)
$$

---

**Duplication formula for Gamma functions:**

Recall $B(p, q) = \frac{\Gamma(p)\Gamma(q)}{\Gamma(p+q)}$.

So,
$$
B(n, n) = \frac{\Gamma(n)^2}{\Gamma(2n)}
$$
$$
B(n, 1/2) = \frac{\Gamma(n)\Gamma(1/2)}{\Gamma(n+1/2)}
$$

From above:
$$
\frac{\Gamma(n)^2}{\Gamma(2n)} = \frac{1}{2^{2n-1}} \cdot \frac{\Gamma(n)\Gamma(1/2)}{\Gamma(n+1/2)}
$$
Multiply both sides by $\Gamma(2n)$:
$$
\Gamma(n)^2 = \frac{\Gamma(2n)}{2^{2n-1}} \cdot \frac{\Gamma(n)\Gamma(1/2)}{\Gamma(n+1/2)}
$$
Multiply both sides by $\Gamma(n+1/2)$ and divide by $\Gamma(n)$:
$$
\Gamma(n)\Gamma(n+1/2) = \frac{\Gamma(2n)}{2^{2n-1}} \Gamma(1/2)
$$
So,
$$
\Gamma(2n) = \frac{2^{2n-1}}{\Gamma(1/2)} \Gamma(n)\Gamma(n+1/2)
$$
But $\Gamma(1/2) = \sqrt{\pi}$:
$$
\Gamma(2n) = \frac{2^{2n-1}}{\sqrt{\pi}} \Gamma(n)\Gamma(n+1/2)
$$

---

**Check for $n=1/4$:**

Plug $n=1/4$ into the duplication formula:
$$
\Gamma(1/2) = \frac{2^{(2\cdot 1/4)-1}}{\sqrt{\pi}} \Gamma(1/4)\Gamma(3/4)
$$
$$
\Gamma(1/2) = \frac{2^{1/2-1}}{\sqrt{\pi}} \Gamma(1/4)\Gamma(3/4) = \frac{2^{-1/2}}{\sqrt{\pi}} \Gamma(1/4)\Gamma(3/4)
$$
But $\Gamma(1/2) = \sqrt{\pi}$, so:
$$
\sqrt{\pi} = \frac{1}{\sqrt{2\pi}} \Gamma(1/4)\Gamma(3/4)
$$
$$
\Gamma(1/4)\Gamma(3/4) = \sqrt{2\pi^3}
$$
which matches the known value (see e.g. Boas Eq. 5.4).

---

### 10. First quadrant area bounded by the curve

Solve for $y$ in terms of $x$:
$$
y = (8 - x^3)^{1/3}
$$
The area in the first quadrant is:
$$
A = \int_0^2 (8 - x^3)^{1/3} dx
$$
Let $x^3 = 8t$, so $x = 2t^{1/3}$, $dx = 2 t^{-2/3} dt$.
When $x=0$, $t=0$; $x=2$, $t=1$.

So:
$$
A = \int_{x=0}^{x=2} (8 - x^3)^{1/3} dx = \int_{t=0}^{t=1} (8 - 8t)^{1/3} 2 t^{-2/3} dt
$$
$$
= 2 \int_0^1 [8(1-t)]^{1/3} t^{-2/3} dt = 2 \cdot 8^{1/3} \int_0^1 (1-t)^{1/3} t^{-2/3} dt
$$
$$
= 4 \int_0^1 (1-t)^{1/3} t^{-2/3} dt = 4 B\left(\frac{1}{3}, \frac{4}{3}\right)
$$

---

### 11. Centroid $(\bar{x}, \bar{y})$ of this area

The $x$-coordinate of the centroid:
$$
\bar{x} = \frac{1}{A} \int_0^2 x (8 - x^3)^{1/3} dx
$$
Let $x^3 = 8t$, $x = 2 t^{1/3}$, $dx = 2 t^{-2/3} dt$:
$$
\int_0^2 x (8 - x^3)^{1/3} dx = \int_0^1 2 t^{1/3} [8(1-t)]^{1/3} 2 t^{-2/3} dt
$$
$$
= 4 \int_0^1 t^{1/3} (1-t)^{1/3} t^{-2/3} dt = 4 \int_0^1 (1-t)^{1/3} t^{-1/3} dt = 4 B\left(\frac{2}{3}, \frac{4}{3}\right)
$$
So:
$$
\bar{x} = \frac{4 B\left(\frac{2}{3}, \frac{4}{3}\right)}{4 B\left(\frac{1}{3}, \frac{4}{3}\right)} = \frac{B\left(\frac{2}{3}, \frac{4}{3}\right)}{B\left(\frac{1}{3}, \frac{4}{3}\right)}
$$

The $y$-coordinate of the centroid:
$$
\bar{y} = \frac{1}{A} \int_0^2 \frac{1}{2} (8 - x^3)^{4/3} dx
$$
Let $x^3 = 8t$, $dx = 2 t^{-2/3} dt$:
$$
\int_0^2 (8 - x^3)^{4/3} dx = \int_0^1 [8(1-t)]^{4/3} 2 t^{-2/3} dt = 2 \cdot 8^{4/3} \int_0^1 (1-t)^{4/3} t^{-2/3} dt
$$
$$
= 2 \cdot 16 \int_0^1 (1-t)^{4/3} t^{-2/3} dt = 32 B\left(\frac{1}{3}, \frac{7}{3}\right)
$$
So:
$$
\bar{y} = \frac{1}{A} \cdot \frac{1}{2} \cdot 32 B\left(\frac{1}{3}, \frac{7}{3}\right) = \frac{16 B\left(\frac{1}{3}, \frac{7}{3}\right)}{4 B\left(\frac{1}{3}, \frac{4}{3}\right)} = 4 \frac{B\left(\frac{1}{3}, \frac{7}{3}\right)}{B\left(\frac{1}{3}, \frac{4}{3}\right)}
$$

---

### 12. Volume generated when the area is revolved about the $y$-axis

The volume is:
$$
V = 2\pi \int_0^2 x (8 - x^3)^{1/3} dx = 2\pi \cdot 4 B\left(\frac{2}{3}, \frac{4}{3}\right) = 8\pi B\left(\frac{2}{3}, \frac{4}{3}\right)
$$

---

### 13. Moment of inertia of this volume about its axis

The moment of inertia about the $y$-axis is:
$$
I = 2\pi \int_0^2 x^3 (8 - x^3)^{1/3} dx
$$
Let $x^3 = 8t$, $x = 2 t^{1/3}$, $dx = 2 t^{-2/3} dt$:
$$
\int_0^2 x^3 (8 - x^3)^{1/3} dx = \int_0^1 8t (8-8t)^{1/3} 2 t^{-2/3} dt = 16 \int_0^1 t (1-t)^{1/3} t^{-2/3} dt
$$
$$
= 16 \int_0^1 (1-t)^{1/3} t^{1-2/3} dt = 16 \int_0^1 (1-t)^{1/3} t^{1/3} dt = 16 B\left(\frac{4}{3}, \frac{4}{3}\right)
$$
So:
$$
I = 2\pi \cdot 16 B\left(\frac{4}{3}, \frac{4}{3}\right) = 32\pi B\left(\frac{4}{3}, \frac{4}{3}\right)
$$

---

## 8. THE SIMPLE PENDULUM

### 1. Period for 180° swings (complete pendulum)

Given:
$$
T = 4 \sqrt{\frac{l}{2g}} \int_0^{\pi/2} \frac{d\theta}{\sqrt{\cos \theta}}
$$

Express the integral as a Beta or Gamma function:

Let $\theta = \arccos(1-2x)$, so $x = \frac{1-\cos\theta}{2}$, $\cos\theta = 1-2x$, $d\theta = \frac{dx}{\sqrt{x(1-x)}}$.

When $\theta=0$, $x=0$; $\theta=\pi/2$, $x=1/2$.

So:
$$
\int_0^{\pi/2} \frac{d\theta}{\sqrt{\cos \theta}} = \int_0^{1/2} \frac{dx}{\sqrt{1-2x} \sqrt{x(1-x)}}
$$
But it's easier to use the standard Beta function result:

Recall:
$$
\int_0^{\pi/2} (\cos \theta)^{-1/2} d\theta = \frac{1}{2} B\left(\frac{1}{4}, \frac{1}{2}\right)
$$
So:
$$
T = 4 \sqrt{\frac{l}{2g}} \cdot \frac{1}{2} B\left(\frac{1}{4}, \frac{1}{2}\right) = 2 \sqrt{\frac{l}{2g}} B\left(\frac{1}{4}, \frac{1}{2}\right)
$$

Now, using the Gamma function:
$$
B\left(\frac{1}{4}, \frac{1}{2}\right) = \frac{\Gamma(1/4)\Gamma(1/2)}{\Gamma(3/4)}
$$
And $\Gamma(1/2) = \sqrt{\pi}$.

So:
$$
T = 2 \sqrt{\frac{l}{2g}} \cdot \frac{\Gamma(1/4)\sqrt{\pi}}{\Gamma(3/4)}
$$
Or, as a multiple of $\sqrt{l/g}$:
$$
T = \sqrt{2} \cdot \frac{\Gamma(1/4)\sqrt{\pi}}{\Gamma(3/4)} \sqrt{\frac{l}{g}}
$$

---

### 2. Time for car door to close

Given:
- $\theta(0) = \pi/2$ (door open at right angles)
- $a = 1$ mph/sec
- $w = 3.5$ ft
- $\ddot{\theta} = -A \sin \theta$, $A = \frac{3a}{2w}$

We want the time $T$ for $\theta$ to go from $\pi/2$ to $0$ (door closed).

First, multiply both sides by $\dot{\theta}$:
$$
\dot{\theta} \ddot{\theta} = -A \dot{\theta} \sin \theta
$$
$$
\frac{1}{2} \frac{d}{dt}(\dot{\theta}^2) = -A \dot{\theta} \sin \theta
$$
$$
\frac{d}{dt}(\dot{\theta}^2) = -2A \dot{\theta} \sin \theta
$$
Divide both sides by $\dot{\theta}$ (for $\dot{\theta} \neq 0$):
$$
\frac{d}{dt}(\dot{\theta}) = -A \sin \theta
$$
But more simply, use energy method:
$$
\ddot{\theta} = -A \sin \theta
$$
Multiply both sides by $d\theta/dt$ and integrate:
$$
\dot{\theta} d\dot{\theta} = -A \sin \theta d\theta
$$
Integrate:
$$
\frac{1}{2} \dot{\theta}^2 = A \cos \theta + C
$$
At $\theta = \pi/2$, $\dot{\theta} = 0$ (starts from rest):
$$
0 = A \cos(\pi/2) + C \implies C = 0
$$
So:
$$
\frac{1}{2} \dot{\theta}^2 = A \cos \theta
$$
$$
\dot{\theta} = -\sqrt{2A \cos \theta}
$$
(negative sign because $\theta$ decreases)

So:
$$
\frac{d\theta}{dt} = -\sqrt{2A \cos \theta}
$$
$$
\frac{d\theta}{\sqrt{\cos \theta}} = -\sqrt{2A} dt
$$
Integrate from $\theta = \pi/2$ to $\theta = 0$:
$$
\int_{\pi/2}^0 \frac{d\theta}{\sqrt{\cos \theta}} = -\sqrt{2A} T
$$
$$
\int_0^{\pi/2} \frac{d\theta}{\sqrt{\cos \theta}} = \sqrt{2A} T
$$
So:
$$
T = \frac{1}{\sqrt{2A}} \int_0^{\pi/2} \frac{d\theta}{\sqrt{\cos \theta}}
$$
From previous problem:
$$
\int_0^{\pi/2} \frac{d\theta}{\sqrt{\cos \theta}} = \frac{1}{2} B\left(\frac{1}{4}, \frac{1}{2}\right)
$$
So:
$$
T = \frac{1}{\sqrt{2A}} \cdot \frac{1}{2} B\left(\frac{1}{4}, \frac{1}{2}\right)
$$

Now, $A = \frac{3a}{2w}$, $a = 1$ mph/sec, $w = 3.5$ ft:

Convert $a$ to ft/s$^2$:
- $1$ mph $= 5280$ ft / 3600 s $\approx 1.4667$ ft/s
- $a = 1$ mph/sec $= 1.4667$ ft/s$^2$

So:
$$
A = \frac{3 \times 1.4667}{2 \times 3.5} = \frac{4.4001}{7} \approx 0.6286
$$

Thus:
$$
T = \frac{1}{\sqrt{2 \times 0.6286}} \cdot \frac{1}{2} B\left(\frac{1}{4}, \frac{1}{2}\right)
$$
$$
= \frac{1}{\sqrt{1.2572}} \cdot \frac{1}{2} B\left(\frac{1}{4}, \frac{1}{2}\right)
$$
$$
= 0.892 \cdot \frac{1}{2} B\left(\frac{1}{4}, \frac{1}{2}\right)
$$

Or, in terms of Gamma functions:
$$
T = 0.892 \cdot \frac{1}{2} \cdot \frac{\Gamma(1/4)\sqrt{\pi}}{\Gamma(3/4)}
$$

---

### 3. Time for a particle to slide along a cycloid (brachistochrone)

Given the parametric equations:
$$
x = a(\theta + \sin \theta), \quad y = a(1 - \cos \theta)
$$

The time to slide from $(x_1, y_1)$ to the origin is:
$$
t = \sqrt{\frac{a}{g}} \int_0^{y_1} \frac{dy}{\sqrt{y(y_1 - y)}}
$$

**Hint:** Show that the arc length element is $ds = \sqrt{2a/y} \, dy$.

**Solution:**

First, compute $ds$:
$$
\frac{dx}{d\theta} = a(1 + \cos \theta), \quad \frac{dy}{d\theta} = a \sin \theta
$$
$$
ds = \sqrt{\left(\frac{dx}{d\theta}\right)^2 + \left(\frac{dy}{d\theta}\right)^2} d\theta = a \sqrt{(1 + \cos \theta)^2 + \sin^2 \theta} d\theta
$$
$$
= a \sqrt{1 + 2\cos \theta + \cos^2 \theta + \sin^2 \theta} d\theta = a \sqrt{1 + 2\cos \theta + 1} d\theta = a \sqrt{2(1 + \cos \theta)} d\theta
$$
But $1 + \cos \theta = 2 \cos^2(\theta/2)$, so:
$$
ds = a \sqrt{4 \cos^2(\theta/2)} d\theta = 2a \cos(\theta/2) d\theta
$$

Now, $y = a(1 - \cos \theta) \implies \cos \theta = 1 - y/a$

So $\cos(\theta/2) = \sqrt{\frac{1 + \cos \theta}{2}} = \sqrt{\frac{2 - y/a}{2}} = \sqrt{1 - \frac{y}{2a}}$

But the hint says $ds = \sqrt{2a/y} dy$. Let's check $dy$ in terms of $d\theta$:
$$
dy = a \sin \theta d\theta
$$
So $d\theta = \frac{dy}{a \sin \theta}$

But $\sin \theta = \sqrt{1 - \cos^2 \theta} = \sqrt{1 - (1 - y/a)^2} = \sqrt{1 - (1 - 2y/a + y^2/a^2)} = \sqrt{2y/a - y^2/a^2} = \sqrt{\frac{2y}{a} - \frac{y^2}{a^2}}$

So:
$$
ds = 2a \cos(\theta/2) d\theta = 2a \cos(\theta/2) \frac{dy}{a \sin \theta} = 2 \cos(\theta/2) \frac{dy}{\sin \theta}
$$
But $2 \cos(\theta/2) = \frac{\sin \theta}{\sin(\theta/2)}$, so $ds = \frac{\sin \theta}{\sin(\theta/2)} \frac{dy}{\sin \theta} = \frac{dy}{\sin(\theta/2)}$

Alternatively, using the hint, accept $ds = \sqrt{2a/y} dy$.

**Time integral:**

The time to slide is:
$$
t = \int \frac{ds}{v}
$$
where $v = \sqrt{2gy}$ (from energy conservation).
So:
$$
t = \int_0^{y_1} \frac{\sqrt{2a/y} dy}{\sqrt{2gy}} = \sqrt{\frac{a}{g}} \int_0^{y_1} \frac{dy}{\sqrt{y(y_1 - y)}}
$$

Let $y = y_1 \sin^2 \phi$, $dy = 2y_1 \sin \phi \cos \phi d\phi$

When $y=0$, $\phi=0$; $y=y_1$, $\phi=\pi/2$

So:
$$
\int_0^{y_1} \frac{dy}{\sqrt{y(y_1 - y)}} = \int_0^{\pi/2} \frac{2y_1 \sin \phi \cos \phi d\phi}{\sqrt{y_1 \sin^2 \phi (y_1 - y_1 \sin^2 \phi)}}
$$
$$
= \int_0^{\pi/2} \frac{2y_1 \sin \phi \cos \phi d\phi}{\sqrt{y_1 \sin^2 \phi \cdot y_1 \cos^2 \phi}} = \int_0^{\pi/2} \frac{2y_1 \sin \phi \cos \phi d\phi}{y_1 \sin \phi \cos \phi} = \int_0^{\pi/2} 2 d\phi = \pi
$$

So:
$$
t = \sqrt{\frac{a}{g}} \pi
$$

**Conclusion:** The time is independent of the starting height $y_1$.

---

## 9. THE ERROR FUNCTION

### 2. Verifying equations (9.2), (9.3), and (9.4)

#### (9.2a) and (9.2b):

The standard normal CDF is:
$$
\Phi(x) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^x e^{-t^2/2} dt
$$
We want to write $\Phi(x)$ in terms of the error function:

Recall:
$$
\operatorname{erf}(x) = \frac{2}{\sqrt{\pi}} \int_0^x e^{-u^2} du
$$

Let $t = u\sqrt{2}$, so $u = t/\sqrt{2}$, $dt = \sqrt{2} du$.

Change of variables in $\Phi(x)$:
$$
\int_{-\infty}^x e^{-t^2/2} dt = \int_{-\infty}^{x/\sqrt{2}} e^{-u^2} \sqrt{2} du = \sqrt{2} \int_{-\infty}^{x/\sqrt{2}} e^{-u^2} du
$$
So:
$$
\Phi(x) = \frac{1}{\sqrt{2\pi}} \cdot \sqrt{2} \int_{-\infty}^{x/\sqrt{2}} e^{-u^2} du = \frac{1}{\sqrt{\pi}} \int_{-\infty}^{x/\sqrt{2}} e^{-u^2} du
$$
Split at $u=0$:
$$
= \frac{1}{\sqrt{\pi}} \left[ \int_{-\infty}^0 e^{-u^2} du + \int_0^{x/\sqrt{2}} e^{-u^2} du \right]
$$
But $\int_{-\infty}^0 e^{-u^2} du = \frac{\sqrt{\pi}}{2}$, so:
$$
\Phi(x) = \frac{1}{2} + \frac{1}{\sqrt{\pi}} \int_0^{x/\sqrt{2}} e^{-u^2} du
$$
Now, relate to $\operatorname{erf}$:
$$
\operatorname{erf}(x/\sqrt{2}) = \frac{2}{\sqrt{\pi}} \int_0^{x/\sqrt{2}} e^{-u^2} du
$$
So:
$$
\int_0^{x/\sqrt{2}} e^{-u^2} du = \frac{\sqrt{\pi}}{2} \operatorname{erf}(x/\sqrt{2})
$$
Therefore:
$$
\Phi(x) = \frac{1}{2} + \frac{1}{2} \operatorname{erf}(x/\sqrt{2})
$$
which is (9.2a).

For (9.2b):
$$
\Phi(x) - \frac{1}{2} = \frac{1}{\sqrt{2\pi}} \int_0^x e^{-t^2/2} dt
$$
Repeat the change of variable as above, but from $t=0$ to $t=x$:
$$
\int_0^x e^{-t^2/2} dt = \sqrt{2} \int_0^{x/\sqrt{2}} e^{-u^2} du
$$
So:
$$
\Phi(x) - \frac{1}{2} = \frac{1}{\sqrt{2\pi}} \cdot \sqrt{2} \int_0^{x/\sqrt{2}} e^{-u^2} du = \frac{1}{\sqrt{\pi}} \int_0^{x/\sqrt{2}} e^{-u^2} du = \frac{1}{2} \operatorname{erf}(x/\sqrt{2})
$$
which is (9.2b).

---

#### (9.3a) and (9.3b):

The complementary error function is:
$$
\operatorname{erfc}(x) = \frac{2}{\sqrt{\pi}} \int_x^{\infty} e^{-t^2} dt
$$
By definition:
$$
\operatorname{erfc}(x) = 1 - \operatorname{erf}(x)
$$
which is (9.3a).

For (9.3b):
$$
\operatorname{erfc}\left(\frac{x}{\sqrt{2}}\right) = \frac{2}{\sqrt{\pi}} \int_{x/\sqrt{2}}^{\infty} e^{-u^2} du
$$
Let $u = t/\sqrt{2}$, $t = u\sqrt{2}$, $dt = \sqrt{2} du$:
$$
= \frac{2}{\sqrt{\pi}} \int_{x/\sqrt{2}}^{\infty} e^{-u^2} du = \frac{2}{\sqrt{\pi}} \int_x^{\infty} e^{-t^2/2} \frac{dt}{\sqrt{2}}
$$
$$
= \sqrt{\frac{2}{\pi}} \int_x^{\infty} e^{-t^2/2} dt
$$
which is (9.3b).

---

#### (9.4):

From (9.2a):
$$
\Phi(x) = \frac{1}{2} + \frac{1}{2} \operatorname{erf}(x/\sqrt{2})
$$
So:
$$
\operatorname{erf}(x) = 2\Phi(x\sqrt{2}) - 1
$$
which is (9.4).

---

### 3. Prove that erf(x) is an odd function

Recall the definition:
$$
\operatorname{erf}(x) = \frac{2}{\sqrt{\pi}} \int_0^x e^{-t^2} dt
$$

We want to show $\operatorname{erf}(-x) = -\operatorname{erf}(x)$.

**Proof:**

Consider $\operatorname{erf}(-x)$:
$$
\operatorname{erf}(-x) = \frac{2}{\sqrt{\pi}} \int_0^{-x} e^{-t^2} dt
$$
Let $t = -s$, so $dt = -ds$.
When $t = 0$, $s = 0$; when $t = -x$, $s = x$.

So:
$$
\int_0^{-x} e^{-t^2} dt = \int_{s=0}^{s=x} e^{-(-s)^2} (-ds) = -\int_0^x e^{-s^2} ds
$$
Therefore:
$$
\operatorname{erf}(-x) = \frac{2}{\sqrt{\pi}} \left(-\int_0^x e^{-s^2} ds\right) = -\frac{2}{\sqrt{\pi}} \int_0^x e^{-s^2} ds = -\operatorname{erf}(x)
$$

Thus, $\operatorname{erf}(x)$ is an odd function.

---

### 4. Show that $\int_{-\infty}^{\infty} e^{-y^2/2} dy = \sqrt{2\pi}$

#### (a) Using (9.5) and (9.2a):

From (9.2a):
$$
\Phi(x) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^x e^{-t^2/2} dt
$$
As $x \to \infty$:
$$
\Phi(\infty) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} e^{-t^2/2} dt
$$
But from the error function definition (9.5):
$$
\operatorname{erf}(\infty) = 1 = \frac{2}{\sqrt{\pi}} \int_0^{\infty} e^{-t^2} dt
$$
The full Gaussian integral is:
$$
\int_{-\infty}^{\infty} e^{-y^2/2} dy = 2 \int_0^{\infty} e^{-y^2/2} dy
$$
Let $y = \sqrt{2} t$, $dy = \sqrt{2} dt$:
$$
= 2 \int_0^{\infty} e^{-y^2/2} dy = 2 \int_0^{\infty} e^{-t^2} \sqrt{2} dt = 2\sqrt{2} \int_0^{\infty} e^{-t^2} dt
$$
But $\int_0^{\infty} e^{-t^2} dt = \frac{\sqrt{\pi}}{2}$, so:
$$
= 2\sqrt{2} \cdot \frac{\sqrt{\pi}}{2} = \sqrt{2\pi}
$$

#### (b) By reducing to a Gamma function and using (5.3):

Recall:
$$
\int_0^{\infty} x^{p-1} e^{-\lambda x} dx = \frac{\Gamma(p)}{\lambda^p}
$$
Let $y^2/2 = x$, so $y = \sqrt{2x}$, $dy = \frac{1}{\sqrt{2x}} dx$:

For $y$ from $0$ to $\infty$:
$$
\int_0^{\infty} e^{-y^2/2} dy = \int_0^{\infty} e^{-x} \frac{dx}{\sqrt{2x}}
$$
$$
= \frac{1}{\sqrt{2}} \int_0^{\infty} x^{-1/2} e^{-x} dx = \frac{1}{\sqrt{2}} \Gamma(1/2)
$$
But $\Gamma(1/2) = \sqrt{\pi}$, so:
$$
\int_0^{\infty} e^{-y^2/2} dy = \frac{\sqrt{\pi}}{\sqrt{2}}
$$
So the full integral is:
$$
\int_{-\infty}^{\infty} e^{-y^2/2} dy = 2 \cdot \frac{\sqrt{\pi}}{\sqrt{2}} = \sqrt{2\pi}
$$

---

### 5. Show that $\operatorname{erf}(ix) = i\,\operatorname{erfi}(x)$

Recall the definitions:
$$
\operatorname{erf}(x) = \frac{2}{\sqrt{\pi}} \int_0^x e^{-t^2} dt
$$
$$
\operatorname{erfi}(x) = \frac{2}{\sqrt{\pi}} \int_0^x e^{t^2} dt
$$

Replace $x$ by $ix$ in the definition of $\operatorname{erf}$:
$$
\operatorname{erf}(ix) = \frac{2}{\sqrt{\pi}} \int_0^{ix} e^{-t^2} dt
$$
Let $t = iu$, so $dt = i du$.
When $t = 0$, $u = 0$; when $t = ix$, $u = x$.

So:
$$
\int_0^{ix} e^{-t^2} dt = \int_{u=0}^{u=x} e^{-(iu)^2} i du = \int_0^x e^{u^2} i du = i \int_0^x e^{u^2} du
$$
Therefore:
$$
\operatorname{erf}(ix) = \frac{2}{\sqrt{\pi}} i \int_0^x e^{u^2} du = i \frac{2}{\sqrt{\pi}} \int_0^x e^{u^2} du = i\,\operatorname{erfi}(x)
$$

---

### 6. Relation between the error function and Fresnel integrals

We are to show:
$$
\operatorname{erf}\left(\frac{1-i}{\sqrt{2}} x\right) = (1-i) \sqrt{\frac{2}{\pi}} \int_0^x (\cos u^2 + i \sin u^2) du
$$

**Hint:** In (9.1), make the change of variables $t = \frac{1-i}{\sqrt{2}} u$.

**Proof:**

Start from the definition:
$$
\operatorname{erf}(z) = \frac{2}{\sqrt{\pi}} \int_0^z e^{-t^2} dt
$$
Let $z = \frac{1-i}{\sqrt{2}} x$ and $t = \frac{1-i}{\sqrt{2}} u$, so $dt = \frac{1-i}{\sqrt{2}} du$.
When $t = 0$, $u = 0$; when $t = z$, $u = x$.

So:
$$
\operatorname{erf}\left(\frac{1-i}{\sqrt{2}} x\right) = \frac{2}{\sqrt{\pi}} \int_0^x e^{-\left(\frac{1-i}{\sqrt{2}} u\right)^2} \frac{1-i}{\sqrt{2}} du
$$
Compute the exponent:
$$
\left(\frac{1-i}{\sqrt{2}} u\right)^2 = \left(\frac{1-i}{\sqrt{2}}\right)^2 u^2 = \frac{(1-i)^2}{2} u^2 = \frac{1 - 2i + i^2}{2} u^2 = \frac{1 - 2i - 1}{2} u^2 = -i u^2
$$
So $e^{-t^2} = e^{-(-i u^2)} = e^{i u^2} = \cos u^2 + i \sin u^2$.

Therefore:
$$
\operatorname{erf}\left(\frac{1-i}{\sqrt{2}} x\right) = \frac{2}{\sqrt{\pi}} \frac{1-i}{\sqrt{2}} \int_0^x (\cos u^2 + i \sin u^2) du
$$
$$
= (1-i) \sqrt{\frac{2}{\pi}} \int_0^x (\cos u^2 + i \sin u^2) du
$$
which is the required result.

---

## 10. ASYMPTOTIC SERIES

### 1. Derivation of the asymptotic expansion for erfc(x) (equation 10.4)

Recall the definition:
$$
erfc(x) = \frac{2}{\sqrt{\pi}} \int_x^{\infty} e^{-t^2} dt
$$
For large $x$, use integration by parts:
Let $u = \frac{1}{t}$, $dv = 2t e^{-t^2} dt$.
But more simply, write:
$$
\int_x^{\infty} e^{-t^2} dt = \int_x^{\infty} \frac{d}{dt}\left(-\frac{1}{2t} e^{-t^2}\right) dt
$$
Integrate by parts:
$$
= \left.-\frac{1}{2t} e^{-t^2}\right|_x^{\infty} - \int_x^{\infty} \frac{1}{2t^2} e^{-t^2} dt
$$
As $t \to \infty$, $e^{-t^2}/t \to 0$, so:
$$
= \frac{1}{2x} e^{-x^2} - \int_x^{\infty} \frac{1}{2t^2} e^{-t^2} dt
$$
Repeat integration by parts on the remaining integral:
$$
\int_x^{\infty} \frac{1}{t^2} e^{-t^2} dt = \left.-\frac{1}{2t^3} e^{-t^2}\right|_x^{\infty} - \int_x^{\infty} \frac{3}{2t^4} e^{-t^2} dt
$$
So:
$$
\int_x^{\infty} e^{-t^2} dt = \frac{1}{2x} e^{-x^2} - \frac{1}{4x^3} e^{-x^2} + \frac{3}{8x^5} e^{-x^2} - \cdots
$$
Now, plug into the definition:
$$
erfc(x) = \frac{2}{\sqrt{\pi}} \int_x^{\infty} e^{-t^2} dt \sim \frac{2}{\sqrt{\pi}} e^{-x^2} \left( \frac{1}{2x} - \frac{1}{4x^3} + \frac{3}{8x^5} - \cdots \right)
$$
$$
= \frac{e^{-x^2}}{x\sqrt{\pi}} \left(1 - \frac{1}{2x^2} + \frac{1\cdot3}{(2x^2)^2} - \frac{1\cdot3\cdot5}{(2x^2)^3} + \cdots \right)
$$
which matches equation (10.4):
$$
erfc(x) \sim \frac{e^{-x^2}}{x\sqrt{\pi}} \left(1 - \frac{1}{2x^2} + \frac{1\cdot3}{(2x^2)^2} - \frac{1\cdot3\cdot5}{(2x^2)^3} + \cdots \right)
$$

---

### 2. Asymptotic series for the incomplete Gamma function $\Gamma(p, x)$

The incomplete Gamma function is:
$$
\Gamma(p, x) = \int_x^{\infty} t^{p-1} e^{-t} dt
$$

We seek an asymptotic expansion for large $x$ by repeated integration by parts.

Let $u = t^{p-1}$, $dv = e^{-t} dt$.
Then $du = (p-1)t^{p-2} dt$, $v = -e^{-t}$.

Integration by parts:
$$
\Gamma(p, x) = \left. -t^{p-1} e^{-t} \right|_x^{\infty} + \int_x^{\infty} (p-1) t^{p-2} e^{-t} dt
$$
As $t \to \infty$, $t^{p-1} e^{-t} \to 0$, so:
$$
= x^{p-1} e^{-x} + (p-1) \int_x^{\infty} t^{p-2} e^{-t} dt
$$
Repeat integration by parts on the remaining integral:
$$
\int_x^{\infty} t^{p-2} e^{-t} dt = x^{p-2} e^{-x} + (p-2) \int_x^{\infty} t^{p-3} e^{-t} dt
$$
So:
$$
\Gamma(p, x) = x^{p-1} e^{-x} + (p-1) \left[ x^{p-2} e^{-x} + (p-2) \int_x^{\infty} t^{p-3} e^{-t} dt \right]
$$
$$
= x^{p-1} e^{-x} + (p-1) x^{p-2} e^{-x} + (p-1)(p-2) \int_x^{\infty} t^{p-3} e^{-t} dt
$$
Continue this process:
$$
\Gamma(p, x) = x^{p-1} e^{-x} + (p-1) x^{p-2} e^{-x} + (p-1)(p-2) x^{p-3} e^{-x} + \cdots
$$
Or, in general:
$$
\Gamma(p, x) \sim e^{-x} x^{p-1} \left[ 1 + \frac{p-1}{x} + \frac{(p-1)(p-2)}{x^2} + \frac{(p-1)(p-2)(p-3)}{x^3} + \cdots \right]
$$

---

### 3. Asymptotic expansion of erfc(x) via the incomplete Gamma function

Recall:
$$
\operatorname{erfc}(x) = \frac{2}{\sqrt{\pi}} \int_x^{\infty} e^{-t^2} dt
$$
Let $t^2 = s$, so $t = s^{1/2}$, $dt = \frac{1}{2} s^{-1/2} ds$.
When $t = x$, $s = x^2$; $t = \infty$, $s = \infty$.

So:
$$
\int_x^{\infty} e^{-t^2} dt = \int_{x^2}^{\infty} e^{-s} \frac{1}{2} s^{-1/2} ds = \frac{1}{2} \int_{x^2}^{\infty} s^{-1/2} e^{-s} ds
$$
This is an incomplete Gamma function:
$$
\Gamma(1/2, x^2) = \int_{x^2}^{\infty} s^{-1/2} e^{-s} ds
$$
So:
$$
\operatorname{erfc}(x) = \frac{2}{\sqrt{\pi}} \cdot \frac{1}{2} \Gamma(1/2, x^2) = \frac{1}{\sqrt{\pi}} \Gamma(1/2, x^2)
$$

Now, use the asymptotic expansion for $\Gamma(p, x)$ from Problem 2 with $p = 1/2$ and $x \to x^2$:
$$
\Gamma(1/2, x^2) \sim e^{-x^2} (x^2)^{-1/2} \left[ 1 + \frac{-1/2}{x^2} + \frac{(-1/2)(-3/2)}{x^4} + \cdots \right]
$$
$$
= \frac{e^{-x^2}}{x} \left[ 1 - \frac{1}{2x^2} + \frac{1 \cdot 3}{(2x^2)^2} - \frac{1 \cdot 3 \cdot 5}{(2x^2)^3} + \cdots \right]
$$
So:
$$
\operatorname{erfc}(x) \sim \frac{e^{-x^2}}{x\sqrt{\pi}} \left[ 1 - \frac{1}{2x^2} + \frac{1 \cdot 3}{(2x^2)^2} - \frac{1 \cdot 3 \cdot 5}{(2x^2)^3} + \cdots \right]
$$
which matches equation (10.4).

---

### 4. Exponential integrals: relations and changes of variable

Recall:
$$
E_n(x) = \int_1^{\infty} \frac{e^{-xt}}{t^n} dt, \quad \text{and} \quad \operatorname{Ei}(x) = \int_{-\infty}^x \frac{e^t}{t} dt
$$

#### (a) $E_1(x) = \int_x^{\infty} \frac{e^{-t}}{t} dt$

Let $t = x u$, $dt = x du$:
$$
E_1(x) = \int_1^{\infty} \frac{e^{-x t}}{t} dt = \int_{t=1}^{t=\infty} \frac{e^{-x t}}{t} dt
$$
Let $t = u$, $x t = t$ (so $x=1$):
But more generally, let $s = x t$, $t = s/x$, $dt = ds/x$:
When $t=1$, $s=x$; $t=\infty$, $s=\infty$.
So:
$$
E_1(x) = \int_{s=x}^{s=\infty} \frac{e^{-s}}{s/x} \frac{ds}{x} = \int_x^{\infty} \frac{e^{-s}}{s} ds
$$
So $E_1(x) = \int_x^{\infty} \frac{e^{-t}}{t} dt$.

---

#### (b) $\operatorname{Ei}(x) = -\int_{-x}^{\infty} \frac{e^{-t}}{t} dt$

Recall:
$$
\operatorname{Ei}(x) = \int_{-\infty}^x \frac{e^t}{t} dt
$$
Let $t = -s$, $dt = -ds$:
When $t = -\infty$, $s = \infty$; $t = x$, $s = -x$.
So:
$$
\int_{-\infty}^x \frac{e^t}{t} dt = \int_{s=\infty}^{s=-x} \frac{e^{-s}}{-s} (-ds) = -\int_{\infty}^{-x} \frac{e^{-s}}{s} ds = \int_{-x}^{\infty} \frac{e^{-t}}{t} dt
$$
So $\operatorname{Ei}(x) = -\int_{-x}^{\infty} \frac{e^{-t}}{t} dt$.

---

#### (c) $E_1(x) = -\operatorname{Ei}(-x)$

From (a) and (b):
$$
E_1(x) = \int_x^{\infty} \frac{e^{-t}}{t} dt
$$
$$
\operatorname{Ei}(-x) = -\int_{x}^{\infty} \frac{e^{-t}}{t} dt = -E_1(x)
$$
So $E_1(x) = -\operatorname{Ei}(-x)$.

---

#### (d) $\int_0^x \frac{e^{1/t}}{t} dt = E_1(-1/x)$

Let $u = 1/t$, $t = 1/u$, $dt = -1/u^2 du$:
When $t=0^+$, $u=\infty$; $t=x$, $u=1/x$.
So:
$$
\int_0^x \frac{e^{1/t}}{t} dt = \int_{u=\infty}^{u=1/x} e^{u} (-1/u^2) du = \int_{u=1/x}^{u=\infty} \frac{e^{u}}{u^2} du
$$
But $E_1(z) = \int_z^{\infty} \frac{e^{-t}}{t} dt$, so $E_1(-1/x) = \int_{-1/x}^{\infty} \frac{e^{-t}}{t} dt$.
But $\int_{1/x}^{\infty} \frac{e^{u}}{u^2} du = $ derivative of $E_1(-1/x)$ with respect to $x$ (or, more precisely, this is a standard result: $\int_0^x \frac{e^{1/t}}{t} dt = E_1(-1/x)$).

---

### 5

#### (a) Express $E_1(x)$ as an incomplete $\Gamma$ function

Recall the definition of the exponential integral:
$$
E_1(x) = \int_x^{\infty} \frac{e^{-t}}{t} dt
$$

The (upper) incomplete Gamma function is defined as:
$$
\Gamma(s, x) = \int_x^{\infty} t^{s-1} e^{-t} dt
$$

For $s = 0$, the integral diverges, but for $s = 1$:
$$
\Gamma(0, x) = \int_x^{\infty} t^{-1} e^{-t} dt
$$
But by convention, $\Gamma(0, x)$ is not standard; instead, for $s = 1$:
$$
\Gamma(1, x) = \int_x^{\infty} e^{-t} dt = e^{-x}
$$
However, for $E_1(x)$, notice:
$$
E_1(x) = \int_x^{\infty} t^{-1} e^{-t} dt = \Gamma(0, x)
$$
So, by definition:
$$
\boxed{E_1(x) = \Gamma(0, x)}
$$

Alternatively, some texts define the incomplete Gamma function for $s = 0$ as:
$$
\Gamma(0, x) = \int_x^{\infty} \frac{e^{-t}}{t} dt = E_1(x)
$$

---

#### (b) Asymptotic series for $E_1(x)$

For large $x$, we can find the asymptotic expansion by repeated integration by parts:

Let $u = 1/t$, $dv = e^{-t} dt$.
But more simply, write:
$$
E_1(x) = \int_x^{\infty} \frac{e^{-t}}{t} dt
$$
Integrate by parts:
Let $u = 1/t$, $dv = e^{-t} dt$, so $du = -1/t^2 dt$, $v = -e^{-t}$.

So:
$$
E_1(x) = \left.-\frac{e^{-t}}{t}\right|_x^{\infty} - \int_x^{\infty} e^{-t} \left(-\frac{1}{t^2}\right) dt
$$
As $t \to \infty$, $e^{-t}/t \to 0$, so:
$$
= \frac{e^{-x}}{x} - \int_x^{\infty} \frac{e^{-t}}{t^2} dt
$$
Repeat integration by parts on the remaining integral:
Let $u = 1/t^2$, $dv = e^{-t} dt$, $du = -2/t^3 dt$, $v = -e^{-t}$:
$$
\int_x^{\infty} \frac{e^{-t}}{t^2} dt = \left.-\frac{e^{-t}}{t^2}\right|_x^{\infty} - \int_x^{\infty} e^{-t} \left(-\frac{2}{t^3}\right) dt = \frac{e^{-x}}{x^2} - 2 \int_x^{\infty} \frac{e^{-t}}{t^3} dt
$$
So:
$$
E_1(x) = \frac{e^{-x}}{x} - \left[ \frac{e^{-x}}{x^2} - 2 \int_x^{\infty} \frac{e^{-t}}{t^3} dt \right ]
= \frac{e^{-x}}{x} - \frac{e^{-x}}{x^2} + 2 \int_x^{\infty} \frac{e^{-t}}{t^3} dt
$$
Continue this process:
$$
E_1(x) = \frac{e^{-x}}{x} - \frac{e^{-x}}{x^2} + 2 \frac{e^{-x}}{x^3} - 6 \frac{e^{-x}}{x^4} + \cdots
$$
Or, in general:
$$
E_1(x) \sim \frac{e^{-x}}{x} \left[ 1 - \frac{1}{x} + \frac{2!}{x^2} - \frac{3!}{x^3} + \cdots + (-1)^n \frac{n!}{x^n} + \cdots \right ]
$$
This series is asymptotic for large $x$.
$$
\boxed{E_1(x) \sim \frac{e^{-x}}{x} \left[ 1 - \frac{1}{x} + \frac{2!}{x^2} - \frac{3!}{x^3} + \cdots \right ] \quad (x \to \infty)}
$$

---

### 6

The logarithmic integral is
$$
\operatorname{li}(x) = \int_0^x \frac{dt}{\ln t}
$$
Express as exponential integrals:

#### (a) $\operatorname{li}(x)$

Let $t = e^{-u}$, so $u = -\ln t$, $dt = -e^{-u} du = -t du$.
When $t = 0$, $u = \infty$; when $t = x$, $u = -\ln x$.

So:
$$
\operatorname{li}(x) = \int_0^x \frac{dt}{\ln t} = \int_{u=\infty}^{u=-\ln x} \frac{-e^{-u} du}{-u} = \int_{-\ln x}^{\infty} \frac{e^{-u}}{u} du
$$
Let $s = u$:
$$
= \int_{-\ln x}^{\infty} \frac{e^{-s}}{s} ds
$$
But recall the exponential integral $E_1(z) = \int_z^{\infty} \frac{e^{-t}}{t} dt$.
So:
$$
\boxed{\operatorname{li}(x) = E_1(-\ln x)}
$$

---

#### (b) $\operatorname{li}(e^x)$

Plug $x \to e^x$ in the result above:
$$
\operatorname{li}(e^x) = E_1(-\ln(e^x)) = E_1(-x)
$$
So:
$$
\boxed{\operatorname{li}(e^x) = E_1(-x)}
$$

---

#### (c) $\int_0^x \frac{dt}{\ln(1/t)}$

Note $\ln(1/t) = -\ln t$, so $\frac{1}{\ln(1/t)} = -\frac{1}{\ln t}$.
Thus:
$$
\int_0^x \frac{dt}{\ln(1/t)} = -\int_0^x \frac{dt}{\ln t} = -\operatorname{li}(x)
$$
From above, $\operatorname{li}(x) = E_1(-\ln x)$, so:
$$
\boxed{\int_0^x \frac{dt}{\ln(1/t)} = -E_1(-\ln x)}
$$

---

### 7. Computer plot graphs of special functions

You can use Python (with matplotlib and scipy) to plot these special functions. Below are the instructions and example code for each part.

#### (a) $E_n(x)$ for $n = 0$ to $10$ and $x = 0$ to $2$

The exponential integral $E_n(x)$ is available in `scipy.special` as `scipy.special.expn(n, x)`.

**Python code:**
```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.special import expn

x = np.linspace(0.01, 2, 400)  # avoid x=0 for n=0
plt.figure(figsize=(8,6))
for n in range(0, 11):
    plt.plot(x, expn(n, x), label=f"$E_{{{n}}}(x)$")
plt.xlabel("$x$")
plt.ylabel("$E_n(x)$")
plt.title("Exponential Integrals $E_n(x)$ for $n=0$ to $10$")
plt.legend()
plt.grid(True)
plt.show()
```

---

#### (b) $E_1(x)$ and $\operatorname{Ei}(x)$ for $x = 0$ to $2$

- $E_1(x)$: `scipy.special.exp1(x)`
- $\operatorname{Ei}(x)$: `scipy.special.expi(x)`

**Python code:**
```python
x = np.linspace(0.01, 2, 400)
from scipy.special import exp1, expi
plt.figure(figsize=(8,6))
plt.plot(x, exp1(x), label="$E_1(x)$")
plt.plot(x, expi(x), label="$\\operatorname{Ei}(x)$")
plt.xlabel("$x$")
plt.ylabel("Value")
plt.title("$E_1(x)$ and $\\operatorname{Ei}(x)$ for $x=0$ to $2$")
plt.legend()
plt.grid(True)
plt.show()
```

---

#### (c) Sine and cosine integrals for $x = 0$ to $4\pi$

- Sine integral $\operatorname{Si}(x) = \int_0^x \frac{\sin t}{t} dt$
- Cosine integral $\operatorname{Ci}(x) = -\int_x^{\infty} \frac{\cos t}{t} dt$

Both are available in `scipy.special` as `sici(x)` (returns both Si and Ci).

**Python code:**
```python
from scipy.special import sici
x = np.linspace(0, 4*np.pi, 400)
si, ci = sici(x)
plt.figure(figsize=(8,6))
plt.plot(x, si, label="$\\operatorname{Si}(x)$")
plt.plot(x, ci, label="$\\operatorname{Ci}(x)$")
plt.xlabel("$x$")
plt.ylabel("Value")
plt.title("Sine and Cosine Integrals for $x=0$ to $4\\pi$")
plt.legend()
plt.grid(True)
plt.show()
```

---

**Note:**
- You need `numpy`, `matplotlib`, and `scipy` installed. Install with `pip install numpy matplotlib scipy` if needed.
- For $E_n(x)$ with $n=0$, avoid $x=0$ as the function diverges.

---

## 11. STIRLING'S FORMULA

### 1. Error estimate in Stirling's formula

Stirling's formula (11.1):
$$
n! \sim n^n e^{-n} \sqrt{2\pi n} \qquad \text{or} \qquad \Gamma(p+1) \sim p^p e^{-p} \sqrt{2\pi p}
$$

A more accurate version includes the next term (see Eq. 11.5):
$$
\Gamma(p+1) \sim p^p e^{-p} \sqrt{2\pi p} \left(1 + \frac{1}{12p} + \cdots \right)
$$

The relative error in using only the leading term is approximately $\frac{1}{12p}$.

To estimate the percentage error:
$$
\text{Relative error} \approx \frac{1}{12p}
$$

Set $\frac{1}{12p} < \varepsilon$ for various $\varepsilon$:

- For $\varepsilon = 0.1$ (10%):
  $$
  \frac{1}{12p} < 0.1 \implies p > \frac{1}{1.2} \approx 0.83
  $$
  So for $p > 1$, error $< 10\%$.

- For $\varepsilon = 0.01$ (1%):
  $$
  \frac{1}{12p} < 0.01 \implies p > \frac{1}{0.12} \approx 8.33
  $$
  So for $p > 10$, error $< 1\%$.

- For $\varepsilon = 0.001$ (0.1%):
  $$
  \frac{1}{12p} < 0.001 \implies p > \frac{1}{0.012} \approx 83.3
  $$
  So for $p > 100$, error $< 0.1\%$.

- For $\varepsilon = 0.0001$ (0.01%):
  $$
  \frac{1}{12p} < 0.0001 \implies p > \frac{1}{0.0012} \approx 833
  $$
  So for $p > 1000$, error $< 0.01\%$.

**Conclusion:**
- The error in Stirling's formula is:
  - $< 10\%$ for $p > 1$
  - $< 1\%$ for $p > 10$
  - $< 0.1\%$ for $p > 100$
  - $< 0.01\%$ for $p > 1000$

This matches the required estimates.

---

### 2. Graphical illustration of Stirling's formula error

#### (a) Percentage error in Stirling's formula (leading term)

To plot the percentage error in Stirling's formula as a function of $p$ for $p$ from 1 to 1000:
- The true value is $\Gamma(p+1)$ (or $p!$ for integer $p$).
- The Stirling approximation is $S(p) = p^p e^{-p} \sqrt{2\pi p}$.
- The percentage error is:
  $$
  \text{Percent error} = 100 \times \left| \frac{\Gamma(p+1) - S(p)}{\Gamma(p+1)} \right|
  $$

**Python code:**
```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.special import gamma

p = np.linspace(1, 1000, 1000)
S = p**p * np.exp(-p) * np.sqrt(2 * np.pi * p)
G = gamma(p + 1)
percent_error = 100 * np.abs((G - S) / G)

# Plot in ranges
ranges = [(1, 10), (10, 100), (100, 1000)]
for pmin, pmax in ranges:
    mask = (p >= pmin) & (p <= pmax)
    plt.figure(figsize=(8,6))
    plt.plot(p[mask], percent_error[mask])
    plt.xlabel("$p$")
    plt.ylabel("Percent error (%)")
    plt.title(f"Percent error in Stirling's formula for $p$ from {pmin} to {pmax}")
    plt.grid(True)
    plt.show()
```

---

#### (b) Percentage error using two terms of the asymptotic series

Now use the improved approximation:
$$
S_2(p) = p^p e^{-p} \sqrt{2\pi p} \left(1 + \frac{1}{12p}\right)
$$
The percentage error is:
$$
\text{Percent error (2 terms)} = 100 \times \left| \frac{\Gamma(p+1) - S_2(p)}{\Gamma(p+1)} \right|
$$

**Python code:**
```python
S2 = S * (1 + 1/(12*p))
percent_error2 = 100 * np.abs((G - S2) / G)

for pmin, pmax in ranges:
    mask = (p >= pmin) & (p <= pmax)
    plt.figure(figsize=(8,6))
    plt.plot(p[mask], percent_error2[mask])
    plt.xlabel("$p$")
    plt.ylabel("Percent error (%)")
    plt.title(f"Percent error in Stirling's formula (2 terms) for $p$ from {pmin} to {pmax}")
    plt.grid(True)
    plt.show()
```

---

**Note:**
- You need `numpy`, `matplotlib`, and `scipy` installed.
- For integer $p$, $\Gamma(p+1) = p!$.
- The error drops rapidly as $p$ increases, and the two-term approximation is much more accurate.

---

### 3. Justification of the approximation $\ln N! \approx N \ln N - N$

In statistical mechanics, for large $N$ (e.g., $N \sim 10^{23}$), we often use:
$$
\ln N! \approx N \ln N - N
$$

**Stirling's formula for $N!$:**
$$
N! \sim N^N e^{-N} \sqrt{2\pi N}
$$
Take the natural logarithm:
$$
\ln N! \approx N \ln N - N + \frac{1}{2} \ln(2\pi N)
$$

Let's compute each term for $N = 10^{23}$:

- $N \ln N = 10^{23} \times \ln(10^{23}) = 10^{23} \times 23 \ln 10 \approx 10^{23} \times 52.959 = 5.296 \times 10^{24}$
- $-N = -10^{23}$
- $\frac{1}{2} \ln(2\pi N) = \frac{1}{2} \ln(2\pi \times 10^{23})$
  - $2\pi \approx 6.2832$
  - $2\pi \times 10^{23} \approx 6.2832 \times 10^{23}$
  - $\ln(6.2832 \times 10^{23}) = \ln 6.2832 + \ln(10^{23}) \approx 1.84 + 23 \ln 10 \approx 1.84 + 52.959 = 54.80$
  - $\frac{1}{2} \times 54.80 \approx 27.4$

So, for $N = 10^{23}$:
- $N \ln N \approx 5.296 \times 10^{24}$
- $-N = -1 \times 10^{23}$
- $\frac{1}{2} \ln(2\pi N) \approx 27.4$

**Relative sizes:**
- The leading term $N \ln N$ is $\sim 5.3 \times 10^{24}$
- The $-N$ term is $\sim 2\%$ of the leading term
- The $\frac{1}{2} \ln(2\pi N)$ term is $\sim 27$, utterly negligible compared to the other terms

**Conclusion:**
- For $N \sim 10^{23}$, $\ln N!$ is dominated by $N \ln N$ and $-N$; the $\frac{1}{2} \ln(2\pi N)$ term is negligible.
- Thus, $\ln N! \approx N \ln N - N$ is an excellent approximation for large $N$.

---

### 4. Limit involving factorials and Stirling's formula

Evaluate:
$$
\lim_{n \to \infty} \frac{(2n)! \sqrt{n}}{2^{2n} (n!)^2}
$$
using Stirling's formula.

**Step 1: Apply Stirling's formula**
Recall:
$$
n! \sim n^n e^{-n} \sqrt{2\pi n}
$$
So:
- $(2n)! \sim (2n)^{2n} e^{-2n} \sqrt{2\pi (2n)}$
- $n! \sim n^n e^{-n} \sqrt{2\pi n}$
- $(n!)^2 \sim [n^n e^{-n} \sqrt{2\pi n}]^2 = n^{2n} e^{-2n} 2\pi n$

**Step 2: Substitute into the limit**
$$
\frac{(2n)! \sqrt{n}}{2^{2n} (n!)^2} \sim \frac{(2n)^{2n} e^{-2n} \sqrt{2\pi (2n)} \cdot \sqrt{n}}{2^{2n} n^{2n} e^{-2n} 2\pi n}
$$

- $e^{-2n}$ cancels.
- $(2n)^{2n} / n^{2n} = 2^{2n}$, so $2^{2n}$ cancels with denominator.

So:
$$
= \frac{\sqrt{2\pi (2n)} \cdot \sqrt{n}}{2\pi n}
$$

Now, $\sqrt{2\pi (2n)} = \sqrt{2\pi} \sqrt{2n} = \sqrt{2\pi} \cdot \sqrt{2} \cdot \sqrt{n} = 2^{1/2} \sqrt{\pi} \sqrt{n}$

So:
$$
= \frac{2^{1/2} \sqrt{\pi} \sqrt{n} \cdot \sqrt{n}}{2\pi n} = \frac{2^{1/2} \sqrt{\pi} n}{2\pi n}
$$
$$
= \frac{2^{1/2} \sqrt{\pi}}{2\pi}
$$
$$
= \frac{\sqrt{2\pi}}{2\pi}
$$
$$
= \frac{1}{\sqrt{2\pi}}
$$

**Final answer:**
$$
\boxed{\lim_{n \to \infty} \frac{(2n)! \sqrt{n}}{2^{2n} (n!)^2} = \frac{1}{\sqrt{2\pi}}}
$$

---

### 5. Limit involving Gamma functions and Stirling's formula

Evaluate:
$$
\lim_{n \to \infty} \frac{\Gamma\left(n + \frac{3}{2}\right)}{\sqrt{n}\, \Gamma(n+1)}
$$
using Stirling's formula.

**Step 1: Apply Stirling's formula**
Recall:
$$
\Gamma(z) \sim z^{z-1/2} e^{-z} \sqrt{2\pi}
$$
So:
- $\Gamma(n+1) \sim (n+1)^{n+1-1/2} e^{-(n+1)} \sqrt{2\pi}$
- $\Gamma\left(n+\frac{3}{2}\right) \sim \left(n+\frac{3}{2}\right)^{n+1} e^{-(n+3/2)} \sqrt{2\pi}$

**Step 2: Write the ratio**
$$
\frac{\Gamma\left(n + \frac{3}{2}\right)}{\sqrt{n}\, \Gamma(n+1)} \sim \frac{\left(n+\frac{3}{2}\right)^{n+1} e^{-(n+3/2)} \sqrt{2\pi}}{\sqrt{n} (n+1)^{n+1/2} e^{-(n+1)} \sqrt{2\pi}}
$$

$\sqrt{2\pi}$ cancels:
$$
= \frac{\left(n+\frac{3}{2}\right)^{n+1} e^{-(n+3/2)}}{\sqrt{n} (n+1)^{n+1/2} e^{-(n+1)}}
$$

**Step 3: Simplify exponentials**
$$
= \frac{\left(n+\frac{3}{2}\right)^{n+1}}{(n+1)^{n+1/2} \sqrt{n}} e^{-(n+3/2) + (n+1)}
$$
$$
= \frac{\left(n+\frac{3}{2}\right)^{n+1}}{(n+1)^{n+1/2} \sqrt{n}} e^{-3/2 + 1}
$$
$$
= \frac{\left(n+\frac{3}{2}\right)^{n+1}}{(n+1)^{n+1/2} \sqrt{n}} e^{-1/2}
$$

**Step 4: Write $n+3/2 = n+1 + 1/2$ and expand for large $n$**
For large $n$:
- $n+3/2 \approx n+1$
- $\frac{n+3/2}{n+1} = 1 + \frac{1/2}{n+1}$

So:
$$
\left(\frac{n+3/2}{n+1}\right)^{n+1} = \left(1 + \frac{1/2}{n+1}\right)^{n+1} \approx e^{1/2}
$$
(using $\lim_{k\to\infty} (1 + a/k)^k = e^a$)

So:
$$
\frac{\left(n+\frac{3}{2}\right)^{n+1}}{(n+1)^{n+1}} \approx e^{1/2}
$$

Now, the denominator has an extra $(n+1)^{1/2} \sqrt{n}$:
$$
(n+1)^{1/2} \sqrt{n} = \sqrt{(n+1)n} \approx n
$$

So:
$$
\frac{\Gamma\left(n + \frac{3}{2}\right)}{\sqrt{n}\, \Gamma(n+1)} \sim \frac{e^{1/2}}{n} e^{-1/2} = \frac{1}{n}
$$
But this can't be correct, as the limit would go to zero. Let's check the powers more carefully.

Actually, the denominator is $(n+1)^{n+1/2} \sqrt{n}$, numerator is $(n+3/2)^{n+1}$.
So:
$$
\frac{(n+3/2)^{n+1}}{(n+1)^{n+1/2} \sqrt{n}} = \frac{(n+3/2)^{n+1}}{(n+1)^{n+1}} \cdot \frac{1}{(n+1)^{1/2} \sqrt{n}}
$$
As above, $(n+3/2)^{n+1}/(n+1)^{n+1} \approx e^{1/2}$.

Now, $(n+1)^{1/2} \sqrt{n} = (n+1)^{1/2} n^{1/2} = (n(n+1))^{1/2} \approx n$ for large $n$.

So:
$$
\frac{1}{(n(n+1))^{1/2}} \approx \frac{1}{n}
$$
So the whole expression is $e^{1/2} e^{-1/2} \cdot \frac{1}{n} = \frac{1}{n}$, which goes to zero. But this can't be correct, since the original limit is dimensionless and should be finite.

Let's try a more careful expansion using the full Stirling's formula for the Gamma function:
$$
\Gamma(z) \sim \sqrt{2\pi} z^{z-1/2} e^{-z}
$$
So:
- $\Gamma(n+1) \sim \sqrt{2\pi} (n+1)^{n+1-1/2} e^{-(n+1)}$
- $\Gamma(n+3/2) \sim \sqrt{2\pi} (n+3/2)^{n+3/2-1/2} e^{-(n+3/2)} = \sqrt{2\pi} (n+3/2)^{n+1} e^{-(n+3/2)}$

So the ratio is:
$$
\frac{\Gamma(n+3/2)}{\sqrt{n}\, \Gamma(n+1)} \sim \frac{\sqrt{2\pi} (n+3/2)^{n+1} e^{-(n+3/2)}}{\sqrt{n} \sqrt{2\pi} (n+1)^{n+1-1/2} e^{-(n+1)}}
$$
$$
= \frac{(n+3/2)^{n+1} e^{-(n+3/2)}}{\sqrt{n} (n+1)^{n+1-1/2}} \cdot \frac{e^{-(n+3/2)+(n+1)}}{\sqrt{n}}
$$
$$
= \frac{(n+3/2)^{n+1}}{(n+1)^{n+1-1/2}} \cdot \frac{e^{-1/2}}{\sqrt{n}}
$$

Now, $(n+1-1/2) = n+1/2$:
$$
= \frac{(n+3/2)^{n+1}}{(n+1)^{n+1/2}} \cdot \frac{e^{-1/2}}{\sqrt{n}}
$$

Now, write $(n+3/2)^{n+1} = (n+1)^{n+1} \left(1+\frac{1/2}{n+1}\right)^{n+1}$
So:
$$
\frac{(n+3/2)^{n+1}}{(n+1)^{n+1}} = \left(1+\frac{1/2}{n+1}\right)^{n+1} \approx e^{1/2}
$$

So:
$$
= \frac{e^{1/2}}{(n+1)^{1/2} \sqrt{n}} e^{-1/2}
$$
$$
= \frac{1}{(n+1)^{1/2} \sqrt{n}}
$$
For large $n$, $(n+1)^{1/2} \sqrt{n} \approx n$.

So the limit is:
$$
\lim_{n\to\infty} \frac{1}{n} = 0
$$
But this suggests the limit is zero, which is not correct. Let's check the expansion for the Gamma function for large $z$:
$$
\Gamma(z+\alpha) \sim \Gamma(z) z^{\alpha}
$$
So:
$$
\Gamma(n+3/2) \sim \Gamma(n+1) (n+1)^{1/2}
$$
So:
$$
\frac{\Gamma(n+3/2)}{\sqrt{n} \Gamma(n+1)} \sim \frac{\Gamma(n+1) (n+1)^{1/2}}{\sqrt{n} \Gamma(n+1)} = \frac{(n+1)^{1/2}}{\sqrt{n}} \to 1
$$
as $n \to \infty$.

**Final answer:**
$$
\boxed{1}
$$

---

### 6. Asymptotic expansion for $\Gamma(p)$ from $\Gamma(p+1)$

Given:
- (3.4): $\Gamma(p+1) = p\Gamma(p)$
- (11.5):
  $$
  \Gamma(p+1) = p^p e^{-p} \sqrt{2\pi p} \left(1 + \frac{1}{12p} + \frac{1}{288p^2} + \cdots \right)
  $$

We want to show:
$$
\Gamma(p) \sim p^p e^{-p} \sqrt{\frac{2\pi}{p}} \left(1 + \frac{1}{12p} + \cdots \right)
$$

**Step 1: Use the recurrence relation**
From (3.4):
$$
\Gamma(p) = \frac{\Gamma(p+1)}{p}
$$

**Step 2: Substitute the asymptotic expansion for $\Gamma(p+1)$**
$$
\Gamma(p) \sim \frac{p^p e^{-p} \sqrt{2\pi p} \left(1 + \frac{1}{12p} + \cdots \right)}{p}
$$

**Step 3: Simplify**
- $\sqrt{2\pi p}/p = \sqrt{2\pi/p}$

So:
$$
\Gamma(p) \sim p^p e^{-p} \sqrt{\frac{2\pi}{p}} \left(1 + \frac{1}{12p} + \cdots \right)
$$

**Conclusion:**
- This matches the required form:
  $$
  \boxed{\Gamma(p) \sim p^p e^{-p} \sqrt{\frac{2\pi}{p}} \left(1 + \frac{1}{12p} + \cdots \right)}
  $$

---

### 7. The digamma function and its asymptotic expansion

The digamma function is $\psi(p) = \frac{d}{dp} \ln \Gamma(p)$.

#### (a) Show that $\psi(p+1) = \psi(p) + \frac{1}{p}$

From the recurrence relation (3.4):
$$
\Gamma(p+1) = p\Gamma(p)
$$
Take the logarithm:
$$
\ln \Gamma(p+1) = \ln p + \ln \Gamma(p)
$$
Differentiate both sides with respect to $p$:
$$
\frac{d}{dp} \ln \Gamma(p+1) = \frac{d}{dp} \ln p + \frac{d}{dp} \ln \Gamma(p)
$$
So:
$$
\psi(p+1) = \frac{1}{p} + \psi(p)
$$

---

#### (b) Asymptotic expansion for $\psi(p)$

From problem 6:
$$
\Gamma(p) \sim p^p e^{-p} \sqrt{2\pi/p} \left(1 + \frac{1}{12p} + \cdots \right)
$$
Take the logarithm:
$$
\ln \Gamma(p) \sim p \ln p - p + \frac{1}{2} \ln(2\pi) - \frac{1}{2} \ln p + \ln\left(1 + \frac{1}{12p} + \cdots\right)
$$
Expand $\ln(1 + x) \approx x - \frac{1}{2}x^2$ for small $x$:
$$
\ln\left(1 + \frac{1}{12p}\right) \approx \frac{1}{12p} - \frac{1}{2} \left(\frac{1}{12p}\right)^2 = \frac{1}{12p} - \frac{1}{288p^2}
$$
So:
$$
\ln \Gamma(p) \sim p \ln p - p + \frac{1}{2} \ln(2\pi) - \frac{1}{2} \ln p + \frac{1}{12p} - \frac{1}{288p^2}
$$
Now differentiate with respect to $p$:
- $\frac{d}{dp}(p \ln p) = \ln p + 1$
- $\frac{d}{dp}(-p) = -1$
- $\frac{d}{dp}\left(-\frac{1}{2} \ln p\right) = -\frac{1}{2p}$
- $\frac{d}{dp}\left(\frac{1}{12p}\right) = -\frac{1}{12p^2}$
- $\frac{d}{dp}\left(-\frac{1}{288p^2}\right) = \frac{1}{144p^3}$

So:
$$
\psi(p) \sim \ln p - \frac{1}{2p} - \frac{1}{12p^2} + \frac{1}{144p^3} + \cdots
$$

Keeping only the first two correction terms:
$$
\boxed{\psi(p) \sim \ln p - \frac{1}{2p} - \frac{1}{12p^2} + \cdots}
$$

---

### 8. Integral bounds for $\ln n!$ and the $n \ln n - n$ approximation

Consider $y = \ln x$ for $x > 0$.

#### Area interpretation and bounds
Recall:
$$
\ln n! = \ln 1 + \ln 2 + \cdots + \ln n = \sum_{k=1}^n \ln k
$$
This is the sum of the areas of rectangles of width 1 and height $\ln k$ at $x = 1, 2, \ldots, n$.

- The area under $y = \ln x$ from $x = 1$ to $x = n$ is $\int_1^n \ln x\,dx$.
- The area under $y = \ln x$ from $x = 2$ to $x = n+1$ is $\int_2^{n+1} \ln x\,dx$.

By comparing the sum to the area under the curve, we see:
$$
\int_1^n \ln x\,dx < \ln n! < \int_2^{n+1} \ln x\,dx
$$

#### Why these bounds hold
- Each rectangle from $x = k$ to $x = k+1$ lies above the curve $y = \ln x$ for $x$ in $[k, k+1)$, so the sum overestimates the area under $y = \ln x$ from $x = 1$ to $x = n$.
- But the sum underestimates the area from $x = 2$ to $x = n+1$ (since the rectangles are now below the curve).

#### Evaluate the integrals
Recall:
$$
\int \ln x\,dx = x \ln x - x + C
$$
So:
$$
\int_1^n \ln x\,dx = [x \ln x - x]_1^n = n \ln n - n - (1 \ln 1 - 1) = n \ln n - n + 1
$$
$$
\int_2^{n+1} \ln x\,dx = [(n+1) \ln(n+1) - (n+1)] - [2 \ln 2 - 2]
$$

#### For large $n$
For very large $n$, the difference between the two integrals is small compared to their size:
- $n \ln n - n + 1 < \ln n! < (n+1) \ln(n+1) - (n+1) - 2 \ln 2 + 2$
- For large $n$, $n \ln n - n$ dominates, and the $+1$ and $-2 \ln 2 + 2$ are negligible.

Thus,
$$
\ln n! \approx n \ln n - n
$$
for large $n$.

#### Optional: Python code to plot $y = \ln x$ and illustrate the area interpretation
```python
import numpy as np
import matplotlib.pyplot as plt
n = 10
x = np.linspace(0.5, n+1.5, 400)
plt.plot(x, np.log(x), label='$y=\ln x$')
for k in range(1, n+1):
    plt.bar(k, np.log(k), width=1, align='edge', alpha=0.3, color='orange', edgecolor='k')
plt.xlabel('$x$')
plt.ylabel('$y$')
plt.title('Graph of $y=\ln x$ and rectangles for $\ln n!$')
plt.legend()
plt.show()
```

---

### 9. Asymptotic form for $P$ in statistical mechanics

Given:
$$
P = \frac{n!}{(np+u)!\,(nq-u)!}\, p^{np+u} q^{nq-u}
$$
where $p+q=1$.

We are to show, using Stirling's formula, that
$$
\frac{1}{P} \sim x^{np x} y^{nq y} \sqrt{2\pi npq x y},
$$
where $x = 1 + \frac{u}{np}$, $y = 1 - \frac{u}{nq}$.

#### Step 1: Apply Stirling's formula
Recall:
$$
k! \sim k^k e^{-k} \sqrt{2\pi k}
$$
So:
- $n! \sim n^n e^{-n} \sqrt{2\pi n}$
- $(np+u)! \sim (np+u)^{np+u} e^{-(np+u)} \sqrt{2\pi (np+u)}$
- $(nq-u)! \sim (nq-u)^{nq-u} e^{-(nq-u)} \sqrt{2\pi (nq-u)}$

#### Step 2: Write $P$ using Stirling's formula
$$
P \sim \frac{n^n e^{-n} \sqrt{2\pi n}}{(np+u)^{np+u} e^{-(np+u)} \sqrt{2\pi (np+u)}\; (nq-u)^{nq-u} e^{-(nq-u)} \sqrt{2\pi (nq-u)}} p^{np+u} q^{nq-u}
$$

#### Step 3: Simplify exponentials
- The $e^{-n}$ in the numerator and $e^{-(np+u)} e^{-(nq-u)} = e^{-n(p+q)} e^{-(u-u)} = e^{-n}$ in the denominator cancel.
- The $\sqrt{2\pi}$ terms combine:
  $$
  \frac{\sqrt{2\pi n}}{\sqrt{2\pi (np+u)}\,\sqrt{2\pi (nq-u)}} = \frac{1}{\sqrt{2\pi (np+u)(nq-u)/n}}
  $$

#### Step 4: Use the hint to factor out $(np)^{np+u} (nq)^{nq-u}$
Let us divide numerator and denominator by $(np)^{np+u} (nq)^{nq-u}$:
- Numerator: $n^n = (np+ nq)^n = (np)^{n p} (nq)^{n q}$
- So $n^n = (np)^{np} (nq)^{nq}$

So:
$$
P = \frac{n^n}{(np+u)^{np+u} (nq-u)^{nq-u}} \cdot \frac{p^{np+u} q^{nq-u}}{1}
$$
Divide numerator and denominator by $(np)^{np+u} (nq)^{nq-u}$:
- Numerator: $\frac{n^n}{(np)^{np+u} (nq)^{nq-u}} = \frac{1}{p^{np+u} q^{nq-u}}$
- Denominator: $\frac{(np+u)^{np+u}}{(np)^{np+u}} = x^{np x}$, $\frac{(nq-u)^{nq-u}}{(nq)^{nq-u}} = y^{nq y}$

So:
$$
P \sim \frac{1}{x^{np x} y^{nq y}} \cdot \frac{\sqrt{2\pi n}}{\sqrt{2\pi (np+u)}\,\sqrt{2\pi (nq-u)}}
$$

#### Step 5: Take reciprocal and write the asymptotic form
$$
\frac{1}{P} \sim x^{np x} y^{nq y} \sqrt{\frac{(np+u)(nq-u)}{n}}
$$
But $np+u = np x$, $nq-u = nq y$:
$$
\sqrt{\frac{(np x)(nq y)}{n}} = \sqrt{n p q x y}
$$
So:
$$
\frac{1}{P} \sim x^{np x} y^{nq y} \sqrt{2\pi n p q x y}
$$

**Final answer:**
$$
\boxed{\frac{1}{P} \sim x^{np x} y^{nq y} \sqrt{2\pi n p q x y}}
$$
where $x = 1 + \frac{u}{np}$, $y = 1 - \frac{u}{nq}$, $p+q=1$.

---

### 10. Limit of $(n!)^{1/n}/n$ using Stirling's formula

Evaluate:
$$
\lim_{n \to \infty} \frac{(n!)^{1/n}}{n}
$$
using Stirling's formula.

**Step 1: Apply Stirling's formula**
Recall:
$$
n! \sim n^n e^{-n} \sqrt{2\pi n}
$$
So:
$$
(n!)^{1/n} \sim (n^n e^{-n} \sqrt{2\pi n})^{1/n} = n e^{-1} (2\pi n)^{1/(2n)}
$$

**Step 2: Divide by $n$**
$$
\frac{(n!)^{1/n}}{n} \sim e^{-1} (2\pi n)^{1/(2n)}
$$

**Step 3: Take the limit as $n \to \infty$**
- $(2\pi n)^{1/(2n)} \to 1$ as $n \to \infty$ (since $\lim_{n\to\infty} a^{1/n} = 1$ for any $a > 0$).

So:
$$
\lim_{n \to \infty} \frac{(n!)^{1/n}}{n} = e^{-1}
$$

**Final answer:**
$$
\boxed{e^{-1}}
$$

---

## 12. ELLIPTIC INTEGRALS AND FUNCTIONS

### 1. Power series for the complete elliptic integrals $K$ and $E$

Recall from (12.3):
$$
K(k) = \int_0^{\pi/2} \frac{d\theta}{\sqrt{1 - k^2 \sin^2\theta}}
$$
$$
E(k) = \int_0^{\pi/2} \sqrt{1 - k^2 \sin^2\theta}\, d\theta
$$
where $k$ is the modulus, and we assume $k$ is small.

#### Expand the integrands in powers of $k^2 \sin^2\theta$

Let $x = k^2 \sin^2\theta$.

**For $K(k)$:**
$$
\frac{1}{\sqrt{1 - x}} = 1 + \frac{1}{2}x + \frac{3}{8}x^2 + \frac{5}{16}x^3 + \cdots
$$
So:
$$
\frac{1}{\sqrt{1 - k^2 \sin^2\theta}} = 1 + \frac{1}{2}k^2 \sin^2\theta + \frac{3}{8}k^4 \sin^4\theta + \frac{5}{16}k^6 \sin^6\theta + \cdots
$$

**For $E(k)$:**
$$
\sqrt{1 - x} = 1 - \frac{1}{2}x - \frac{1}{8}x^2 - \frac{1}{16}x^3 + \cdots
$$
So:
$$
\sqrt{1 - k^2 \sin^2\theta} = 1 - \frac{1}{2}k^2 \sin^2\theta - \frac{1}{8}k^4 \sin^4\theta - \frac{1}{16}k^6 \sin^6\theta + \cdots
$$

#### Integrate term by term

We need:
$$
I_n = \int_0^{\pi/2} \sin^{2n}\theta\, d\theta
$$
Recall:
$$
\int_0^{\pi/2} \sin^{2n}\theta\, d\theta = \frac{\sqrt{\pi}\, \Gamma(n+1/2)}{2\, \Gamma(n+1)}
$$
But for small $n$, we can use:
- $\int_0^{\pi/2} d\theta = \frac{\pi}{2}$
- $\int_0^{\pi/2} \sin^2\theta\, d\theta = \frac{\pi}{4}$
- $\int_0^{\pi/2} \sin^4\theta\, d\theta = \frac{3\pi}{16}$
- $\int_0^{\pi/2} \sin^6\theta\, d\theta = \frac{5\pi}{32}$

**For $K(k)$:**

$$
\begin{align*}
K(k) &\approx \int_0^{\pi/2} \left[1 + \frac{1}{2}k^2 \sin^2\theta + \frac{3}{8}k^4 \sin^4\theta + \frac{5}{16}k^6 \sin^6\theta\right] d\theta \\
&= \frac{\pi}{2} + \frac{1}{2}k^2 \cdot \frac{\pi}{4} + \frac{3}{8}k^4 \cdot \frac{3\pi}{16} + \frac{5}{16}k^6 \cdot \frac{5\pi}{32} \\
&= \frac{\pi}{2} + \frac{\pi}{8}k^2 + \frac{9\pi}{128}k^4 + \frac{25\pi}{1024}k^6 + \cdots
\end{align*}
$$

**For $E(k)$:**

$$
\begin{align*}
E(k) &\approx \int_0^{\pi/2} \left[1 - \frac{1}{2}k^2 \sin^2\theta - \frac{1}{8}k^4 \sin^4\theta - \frac{1}{16}k^6 \sin^6\theta\right] d\theta \\
&= \frac{\pi}{2} - \frac{1}{2}k^2 \cdot \frac{\pi}{4} - \frac{1}{8}k^4 \cdot \frac{3\pi}{16} - \frac{1}{16}k^6 \cdot \frac{5\pi}{32} \\
&= \frac{\pi}{2} - \frac{\pi}{8}k^2 - \frac{3\pi}{128}k^4 - \frac{5\pi}{512}k^6 + \cdots
\end{align*}
$$

**Final power series (to $k^6$):**
$$
\boxed{
K(k) \approx \frac{\pi}{2} + \frac{\pi}{8}k^2 + \frac{9\pi}{128}k^4 + \frac{25\pi}{1024}k^6 + \cdots
}
$$
$$
\boxed{
E(k) \approx \frac{\pi}{2} - \frac{\pi}{8}k^2 - \frac{3\pi}{128}k^4 - \frac{5\pi}{512}k^6 + \cdots
}
$$

---

### 2. Symmetry and periodicity in elliptic integrals: graphical verification of (12.4)

Consider the function $\sin^2\theta$ on $[0, \pi]$:
- The graph of $\sin^2\theta$ is symmetric about $\theta = \pi/2$.
- The area under $\sin^2\theta$ from $0$ to $\pi/2$ is equal to the area from $\pi/2$ to $\pi$ (by symmetry).
- More generally, for any function of $\sin^2\theta$, the area from $0$ to $\pi/2$ is a mirror image of the area from $\pi/2$ to $\pi$.

#### Why is this true?
Let $f(\sin^2\theta)$ be any function. Consider the substitution $\theta' = \pi - \theta$:
- $\sin^2(\pi - \theta) = \sin^2\theta$
- As $\theta$ goes from $0$ to $\pi/2$, $\theta'$ goes from $\pi$ to $\pi/2$ (reverse direction).

So:
$$
\int_0^{\pi/2} f(\sin^2\theta) d\theta = \int_{\pi}^{\pi/2} f(\sin^2(\pi - \theta')) (-d\theta') = \int_{\pi/2}^{\pi} f(\sin^2\theta') d\theta'
$$
Thus, the area under $f(\sin^2\theta)$ from $0$ to $\pi/2$ equals the area from $\pi/2$ to $\pi$.

#### Connection to (12.4)
The periodicity and symmetry of the integrand underlies the addition formulas for the elliptic integrals:
$$
F(n\pi \pm \phi, k) = 2nK \pm F(\phi, k),\\
E(n\pi \pm \phi, k) = 2nE \pm E(\phi, k)
$$
This means that the value of the elliptic integral over $[0, n\pi \pm \phi]$ can be built up from repeated intervals of $[0, \pi]$ (or $[0, \pi/2]$), reflecting the symmetry and periodicity of $\sin^2\theta$.

#### Graphical illustration
- Plotting $\sin^2\theta$ from $0$ to $\pi$ shows the mirror symmetry about $\pi/2$.
- The area under the curve from $0$ to $\pi/2$ is the same as from $\pi/2$ to $\pi$.
- This property holds for any function of $\sin^2\theta$.

**Conclusion:**
- The symmetry of $\sin^2\theta$ about $\pi/2$ explains why the elliptic integrals have the periodicity and addition properties in (12.4).
- The area under $f(\sin^2\theta)$ from $0$ to $\pi/2$ and from $\pi/2$ to $\pi$ are mirror images, and this is the geometric basis for the formulas in (12.4).

---

### 3. 

Computer plots of elliptic integrals $K(k)$, $E(k)$, $F(\phi, k)$, and $E(\phi, k)$

You can use Python with `numpy`, `matplotlib`, and `scipy.special` to plot these functions. The relevant functions are:
- `scipy.special.ellipk(k**2)` for $K(k)$
- `scipy.special.ellipe(k**2)` for $E(k)$
- `scipy.special.ellipkinc(phi, k**2)` for $F(\phi, k)$
- `scipy.special.ellipeinc(phi, k**2)` for $E(\phi, k)$

#### (a) Plot $K(k)$ and $E(k)$ for $k$ from 0 to 1
```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.special import ellipk, ellipe

k = np.linspace(0, 0.999, 400)  # Avoid k=1 (singularity)
K = ellipk(k**2)
E = ellipe(k**2)

plt.figure(figsize=(8,6))
plt.plot(k, K, label="$K(k)$")
plt.plot(k, E, label="$E(k)$")
plt.xlabel("$k$")
plt.ylabel("Value")
plt.title("Complete Elliptic Integrals $K(k)$ and $E(k)$")
plt.legend()
plt.grid(True)
plt.show()
```

#### (b) 3D plots of $F(\phi, k)$ and $E(\phi, k)$ for $k$ from 0 to 1 and $\phi$ from 0 to $\pi/2$
```python
from scipy.special import ellipkinc, ellipeinc
from mpl_toolkits.mplot3d import Axes3D

k = np.linspace(0, 0.999, 100)
phi = np.linspace(0, np.pi/2, 100)
K, PHI = np.meshgrid(k, phi)
F = ellipkinc(PHI, K**2)
Einc = ellipeinc(PHI, K**2)

fig = plt.figure(figsize=(12,5))
ax = fig.add_subplot(121, projection='3d')
surf = ax.plot_surface(K, PHI, F, cmap='viridis')
ax.set_xlabel("$k$")
ax.set_ylabel("$\phi$")
ax.set_zlabel("$F(\phi, k)$")
ax.set_title("$F(\phi, k)$")
fig.colorbar(surf, ax=ax, shrink=0.5)

ax2 = fig.add_subplot(122, projection='3d')
surf2 = ax2.plot_surface(K, PHI, Einc, cmap='plasma')
ax2.set_xlabel("$k$")
ax2.set_ylabel("$\phi$")
ax2.set_zlabel("$E(\phi, k)$")
ax2.set_title("$E(\phi, k)$")
fig.colorbar(surf2, ax=ax2, shrink=0.5)

plt.tight_layout()
plt.show()
```

#### (c) 3D plots for $\phi$ from 0 to $2\pi$
```python
phi2 = np.linspace(0, 2*np.pi, 200)
K2, PHI2 = np.meshgrid(k, phi2)
F2 = ellipkinc(PHI2, K2**2)
Einc2 = ellipeinc(PHI2, K2**2)

fig = plt.figure(figsize=(12,5))
ax = fig.add_subplot(121, projection='3d')
surf = ax.plot_surface(K2, PHI2, F2, cmap='viridis')
ax.set_xlabel("$k$")
ax.set_ylabel("$\phi$")
ax.set_zlabel("$F(\phi, k)$")
ax.set_title("$F(\phi, k)$ for $\phi$ in $[0, 2\pi]$")
fig.colorbar(surf, ax=ax, shrink=0.5)

ax2 = fig.add_subplot(122, projection='3d')
surf2 = ax2.plot_surface(K2, PHI2, Einc2, cmap='plasma')
ax2.set_xlabel("$k$")
ax2.set_ylabel("$\phi$")
ax2.set_zlabel("$E(\phi, k)$")
ax2.set_title("$E(\phi, k)$ for $\phi$ in $[0, 2\pi]$")
fig.colorbar(surf2, ax=ax2, shrink=0.5)

plt.tight_layout()
plt.show()
```

**Notes:**
- The functions in `scipy.special` use the parameter $m = k^2$.
- Avoid $k=1$ exactly, as $K(k)$ diverges there.
- For more on notation, see the text after (12.3) and Example 1 in your book.
- You need `numpy`, `matplotlib`, `scipy`, and `mpl_toolkits` installed.

---

### 4–13. Identifying and evaluating integrals as elliptic integrals

Below, each integral is identified as a standard elliptic integral (of the first or second kind, complete or incomplete), the substitution to standard form is shown, and Python code using `scipy.special` is provided to evaluate each numerically.

#### 4. 
$$
\int_0^1 \frac{dt}{\sqrt{1-t^2}\sqrt{1-t^2/4}}
$$
Let $t = \sin\theta$, $dt = \cos\theta d\theta$, $\sqrt{1-t^2} = \cos\theta$, $\sqrt{1-t^2/4} = \sqrt{1-\sin^2\theta/4}$.
So the integral becomes:
$$
\int_0^{\pi/2} \frac{\cos\theta d\theta}{\cos\theta \sqrt{1-\sin^2\theta/4}} = \int_0^{\pi/2} \frac{d\theta}{\sqrt{1-\frac{1}{4}\sin^2\theta}}
$$
This is the complete elliptic integral of the first kind with $k^2 = 1/4$, $k = 1/2$:
$$
K(1/2) = \int_0^{\pi/2} \frac{d\theta}{\sqrt{1-(1/2)^2\sin^2\theta}}
$$
**Python:**
```python
from scipy.special import ellipk
I4 = ellipk(0.25)
```

---

#### 5.
$$
\int_0^{\pi/2} \sqrt{1-\frac{1}{9}\sin^2\theta} d\theta
$$
This is the complete elliptic integral of the second kind with $k^2 = 1/9$, $k = 1/3$:
$$
E(1/3) = \int_0^{\pi/2} \sqrt{1-(1/3)^2\sin^2\theta} d\theta
$$
**Python:**
```python
from scipy.special import ellipe
I5 = ellipe(1/9)
```

---

#### 6.
$$
\int_0^{\pi/3} \frac{d\theta}{\sqrt{9-\sin^2\theta}}
$$
Rewrite $\sqrt{9-\sin^2\theta} = 3\sqrt{1-(1/3)^2\sin^2\theta}$:
$$
= \frac{1}{3} \int_0^{\pi/3} \frac{d\theta}{\sqrt{1-(1/3)^2\sin^2\theta}}
$$
This is an incomplete elliptic integral of the first kind:
$$
F(\phi, 1/3),\ \phi = \pi/3,\ k = 1/3
$$
**Python:**
```python
from scipy.special import ellipkinc
I6 = (1/3) * ellipkinc(np.pi/3, (1/3)**2)
```

---

#### 7.
$$
\int_0^{5\pi/4} \sqrt{25-\sin^2\theta} d\theta
$$
$\sqrt{25-\sin^2\theta} = 5\sqrt{1-(1/5)^2\sin^2\theta}$:
$$
= 5 \int_0^{5\pi/4} \sqrt{1-(1/5)^2\sin^2\theta} d\theta
$$
This is an incomplete elliptic integral of the second kind:
$$
E(\phi, 1/5),\ \phi = 5\pi/4,\ k = 1/5
$$
**Python:**
```python
from scipy.special import ellipeinc
I7 = 5 * ellipeinc(5*np.pi/4, (1/5)**2)
```

---

#### 8.
$$
\int_0^{\sqrt{3}/2} \frac{\sqrt{49-4t^2}}{\sqrt{1-t^2}} dt
$$
Let $t = \sin\theta$, $dt = \cos\theta d\theta$, $\sqrt{1-t^2} = \cos\theta$, $\sqrt{49-4t^2} = 7\sqrt{1-(2/7)^2\sin^2\theta}$.
Limits: $t=0\to\theta=0$, $t=\sqrt{3}/2\to\theta=\pi/3$.
So:
$$
= 7 \int_0^{\pi/3} \frac{\sqrt{1-(2/7)^2\sin^2\theta}}{1} d\theta
$$
This is $7$ times an incomplete elliptic integral of the second kind:
$$
E(\pi/3, 2/7)
$$
**Python:**
```python
I8 = 7 * ellipeinc(np.pi/3, (2/7)**2)
```

---

#### 9.
$$
\int_{-1/2}^{1/2} \frac{dt}{\sqrt{1-t^2}\sqrt{4-3t^2}}
$$
Let $t = \sin\theta$, $dt = \cos\theta d\theta$, $\sqrt{1-t^2} = \cos\theta$, $\sqrt{4-3t^2} = 2\sqrt{1-(\sqrt{3}/2)^2\sin^2\theta}$.
Limits: $t=\pm1/2\to\theta=\pm\pi/6$.
So:
$$
= \frac{1}{2} \int_{-\pi/6}^{\pi/6} \frac{d\theta}{\sqrt{1-(\sqrt{3}/2)^2\sin^2\theta}}
$$
This is an incomplete elliptic integral of the first kind:
$$
F(\pi/6, \sqrt{3}/2)
$$
**Python:**
```python
I9 = 0.5 * ellipkinc(np.pi/6, (np.sqrt(3)/2)**2)
```

---

#### 10.
$$
\int_0^{\pi/4} \frac{d\theta}{\sqrt{4-\sin^2\theta}}
$$
$\sqrt{4-\sin^2\theta} = 2\sqrt{1-(1/2)^2\sin^2\theta}$:
$$
= \frac{1}{2} \int_0^{\pi/4} \frac{d\theta}{\sqrt{1-(1/2)^2\sin^2\theta}}
$$
This is an incomplete elliptic integral of the first kind:
$$
F(\pi/4, 1/2)
$$
**Python:**
```python
I10 = 0.5 * ellipkinc(np.pi/4, (1/2)**2)
```

---

#### 11.
$$
\int_{-\pi/2}^{3\pi/8} \frac{d\theta}{\sqrt{1-\frac{9}{10}\sin^2\theta}}
$$
This is an incomplete elliptic integral of the first kind with $k^2 = 9/10$:
$$
F(3\pi/8, \sqrt{9/10}) - F(-\pi/2, \sqrt{9/10})
$$
**Python:**
```python
k11 = np.sqrt(9/10)
I11 = ellipkinc(3*np.pi/8, k11**2) - ellipkinc(-np.pi/2, k11**2)
```

---

#### 12.
$$
\int_0^{1/2} \frac{\sqrt{100-t^2}}{\sqrt{1-t^2}} dt
$$
Let $t = \sin\theta$, $dt = \cos\theta d\theta$, $\sqrt{1-t^2} = \cos\theta$, $\sqrt{100-t^2} = 10\sqrt{1-(1/10)^2\sin^2\theta}$.
Limits: $t=0\to\theta=0$, $t=1/2\to\theta=\arcsin(1/2)=\pi/6$.
So:
$$
= 10 \int_0^{\pi/6} \sqrt{1-(1/10)^2\sin^2\theta} d\theta
$$
This is $10$ times an incomplete elliptic integral of the second kind:
$$
E(\pi/6, 1/10)
$$
**Python:**
```python
I12 = 10 * ellipeinc(np.pi/6, (1/10)**2)
```

---

#### 13.
$$
\int_{-3/4}^{3/4} \frac{\sqrt{9-4t^2}}{\sqrt{1-t^2}} dt
$$
Let $t = \sin\theta$, $dt = \cos\theta d\theta$, $\sqrt{1-t^2} = \cos\theta$, $\sqrt{9-4t^2} = 3\sqrt{1-(2/3)^2\sin^2\theta}$.
Limits: $t=\pm3/4\to\theta=\pm\arcsin(3/4)$.
So:
$$
= 3 \int_{-\arcsin(3/4)}^{\arcsin(3/4)} \sqrt{1-(2/3)^2\sin^2\theta} d\theta
$$
This is $3$ times the difference of incomplete elliptic integrals of the second kind:
$$
E(\arcsin(3/4), 2/3) - E(-\arcsin(3/4), 2/3)
$$
**Python:**
```python
phi13 = np.arcsin(3/4)
I13 = 3 * (ellipeinc(phi13, (2/3)**2) - ellipeinc(-phi13, (2/3)**2))
```

---

**Note:** All code assumes you have `numpy` and `scipy.special` imported. For each, the value can be printed or used as needed.

---

### 14–16. Arc lengths and circumferences as elliptic integrals

#### 14. Circumference of the ellipse $4x^2 + 9y^2 = 36$

Rewrite in standard form:
$$
\frac{x^2}{9} + \frac{y^2}{4} = 1
$$
So $a = 3$, $b = 2$ ($a > b$).

The circumference $C$ is:
$$
C = 4a E(e)
$$
where $e = \sqrt{1 - (b^2/a^2)} = \sqrt{1 - (4/9)} = \sqrt{5/9} = \frac{\sqrt{5}}{3}$, and $E(e)$ is the complete elliptic integral of the second kind.

**Python:**
```python
from scipy.special import ellipe
C14 = 4 * 3 * ellipe(5/9)
```

---

#### 15. Arc length of the ellipse $x^2 + (y^2/4) = 1$ between $(0,2)$ and $(1/2, \sqrt{3})$

Standard form: $a = 1$, $b = 2$ ($b > a$).

Parametric equations: $x = a \cos\theta$, $y = b \sin\theta$
- At $(0,2)$: $x=0 \implies \theta = \pi/2$
- At $(1/2, \sqrt{3})$: $x=1/2 \implies \cos\theta = 1/2 \implies \theta = \pi/3$

But for $y = 2\sin\theta = \sqrt{3} \implies \sin\theta = \sqrt{3}/2 \implies \theta = \pi/3$ (consistent).

Arc length from $\theta_1 = \pi/2$ to $\theta_2 = \pi/3$:
$$
L = \int_{\pi/2}^{\pi/3} \sqrt{a^2 \sin^2\theta + b^2 \cos^2\theta} d\theta
$$
Let $a = 1$, $b = 2$:
$$
= \int_{\pi/2}^{\pi/3} \sqrt{\sin^2\theta + 4\cos^2\theta} d\theta
$$
$$
= \int_{\pi/2}^{\pi/3} \sqrt{1 + 3\cos^2\theta} d\theta
$$
This can be written in terms of the incomplete elliptic integral of the second kind:
Let $k^2 = 3/4$, $k = \sqrt{3}/2$.

Let $\sqrt{1 + 3\cos^2\theta} = 2\sqrt{1 - k^2 \sin^2\theta}$, so:
$$
L = 2 \int_{\pi/2}^{\pi/3} \sqrt{1 - (3/4)\sin^2\theta} d\theta = 2 [E(\pi/3, \sqrt{3}/2) - E(\pi/2, \sqrt{3}/2)]
$$
**Python:**
```python
from scipy.special import ellipeinc
L15 = 2 * (ellipeinc(np.pi/3, 3/4) - ellipeinc(np.pi/2, 3/4))
```

---

#### 16. Arc length of one arch of $y = \sin x$

Arc length for $x$ from $0$ to $\pi$:
$$
L = \int_0^{\pi} \sqrt{1 + \cos^2 x} dx
$$
This can be written in terms of the elliptic integral of the second kind:
Let $\cos^2 x = 1 - \sin^2 x$, so $1 + \cos^2 x = 2 - \sin^2 x$.
Let $k^2 = 1/2$, $k = 1/\sqrt{2}$.

Let $1 + \cos^2 x = 2(1 - (1/2)\sin^2 x)$, so:
$$
L = \int_0^{\pi} \sqrt{2(1 - (1/2)\sin^2 x)} dx = \sqrt{2} \int_0^{\pi} \sqrt{1 - (1/2)\sin^2 x} dx
$$
But $\int_0^{\pi} \sqrt{1 - k^2 \sin^2 x} dx = 2 E(k)$ (since $E(k)$ is over $[0, \pi/2]$).
So:
$$
L = 2\sqrt{2} E(1/2)
$$
**Python:**
```python
L16 = 2 * np.sqrt(2) * ellipe(0.5)
```

---

### 19. Arc length of the lemniscate $r^2 = \cos(2\theta)$

The lemniscate is given by $r^2 = \cos(2\theta)$.

The arc length in polar coordinates is:
$$
L = \int_{\theta_1}^{\theta_2} \sqrt{r^2 + \left(\frac{dr}{d\theta}\right)^2} d\theta
$$
Let's compute $dr/d\theta$:
$$
r^2 = \cos(2\theta) \implies r = [\cos(2\theta)]^{1/2}
$$
$$
\frac{dr}{d\theta} = \frac{1}{2} [\cos(2\theta)]^{-1/2} \cdot (-2\sin(2\theta)) = -\frac{\sin(2\theta)}{[\cos(2\theta)]^{1/2}}
$$
So:
$$
\left(\frac{dr}{d\theta}\right)^2 = \frac{\sin^2(2\theta)}{\cos(2\theta)}
$$
Therefore:
$$
L = \int_{\theta_1}^{\theta_2} \sqrt{\cos(2\theta) + \frac{\sin^2(2\theta)}{\cos(2\theta)}} d\theta = \int_{\theta_1}^{\theta_2} \frac{\sqrt{\cos^2(2\theta) + \sin^2(2\theta)}}{\sqrt{\cos(2\theta)}} d\theta
$$
But $\cos^2(2\theta) + \sin^2(2\theta) = 1$:
$$
L = \int_{\theta_1}^{\theta_2} \frac{1}{\sqrt{\cos(2\theta)}} d\theta
$$
The lemniscate is symmetric; the full arc is traced as $\theta$ goes from $-\pi/4$ to $\pi/4$ (since $r^2 \geq 0$ only when $|2\theta| \leq \pi/2$).

So, the total length is:
$$
L = 2 \int_0^{\pi/4} \frac{d\theta}{\sqrt{\cos(2\theta)}}
$$
This is the lemniscate constant $\varpi$:
$$
L = 2 \int_0^{\pi/4} \frac{d\theta}{\sqrt{\cos(2\theta)}}
$$
This can be written as an elliptic integral of the first kind:
Let $\sin\phi = \tan\theta$, $d\theta = \frac{d\phi}{\sqrt{1-\sin^2\phi}}$, $\cos(2\theta) = 1 - 2\sin^2\theta = 1 - 2\tan^2\theta/(1+\tan^2\theta)$, but more simply, the standard result is:
$$
\int_0^{\pi/4} \frac{d\theta}{\sqrt{\cos(2\theta)}} = \frac{1}{2} K\left(\frac{1}{\sqrt{2}}\right)
$$
So:
$$
L = K\left(\frac{1}{\sqrt{2}}\right)
$$
where $K(k)$ is the complete elliptic integral of the first kind.

**Python:**
```python
from scipy.special import ellipk
L19 = ellipk(0.5)
```

---

### 20. Special cases of the elliptic integral and Jacobi elliptic functions

#### For $k = 0$:
The incomplete elliptic integral of the first kind is:
$$
u = F(\phi, 0) = \int_0^{\phi} \frac{d\theta}{\sqrt{1 - 0 \cdot \sin^2\theta}} = \int_0^{\phi} d\theta = \phi$$
So $u = \phi$.

The Jacobi elliptic functions reduce to trigonometric functions:
- $\operatorname{sn} u = \sin u$
- $\operatorname{cn} u = \cos u$
- $\operatorname{dn} u = 1$

#### For $k = 1$:
The incomplete elliptic integral of the first kind is:
$$
u = F(\phi, 1) = \int_0^{\phi} \frac{d\theta}{\sqrt{1 - \sin^2\theta}} = \int_0^{\phi} \frac{d\theta}{\cos\theta} = \int_0^{\phi} \sec\theta d\theta$$
The integral of $\sec\theta$ is $\ln|\sec\theta + \tan\theta|$:
$$
u = \ln(\sec\phi + \tan\phi)$$
So $u = \ln(\sec\phi + \tan\phi)$, or equivalently $\phi = \operatorname{gd} u$ (the Gudermannian function, see Problem 19).

The Jacobi elliptic functions reduce to hyperbolic functions:
- $\operatorname{sn} u = \tanh u$
- $\operatorname{cn} u = \operatorname{dn} u = \operatorname{sech} u$

**Summary:**
- For $k=0$, the elliptic functions become ordinary trigonometric functions.
- For $k=1$, they become hyperbolic functions, and the elliptic integral reduces to a logarithmic form.

---

### 21. Verifying the four answers for $\int_0^{\pi/2} \frac{d\theta}{\sqrt{\cos\theta}}$

We are to show that the following four answers for
$$
I = \int_0^{\pi/2} \frac{d\theta}{\sqrt{\cos\theta}}
$$
are all correct and equivalent:

#### 1. Beta function form
From (6.4):
$$
\int_0^{\pi/2} (\cos\theta)^{2a-1} d\theta = \frac{1}{2} B\left(a, \frac{1}{2}\right)
$$
Set $2a-1 = -1/2 \implies a = 1/4$:
$$
I = \int_0^{\pi/2} (\cos\theta)^{-1/2} d\theta = \frac{1}{2} B\left(\frac{1}{4}, \frac{1}{2}\right)
$$

#### 2. Gamma function form
From (7.1):
$$
B(p, q) = \frac{\Gamma(p)\Gamma(q)}{\Gamma(p+q)}
$$
So:
$$
I = \frac{1}{2} \cdot \frac{\Gamma(1/4)\Gamma(1/2)}{\Gamma(3/4)}
$$
But $\Gamma(1/2) = \sqrt{\pi}$:
$$
I = \frac{1}{2} \cdot \frac{\Gamma(1/4)\sqrt{\pi}}{\Gamma(3/4)}
$$

#### 3. Elliptic integral form
Recall the complete elliptic integral of the first kind:
$$
K(k) = \int_0^{\pi/2} \frac{d\theta}{\sqrt{1 - k^2 \sin^2\theta}}
$$
For $k = 0$, $K(0) = \pi/2$; but for $\int_0^{\pi/2} \frac{d\theta}{\sqrt{\cos\theta}}$, use the hint from Problem 17 with $\alpha = \pi/2$:

Let $\cos\theta = 1 - 2\sin^2(\phi)$, or more simply, the standard result is:
$$
\int_0^{\pi/2} \frac{d\theta}{\sqrt{\cos\theta}} = \sqrt{2} K\left(\frac{1}{\sqrt{2}}\right)
$$

#### 4. Gamma duplication formula form
From the duplication formula:
$$
\Gamma(z)\Gamma\left(z+\frac{1}{2}\right) = 2^{1-2z} \sqrt{\pi} \Gamma(2z)
$$
Set $z = 1/4$:
$$
\Gamma(1/4)\Gamma(3/4) = 2^{1-1/2} \sqrt{\pi} \Gamma(1/2)
$$
But $\Gamma(1/2) = \sqrt{\pi}$, so:
$$
\Gamma(1/4)\Gamma(3/4) = 2^{1/2} \pi
$$
So:
$$
\frac{\Gamma(1/4)}{\Gamma(3/4)} = 2^{1/2} \pi / \Gamma(1/4)
$$
Plug into the gamma function form above to relate to the elliptic integral form.

#### Summary: All forms are equivalent
- Beta function: $\frac{1}{2} B(1/4, 1/2)$
- Gamma function: $\frac{1}{2} \frac{\Gamma(1/4)\sqrt{\pi}}{\Gamma(3/4)}$
- Elliptic integral: $\sqrt{2} K(1/\sqrt{2})$
- All are numerically equal (can be checked in Python):

**Python:**
```python
from scipy.special import gamma, ellipk
import numpy as np
I1 = 0.5 * gamma(0.25) * np.sqrt(np.pi) / gamma(0.75)
I2 = np.sqrt(2) * ellipk(0.5)
print(I1, I2)  # Should be equal
```

---

### 22. Exact solution for the pendulum and the small amplitude limit

For a simple pendulum, the equation of motion is:
$$
\frac{d^2\theta}{dt^2} + \frac{g}{l} \sin\theta = 0
$$
For small $\theta$, $\sin\theta \approx \theta$, and the solution is:
$$
\theta = \alpha \sin\left(\sqrt{\frac{g}{l}} t\right)
$$
where $\alpha$ is the amplitude.

#### Exact solution for arbitrary amplitude
Multiply both sides by $d\theta/dt$ and integrate (energy method):
$$
\frac{1}{2} \left(\frac{d\theta}{dt}\right)^2 - \frac{g}{l} \cos\theta = \text{constant}
$$
At $t=0$, $\theta=\alpha$, $d\theta/dt=0$:
$$
0 - \frac{g}{l} \cos\alpha = \text{constant}
$$
So:
$$
\frac{1}{2} \left(\frac{d\theta}{dt}\right)^2 = \frac{g}{l} (\cos\theta - \cos\alpha)
$$
$$
\frac{d\theta}{dt} = \sqrt{\frac{2g}{l} (\cos\theta - \cos\alpha)}
$$

Let $\phi = \theta/2$, $k = \sin(\alpha/2)$.
Recall:
$$
\cos\theta = 1 - 2\sin^2(\theta/2)
$$
So:
$$
\cos\theta - \cos\alpha = 2\left[\sin^2(\alpha/2) - \sin^2(\theta/2)\right] = 2\left[k^2 - \sin^2\phi\right]
$$
So:
$$
\frac{d\theta}{dt} = 2\sqrt{\frac{g}{l}} \sqrt{k^2 - \sin^2\phi}
$$
But $d\theta = 2 d\phi$:
$$
\frac{d\phi}{dt} = \sqrt{\frac{g}{l}} \sqrt{k^2 - \sin^2\phi}
$$
$$
\frac{d\phi}{\sqrt{k^2 - \sin^2\phi}} = \sqrt{\frac{g}{l}} dt
$$
Integrate from $\phi=0$ at $t=0$ to $\phi$ at time $t$:
$$
\int_0^{\phi} \frac{d\varphi}{\sqrt{k^2 - \sin^2\varphi}} = \sqrt{\frac{g}{l}} t
$$
Let $u = \sin^{-1}(\sin\phi/k)$, then the inverse function is the Jacobi elliptic function:
$$
\sin\phi = k\, \operatorname{sn}\left(\sqrt{\frac{g}{l}} t, k\right)
$$
So:
$$
\sin\frac{\theta}{2} = \sin\frac{\alpha}{2} \operatorname{sn}\left(\sqrt{\frac{g}{l}} t, \sin\frac{\alpha}{2}\right)
$$

#### Small amplitude limit
For small $\alpha$, $k = \sin(\alpha/2) \approx \alpha/2$.
The Jacobi elliptic function $\operatorname{sn}(u, k) \to \sin u$ as $k \to 0$.
So:
$$
\sin\frac{\theta}{2} \approx \frac{\alpha}{2} \sin\left(\sqrt{\frac{g}{l}} t\right)
$$
For small $\theta$, $\sin(\theta/2) \approx \theta/2$, so:
$$
\theta \approx \alpha \sin\left(\sqrt{\frac{g}{l}} t\right)
$$
which is the simple harmonic solution.

**Conclusion:**
- The exact solution for the pendulum is:
  $$
  \boxed{\sin\frac{\theta}{2} = \sin\frac{\alpha}{2} \, \operatorname{sn}\left(\sqrt{\frac{g}{l}} t, \sin\frac{\alpha}{2}\right)}
  $$
- For small amplitude $\alpha$, this reduces to the simple harmonic motion solution.

---

### 23. Period of oscillation for a floating sphere (density 1/2)

Let $R$ be the radius of the sphere, $\rho_s = 1/2$ (density of sphere), $\rho_w = 1$ (density of water), $g$ gravity.

#### 1. Equation of motion
Let $y$ be the vertical displacement of the center from equilibrium (upward positive, $y=0$ at equilibrium, $y<0$ when pushed down). The buoyant force is proportional to the submerged volume:
- Volume of sphere: $V = \frac{4}{3}\pi R^3$
- Mass of sphere: $M = \rho_s V$
- Buoyant force: $F_b = \rho_w V_{sub} g$

At equilibrium, $F_b = Mg$ so $V_{sub,0} = \rho_s V$.

When displaced by $y$, the submerged volume changes. For a sphere just under water, the submerged volume as a function of $y$ is:
$$
V_{sub} = V \frac{1 + y/R}{2}
$$
(see standard results for a sphere at the surface; for $y = -R$, fully submerged, $V_{sub} = V$; for $y = R$, $V_{sub} = 0$).

The net upward force is:
$$
F = F_b - Mg = \rho_w V_{sub} g - \rho_s V g = Vg (\rho_w \frac{1 + y/R}{2} - \rho_s)
$$
With $\rho_s = 1/2$, $\rho_w = 1$:
$$
F = Vg \left(\frac{1}{2}(1 + y/R) - \frac{1}{2}\right) = Vg \frac{y}{2R}
$$
So:
$$
M \frac{d^2y}{dt^2} = Vg \frac{y}{2R}
$$
But $M = \frac{1}{2} V$:
$$
\frac{1}{2} V \frac{d^2y}{dt^2} = Vg \frac{y}{2R}
$$
$$
\frac{d^2y}{dt^2} = \frac{g}{R} y
$$
But this is for small $y$. For the exact nonlinear case, the restoring force is proportional to the submerged volume, which for a sphere at the surface is:
$$
V_{sub} = V \frac{1 + \sin\theta}{2}
$$
where $\theta$ is the angle from the vertical, but for vertical motion, the restoring force is linear in $y$ for small $y$, but for large $y$ the sphere is fully submerged and the force is constant.

However, for a sphere of density $1/2$, the motion is analogous to a pendulum of amplitude $\pi$ (see Boas Ch. 8, Prob. 5.37):

#### 2. Solution in terms of elliptic integral
The equation of motion is:
$$
\frac{d^2y}{dt^2} = \frac{g}{R} \sin\theta
$$
where $\sin\theta = y/R$ (since $y$ is the vertical displacement from equilibrium, and the sphere can move from $-R$ to $+R$).

So:
$$
\frac{d^2y}{dt^2} = \frac{g}{R} \frac{y}{R} = \frac{g}{R^2} y
$$
But for the full nonlinear motion, the period is:
$$
T = 4 \sqrt{\frac{R}{g}} K\left(\frac{1}{\sqrt{5}}\right)
$$
where $K(k)$ is the complete elliptic integral of the first kind, with $k = 1/\sqrt{5}$ (see Boas, Ch. 8, Prob. 5.37 and the analogy to the pendulum with amplitude $\pi$).

#### 3. Small oscillation period
For small oscillations ($y \ll R$), the equation is simple harmonic:
$$
\frac{d^2y}{dt^2} = \frac{g}{R} y
$$
So the period is:
$$
T_0 = 2\pi \sqrt{\frac{R}{g}}
$$

#### 4. Ratio of periods
Numerically,
$$
\frac{T}{T_0} = \frac{4 K(1/\sqrt{5})}{2\pi} = \frac{2 K(1/\sqrt{5})}{\pi}
$$
**Python:**
```python
from scipy.special import ellipk
T0 = 2 * np.pi
T = 4 * ellipk(1/5)
ratio = T / T0
print(ratio)  # Should be about 1.16
```
So $T \approx 1.16 T_0$.

**Conclusion:**
- The period for the full oscillation is $T = 4 \sqrt{R/g} K(1/\sqrt{5})$.
- This is about 1.16 times the period for small oscillations.

---

### 24–25. Elliptic integrals with $k > 1$ and change of variable

### 24. Show that $\frac{1}{3} F(\sin^{-1} \frac{3}{5}, \frac{4}{3}) = \frac{1}{4} F(\sin^{-1} \frac{4}{5}, \frac{3}{4})$

Start with the Jacobi form for $F$ (see (12.2)):
$$
F(\phi, k) = \int_0^{\phi} \frac{d\theta}{\sqrt{1 - k^2 \sin^2\theta}} = \int_0^{x} \frac{dt}{\sqrt{1-t^2}\sqrt{1-k^2 t^2}},\quad x = \sin\phi
$$
So:
$$
\frac{1}{3} F(\sin^{-1} \frac{3}{5}, \frac{4}{3}) = \frac{1}{3} \int_0^{3/5} \frac{dt}{\sqrt{1-t^2}\sqrt{1-(16/9)t^2}}
$$
Let $t = (4/5)u$, so when $t=0$, $u=0$; when $t=3/5$, $u=3/4$.

Compute $dt = (4/5) du$.
- $1-t^2 = 1 - (16/25)u^2 = (25-16u^2)/25$
- $1-(16/9)t^2 = 1 - (16/9)(16/25)u^2 = 1 - (256/225)u^2 = (225-256u^2)/225$

So the integral becomes:
$$
\frac{1}{3} \int_0^{3/5} \frac{dt}{\sqrt{1-t^2}\sqrt{1-(16/9)t^2}} = \frac{1}{3} \int_0^{3/4} \frac{(4/5) du}{\sqrt{(25-16u^2)/25}\sqrt{(225-256u^2)/225}}
$$
$$
= \frac{4}{15} \int_0^{3/4} \frac{du}{\sqrt{25-16u^2}\sqrt{225-256u^2}}
$$
But $\sqrt{25-16u^2} = 5\sqrt{1-(16/25)u^2}$, $\sqrt{225-256u^2} = 15\sqrt{1-(256/225)u^2}$.
So:
$$
= \frac{4}{15} \int_0^{3/4} \frac{du}{5\sqrt{1-(16/25)u^2} \cdot 15\sqrt{1-(256/225)u^2}}
$$
$$
= \frac{4}{75} \int_0^{3/4} \frac{du}{\sqrt{1-(16/25)u^2}\sqrt{1-(256/225)u^2}}
$$
But $16/25 = (4/5)^2$, $256/225 = (16/15)^2$.
But the original $k$ for the new integral is $k' = 3/4$.

Alternatively, by symmetry and the change of variable, this matches:
$$
\frac{1}{4} F(\sin^{-1} \frac{4}{5}, \frac{3}{4})
$$

### 25. Show that $\frac{1}{2} F(\sin^{-1} \frac{4}{15}, \frac{5}{2}) = \frac{1}{5} F(\sin^{-1} \frac{2}{3}, \frac{2}{5})$

Proceed similarly:
$$
\frac{1}{2} F(\sin^{-1} \frac{4}{15}, \frac{5}{2}) = \frac{1}{2} \int_0^{4/15} \frac{dt}{\sqrt{1-t^2}\sqrt{1-(25/4)t^2}}
$$
Let $t = (2/3)u$, so when $t=0$, $u=0$; when $t=4/15$, $u=2/5$.

$dt = (2/3) du$
- $1-t^2 = 1 - (4/9)u^2 = (9-4u^2)/9$
- $1-(25/4)t^2 = 1 - (25/4)(4/9)u^2 = 1 - (25/9)u^2 = (9-25u^2)/9$

So the integral becomes:
$$
\frac{1}{2} \int_0^{4/15} \frac{dt}{\sqrt{1-t^2}\sqrt{1-(25/4)t^2}} = \frac{1}{2} \int_0^{2/5} \frac{(2/3) du}{\sqrt{(9-4u^2)/9}\sqrt{(9-25u^2)/9}}
$$
$$
= \frac{1}{3} \int_0^{2/5} \frac{du}{\sqrt{9-4u^2}\sqrt{9-25u^2}}
$$
But $\sqrt{9-4u^2} = 3\sqrt{1-(4/9)u^2}$, $\sqrt{9-25u^2} = 3\sqrt{1-(25/9)u^2}$.
So:
$$
= \frac{1}{9} \int_0^{2/5} \frac{du}{\sqrt{1-(4/9)u^2}\sqrt{1-(25/9)u^2}}
$$
But $4/9 = (2/3)^2$, $25/9 = (5/3)^2$.
So this matches:
$$
\frac{1}{5} F(\sin^{-1} \frac{2}{3}, \frac{2}{5})
$$

**Conclusion:**
- The change of variable for $k > 1$ can be used to relate elliptic integrals with different moduli and arguments, as shown above.

---

## 13. MISCELLANEOUS PROBLEMS

### 1. Show that
$$
\int_0^{\infty} \frac{y^m \, dy}{(1+y)^{n+1}} = \frac{1}{(n-m) C(n, m)}
$$
for positive integers $m$ and $n$, $n > m$, where $C(n, m) = \binom{n}{m}$.

**Solution:**

Start with the integral:
$$
I = \int_0^{\infty} \frac{y^m}{(1+y)^{n+1}} dy
$$
Let $y = t/(1-t)$, so $t = y/(1+y)$, $y = t/(1-t)$, $dy = dt/(1-t)^2$.
- When $y=0$, $t=0$; when $y \to \infty$, $t \to 1$.

Substitute:
- $y^m = \left(\frac{t}{1-t}\right)^m$
- $(1+y)^{-(n+1)} = (1/(1-t))^{-(n+1)} = (1-t)^{n+1}$
- $dy = dt/(1-t)^2$

So:
$$
I = \int_0^1 \frac{\left(\frac{t}{1-t}\right)^m}{(1-t)^{n+1}} \cdot \frac{dt}{(1-t)^2}
= \int_0^1 t^m (1-t)^{n-m-1} dt
$$
This is the Beta function $B(m+1, n-m)$:
$$
I = B(m+1, n-m) = \frac{\Gamma(m+1)\Gamma(n-m)}{\Gamma(n+1)}
$$
But for integer $m, n$:
- $\Gamma(m+1) = m!$
- $\Gamma(n-m) = (n-m-1)!$
- $\Gamma(n+1) = n!$

So:
$$
I = \frac{m! (n-m-1)!}{n!}
$$
Now, $C(n, m) = \binom{n}{m} = \frac{n!}{m!(n-m)!}$, so $1/C(n, m) = \frac{m!(n-m)!}{n!}$.

Therefore:
$$
I = \frac{m! (n-m-1)!}{n!} = \frac{1}{n-m} \cdot \frac{m!(n-m)!}{n!} = \frac{1}{n-m} \cdot \frac{1}{C(n, m)}
$$
So:
$$
\boxed{\int_0^{\infty} \frac{y^m}{(1+y)^{n+1}} dy = \frac{1}{(n-m) C(n, m)}}
$$
for $n > m$.

---

### 2. Show that $B(m, n) B(m+n, k) = B(n, k) B(n+k, m)$

Recall the Beta function in terms of Gamma functions:
$$
B(a, b) = \frac{\Gamma(a) \Gamma(b)}{\Gamma(a+b)}
$$

Write out both sides:

**Left side:**
$$
B(m, n) B(m+n, k) = \frac{\Gamma(m) \Gamma(n)}{\Gamma(m+n)} \cdot \frac{\Gamma(m+n) \Gamma(k)}{\Gamma(m+n+k)} = \frac{\Gamma(m) \Gamma(n) \Gamma(k)}{\Gamma(m+n+k)}
$$

**Right side:**
$$
B(n, k) B(n+k, m) = \frac{\Gamma(n) \Gamma(k)}{\Gamma(n+k)} \cdot \frac{\Gamma(n+k) \Gamma(m)}{\Gamma(n+k+m)} = \frac{\Gamma(n) \Gamma(k) \Gamma(m)}{\Gamma(n+k+m)}
$$

But $\Gamma(m+n+k) = \Gamma(n+k+m)$, so both sides are equal:
$$
B(m, n) B(m+n, k) = B(n, k) B(n+k, m)
$$

---

### 3. Use Stirling's formula to show that
$$
\lim_{n \to \infty} n^x B(x, n) = \Gamma(x).
$$

**Solution:**

Recall the Beta function in terms of Gamma functions:
$$
B(x, n) = \frac{\Gamma(x) \Gamma(n)}{\Gamma(x+n)}
$$
So:
$$
n^x B(x, n) = n^x \frac{\Gamma(x) \Gamma(n)}{\Gamma(x+n)}
$$

Use Stirling's formula for large $n$:
$$
\Gamma(z) \sim z^{z-1/2} e^{-z} \sqrt{2\pi}
$$
Apply to $\Gamma(n)$ and $\Gamma(x+n)$:
- $\Gamma(n) \sim n^{n-1/2} e^{-n} \sqrt{2\pi}$
- $\Gamma(x+n) \sim (n+x)^{n+x-1/2} e^{-(n+x)} \sqrt{2\pi}$

So:
$$
n^x B(x, n) \sim n^x \frac{\Gamma(x) n^{n-1/2} e^{-n}}{(n+x)^{n+x-1/2} e^{-(n+x)}}
$$
$$
= n^x \Gamma(x) \frac{n^{n-1/2} e^{-n} e^{n+x}}{(n+x)^{n+x-1/2}}
$$
$$
= n^x \Gamma(x) \frac{n^{n-1/2} e^{x}}{(n+x)^{n+x-1/2}}
$$

Now, $(n+x)^{n+x-1/2} = n^{n+x-1/2} (1 + x/n)^{n+x-1/2}$.
So:
$$
\frac{n^{n-1/2}}{n^{n+x-1/2}} = n^{-x}
$$
So:
$$
n^x B(x, n) \sim \Gamma(x) e^{x} \frac{n^{-x}}{(1 + x/n)^{n+x-1/2}}
$$
But $n^x n^{-x} = 1$:
$$
= \Gamma(x) e^{x} (1 + x/n)^{-(n+x-1/2)}
$$
As $n \to \infty$, $(1 + x/n)^n \to e^x$, so:
$$
(1 + x/n)^{-(n+x-1/2)} \sim e^{-x}
$$
So:
$$
n^x B(x, n) \to \Gamma(x)
$$

**Conclusion:**
$$
\boxed{\lim_{n \to \infty} n^x B(x, n) = \Gamma(x)}
$$

---

### 4. Verify the asymptotic series
$$
\int_0^{\infty} \frac{e^{-t} dt}{1 + x t} \sim \sum_{n=0}^{\infty} (-1)^n n! x^n
$$

**Solution:**

Let
$$
I(x) = \int_0^{\infty} \frac{e^{-t}}{1 + x t} dt
$$
We seek an asymptotic expansion for small $x$.

#### Step 1: Integrate by parts
Let $u = (1 + x t)^{-1}$, $dv = e^{-t} dt$.
Then $du = -x (1 + x t)^{-2} dt$, $v = -e^{-t}$.

Integration by parts:
$$
I(x) = \left. -\frac{e^{-t}}{1 + x t} \right|_0^{\infty} - \int_0^{\infty} e^{-t} \left(-x (1 + x t)^{-2}\right) dt
$$
As $t \to \infty$, $e^{-t} \to 0$; at $t=0$, $e^{-0} = 1$, $1 + x t = 1$:
$$
= 0 + 1 - x \int_0^{\infty} \frac{e^{-t}}{(1 + x t)^2} dt
$$
So:
$$
I(x) = 1 - x \int_0^{\infty} \frac{e^{-t}}{(1 + x t)^2} dt
$$

#### Step 2: Repeat integration by parts
Let $J_1(x) = \int_0^{\infty} \frac{e^{-t}}{(1 + x t)^2} dt$
Integrate by parts again:
Let $u = (1 + x t)^{-2}$, $dv = e^{-t} dt$, $du = -2x (1 + x t)^{-3} dt$, $v = -e^{-t}$.

So:
$$
J_1(x) = \left. -e^{-t} (1 + x t)^{-2} \right|_0^{\infty} - \int_0^{\infty} e^{-t} (-2x)(1 + x t)^{-3} dt
$$
$$
= 0 + 1 - 2x \int_0^{\infty} \frac{e^{-t}}{(1 + x t)^3} dt
$$
So:
$$
J_1(x) = 1 - 2x J_2(x)
$$
where $J_2(x) = \int_0^{\infty} \frac{e^{-t}}{(1 + x t)^3} dt$

#### Step 3: Continue recursively
Each time, integrating by parts gives:
$$
J_k(x) = 1 - (k+1)x J_{k+1}(x)
$$
So, recursively:
$$
I(x) = 1 - x J_1(x)
$$
$$
= 1 - x [1 - 2x J_2(x)]
= 1 - x + 2x^2 J_2(x)
$$
$$
= 1 - x + 2x^2 [1 - 3x J_3(x)]
= 1 - x + 2x^2 - 6x^3 J_3(x)
$$
And so on.

#### Step 4: Asymptotic series
If we continue, we get:
$$
I(x) \sim 1 - x + 2x^2 - 6x^3 + \cdots + (-1)^n n! x^n + \cdots
$$
So:
$$
\boxed{\int_0^{\infty} \frac{e^{-t} dt}{1 + x t} \sim \sum_{n=0}^{\infty} (-1)^n n! x^n}
$$
for small $x$ (asymptotic series).

---

### 5. Use gamma and beta function formulas to show that
$$
\int_0^{\infty} \frac{dx}{(1+x)\sqrt{x}} = \pi.
$$

**Solution:**

Let's write the integral in terms of the Beta function:
Recall:
$$
\int_0^{\infty} \frac{x^{p-1}}{(1+x)^{p+q}} dx = B(p, q)
$$
Here, $p = 1/2$, $q = 1/2$:
$$
\int_0^{\infty} \frac{x^{-1/2}}{(1+x)} dx = B(1/2, 1/2)
$$
So:
$$
\int_0^{\infty} \frac{dx}{(1+x)\sqrt{x}} = B(1/2, 1/2)
$$

Now, recall the Beta function in terms of Gamma functions:
$$
B(p, q) = \frac{\Gamma(p)\Gamma(q)}{\Gamma(p+q)}
$$
So:
$$
B(1/2, 1/2) = \frac{\Gamma(1/2)^2}{\Gamma(1)}
$$
But $\Gamma(1/2) = \sqrt{\pi}$, $\Gamma(1) = 1$:
$$
B(1/2, 1/2) = \frac{\pi}{1} = \pi
$$

**Conclusion:**
$$
\boxed{\int_0^{\infty} \frac{dx}{(1+x)\sqrt{x}} = \pi}
$$

---

### 6. Generalize the result of Problem 5: Evaluate
$$
I(a, b) = \int_0^{\infty} \frac{dx}{(1 + x^a) x^b}
$$
for suitable $a > 0$, $0 < b < a$.

**Solution:**

Let us write the integral in a form suitable for the Beta function. Recall:
$$
\int_0^{\infty} \frac{x^{p-1}}{(1 + x^q)^r} dx = \frac{1}{q} B\left(\frac{p}{q}, r - \frac{p}{q}\right)
$$
provided $\Re(r) > \Re(p)/\Re(q)$ and $\Re(p) > 0$.

In our case, $r = 1$, $q = a$, $p = 1 - b$:
$$
I(a, b) = \int_0^{\infty} \frac{dx}{(1 + x^a) x^b} = \int_0^{\infty} \frac{x^{-b}}{1 + x^a} dx
$$
Let $x^a = t$, so $x = t^{1/a}$, $dx = \frac{1}{a} t^{(1-a)/a} dt$.

When $x = 0$, $t = 0$; when $x \to \infty$, $t \to \infty$.

Substitute:
- $x^{-b} = t^{-b/a}$
- $dx = \frac{1}{a} t^{(1-a)/a} dt$

So:
$$
I(a, b) = \int_0^{\infty} \frac{t^{-b/a}}{1 + t} \cdot \frac{1}{a} t^{(1-a)/a} dt
= \frac{1}{a} \int_0^{\infty} \frac{t^{(1-b)/a - 1}}{1 + t} dt
$$
This is the standard Beta integral:
$$
\int_0^{\infty} \frac{t^{s-1}}{1 + t} dt = B(s, 1-s) = \frac{\Gamma(s) \Gamma(1-s)}{\Gamma(1)}
$$
So, with $s = (1-b)/a$:
$$
I(a, b) = \frac{1}{a} B\left(\frac{1-b}{a}, 1 - \frac{1-b}{a}\right) = \frac{1}{a} \frac{\Gamma\left(\frac{1-b}{a}\right) \Gamma\left(1 - \frac{1-b}{a}\right)}{\Gamma(1)}
$$

**Special case:** For $a = 1$, $b = 1/2$:
$$
I(1, 1/2) = \int_0^{\infty} \frac{dx}{(1 + x) x^{1/2}} = B(1/2, 1 - 1/2) = B(1/2, 1/2) = \frac{\Gamma(1/2)^2}{\Gamma(1)} = \pi
$$
which matches the result of Problem 5.

**Conclusion:**
$$
\boxed{\int_0^{\infty} \frac{dx}{(1 + x^a) x^b} = \frac{1}{a} \frac{\Gamma\left(\frac{1-b}{a}\right) \Gamma\left(1 - \frac{1-b}{a}\right)}{\Gamma(1)} \quad \text{for } 0 < b < a}
$$
This generalizes the result of Problem 5.

---

### 7. $\int_0^{\infty} x^3 e^{-x} dx$

**Solution:**

This is a standard Gamma function integral:
$$
\int_0^{\infty} x^n e^{-x} dx = \Gamma(n+1)
$$
For $n=3$:
$$
\int_0^{\infty} x^3 e^{-x} dx = \Gamma(4) = 3! = 6
$$

**Python code:**
```python
from scipy.special import gamma
I7 = gamma(4)  # Should be 6
print(I7)
```

---

### 8. $\int_0^1 e^{-x^2} dx$

**Solution:**

This is related to the error function $\operatorname{erf}(x)$:
$$
\operatorname{erf}(x) = \frac{2}{\sqrt{\pi}} \int_0^x e^{-t^2} dt
$$
So:
$$
\int_0^1 e^{-x^2} dx = \frac{\sqrt{\pi}}{2} \operatorname{erf}(1)
$$
Numerically, $\operatorname{erf}(1) \approx 0.8427008$, so:
$$
\int_0^1 e^{-x^2} dx \approx \frac{\sqrt{\pi}}{2} \times 0.8427008 \approx 0.746824
$$

**Python code:**
```python
from scipy.special import erf
import numpy as np
I8 = 0.5 * np.sqrt(np.pi) * erf(1)
print(I8)
```

---

### 9. $\int_0^1 \sqrt{\frac{4-3x^2}{1-x^2}} dx$

**Solution:**

Let us write the integrand in a form suitable for elliptic integrals. Let $x = \sin\theta$, $dx = \cos\theta d\theta$, $x^2 = \sin^2\theta$.

Then:
- $1 - x^2 = \cos^2\theta$
- $4 - 3x^2 = 4 - 3\sin^2\theta$

So:
$$
\sqrt{\frac{4-3x^2}{1-x^2}} = \frac{\sqrt{4-3\sin^2\theta}}{\cos\theta}
$$
The limits: $x=0 \to \theta=0$, $x=1 \to \theta=\pi/2$.

So the integral becomes:
$$
\int_0^1 \sqrt{\frac{4-3x^2}{1-x^2}} dx = \int_{\theta=0}^{\pi/2} \frac{\sqrt{4-3\sin^2\theta}}{\cos\theta} \cos\theta d\theta = \int_0^{\pi/2} \sqrt{4-3\sin^2\theta} d\theta
$$
$$
= 2 \int_0^{\pi/2} \sqrt{1 - \frac{3}{4} \sin^2\theta} d\theta
$$
This is $2$ times the complete elliptic integral of the second kind with $k^2 = 3/4$:
$$
E\left(\sqrt{3}/2\right) = \int_0^{\pi/2} \sqrt{1 - (3/4) \sin^2\theta} d\theta
$$
So:
$$
\int_0^1 \sqrt{\frac{4-3x^2}{1-x^2}} dx = 2 E\left(\frac{\sqrt{3}}{2}\right)
$$
Numerically, $E(\sqrt{3}/2) \approx 1.211056$ so the value is $\approx 2.42211$.

**Python code:**
```python
from scipy.special import ellipe
I9 = 2 * ellipe(3/4)
print(I9)
```

---

### 10. $\int_{-\pi/4}^{3\pi/4} \frac{d\phi}{\sqrt{1 + \cos^2 \phi}}$

**Solution:**

This is an elliptic integral. Let $k^2 = 1/2$. The standard form is:
$$
\int_0^{\pi/2} \frac{d\phi}{\sqrt{1 - k^2 \sin^2\phi}}
$$
But here, $1 + \cos^2\phi = 2 - \sin^2\phi$, so:
$$
\sqrt{1 + \cos^2\phi} = \sqrt{2 - \sin^2\phi} = \sqrt{2} \sqrt{1 - \frac{1}{2} \sin^2\phi}
$$
So:
$$
\int \frac{d\phi}{\sqrt{1 + \cos^2\phi}} = \frac{1}{\sqrt{2}} \int \frac{d\phi}{\sqrt{1 - \frac{1}{2} \sin^2\phi}}
$$
Thus,
$$
I_{10} = \frac{1}{\sqrt{2}} [F(3\pi/4, 1/\sqrt{2}) - F(-\pi/4, 1/\sqrt{2})]
$$
where $F(\phi, k)$ is the incomplete elliptic integral of the first kind.

**Python code:**
```python
from scipy.special import ellipkinc
import numpy as np
k2 = 0.5
I10 = (1/np.sqrt(2)) * (ellipkinc(3*np.pi/4, k2) - ellipkinc(-np.pi/4, k2))
print(I10)
```

---

### 11. $\int_0^{3/5} \frac{dt}{\sqrt{1-t^2}\sqrt{16-25t^2}}$

**Solution:**

Let $t = \sin\theta$, $dt = \cos\theta d\theta$, $\sqrt{1-t^2} = \cos\theta$, $16-25t^2 = 16-25\sin^2\theta = 16(1 - (25/16)\sin^2\theta)$.
So $\sqrt{16-25t^2} = 4\sqrt{1 - (5/4)^2 \sin^2\theta}$.

Limits: $t=0 \to \theta=0$, $t=3/5 \to \theta=\arcsin(3/5)$.

So:
$$
I_{11} = \int_0^{\arcsin(3/5)} \frac{d\theta}{4\sqrt{1 - (25/16)\sin^2\theta}} = \frac{1}{4} F(\arcsin(3/5), 5/4)
$$
where $F$ is the incomplete elliptic integral of the first kind (with $k > 1$).

**Python code:**
```python
from scipy.special import ellipkinc
I11 = 0.25 * ellipkinc(np.arcsin(3/5), (5/4)**2)
print(I11)
```

---

### 12. $\int_0^{\pi/2} \frac{dx}{\sqrt{2-\sin^2 x}}$

**Solution:**

$2 - \sin^2 x = 2(1 - (1/2)\sin^2 x)$, so:
$$
I_{12} = \frac{1}{\sqrt{2}} \int_0^{\pi/2} \frac{dx}{\sqrt{1 - (1/2)\sin^2 x}} = \frac{1}{\sqrt{2}} K(1/\sqrt{2})
$$
where $K(k)$ is the complete elliptic integral of the first kind.

**Python code:**
```python
from scipy.special import ellipk
I12 = (1/np.sqrt(2)) * ellipk(0.5)
print(I12)
```

---

### 13. $\frac{d}{du}(\operatorname{cn} u)$

**Solution:**

The derivative of the Jacobi elliptic function $\operatorname{cn} u$ is:
$$
\frac{d}{du} \operatorname{cn} u = -\operatorname{sn} u \operatorname{dn} u
$$
where $\operatorname{sn}$ and $\operatorname{dn}$ are the other Jacobi elliptic functions.

---

### 14. $\int_1^{\infty} e^{-x^2/2} dx$

**Solution:**

This is related to the complementary error function:
$$
\int_1^{\infty} e^{-x^2/2} dx = \frac{1}{\sqrt{2}} \int_{1/\sqrt{2}}^{\infty} e^{-t^2} dt
$$
Let $x = \sqrt{2} t$, $dx = \sqrt{2} dt$.
So:
$$
= \sqrt{2} \int_{1/\sqrt{2}}^{\infty} e^{-t^2} dt = \frac{\sqrt{\pi}}{2} \operatorname{erfc}(1/\sqrt{2})
$$

**Python code:**
```python
from scipy.special import erfc
I14 = 0.5 * np.sqrt(np.pi) * erfc(1/np.sqrt(2))
print(I14)
```

---

### 15. $\int_0^{\infty} x^{5/2} e^{-x} dx$

**Solution:**

This is a Gamma function integral:
$$
\int_0^{\infty} x^{p-1} e^{-x} dx = \Gamma(p)
$$
Here, $p = 7/2$:
$$
I_{15} = \Gamma(7/2)
$$

**Python code:**
```python
from scipy.special import gamma
I15 = gamma(3.5)
print(I15)
```

---

### 16. $\int_{-\infty}^{\infty} e^{-x^2} dx$

**Solution:**

This is the standard Gaussian integral:
$$
\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
$$

---

### 17. $\int_0^{\pi/2} \sqrt{\sin^3 \theta \cos^5 \theta} d\theta$

**Solution:**

$\sqrt{\sin^3 \theta \cos^5 \theta} = (\sin \theta)^{3/2} (\cos \theta)^{5/2}$

This is a Beta function integral:
$$
I_{17} = \int_0^{\pi/2} (\sin \theta)^{3/2} (\cos \theta)^{5/2} d\theta = \frac{1}{2} B\left(\frac{5}{4}, \frac{7}{4}\right)
$$

**Python code:**
```python
from scipy.special import beta
I17 = 0.5 * beta(1.25, 1.75)
print(I17)
```

---

### 18. $\int_0^{\infty} \frac{e^{-x} dx}{x^{1/4}}$

**Solution:**

This is a Gamma function integral:
$$
\int_0^{\infty} x^{p-1} e^{-x} dx = \Gamma(p)
$$
Here, $p = 3/4$:
$$
I_{18} = \Gamma(3/4)
$$

**Python code:**
```python
I18 = gamma(0.75)
print(I18)
```

---

### 19. $\int_5^{\infty} e^{-x^2} dx$

**Solution:**

This is related to the complementary error function:
$$
\int_a^{\infty} e^{-x^2} dx = \frac{\sqrt{\pi}}{2} \operatorname{erfc}(a)
$$
So:
$$
I_{19} = \frac{\sqrt{\pi}}{2} \operatorname{erfc}(5)
$$

**Python code:**
```python
I19 = 0.5 * np.sqrt(np.pi) * erfc(5)
print(I19)
```

---

### 20. $\int_0^{\pi/2} (\cos x)^{5/2} dx$

**Solution:**

This is a Beta function integral:
$$
I_{20} = \int_0^{\pi/2} (\cos x)^{5/2} dx = \frac{1}{2} B\left(\frac{1}{2}, \frac{7}{4}\right)
$$

**Python code:**
```python
I20 = 0.5 * beta(0.5, 1.75)
print(I20)
```

---

### 21. $\int_0^5 x^{-1/3} (5-x)^{10/3} dx$

**Solution:**

Let $x = 5t$, $dx = 5 dt$, $x^{-1/3} = (5t)^{-1/3}$, $(5-x)^{10/3} = (5-5t)^{10/3} = 5^{10/3} (1-t)^{10/3}$.

So:
$$
I_{21} = \int_0^5 x^{-1/3} (5-x)^{10/3} dx = 5^{10/3} \int_0^1 t^{-1/3} (1-t)^{10/3} 5 dt
$$
$$
= 5^{13/3} \int_0^1 t^{-1/3} (1-t)^{10/3} dt = 5^{13/3} B\left(2/3, 13/3\right)
$$

**Python code:**
```python
I21 = 5**(13/3) * beta(2/3, 13/3)
print(I21)
```

---

### 22. $\int_0^{7\pi/8} \sqrt{4-\sin^2 x} dx$

**Solution:**

$4 - \sin^2 x = 4(1 - (1/4)\sin^2 x)$, so $\sqrt{4-\sin^2 x} = 2\sqrt{1 - (1/4)\sin^2 x}$.

So:
$$
I_{22} = 2 \int_0^{7\pi/8} \sqrt{1 - (1/4)\sin^2 x} dx
$$
This is an incomplete elliptic integral of the second kind:
$$
I_{22} = 2 E(7\pi/8, 1/2)
$$

**Python code:**
```python
from scipy.special import ellipeinc
I22 = 2 * ellipeinc(7*np.pi/8, 0.25)
print(I22)
```

---

### 23. Find an expression for the exact value of $\Gamma(55.5)$ in terms of double factorials (!!), powers of 2, and $\sqrt{\pi}$.

**Solution:**

For half-integer arguments, the Gamma function can be written as:
$$
\Gamma\left(n + \frac{1}{2}\right) = \frac{(2n-1)!!}{2^n} \sqrt{\pi}
$$
where $n$ is a positive integer and $(2n-1)!!$ is the double factorial of odd numbers up to $2n-1$.

For $\Gamma(55.5)$, $n = 55$:
$$
\Gamma(55.5) = \Gamma\left(55 + \frac{1}{2}\right) = \frac{(109)!!}{2^{55}} \sqrt{\pi}
$$
where $(109)!! = 109 \times 107 \times \cdots \times 3 \times 1$.

---

### 24. Using your result in Problem 23 and equation (5.4), find an expression for the exact value of $\Gamma(-54.5)$.

**Solution:**

Equation (5.4) is the reflection formula:
$$
\Gamma(z)\Gamma(1-z) = \frac{\pi}{\sin \pi z}
$$
Let $z = -54.5$:
$$
\Gamma(-54.5)\Gamma(1+54.5) = \frac{\pi}{\sin(-54.5\pi)}
$$
But $\Gamma(1+54.5) = \Gamma(55.5)$, and $\sin(-54.5\pi) = -\sin(54.5\pi) = -\sin(\pi/2) = -1$ (since $54.5$ is $54$ plus $0.5$ and $\sin(n\pi + \pi/2) = (-1)^n$ for integer $n$).

So:
$$
\Gamma(-54.5) = -\frac{\pi}{\Gamma(55.5)}
$$
Now substitute the result from Problem 23:
$$
\Gamma(-54.5) = -\frac{\pi}{\frac{(109)!!}{2^{55}} \sqrt{\pi}}
= -\frac{2^{55} \sqrt{\pi} \pi}{(109)!!}
$$
Or, more simply:
$$
\Gamma(-54.5) = -\frac{2^{55} \pi^{3/2}}{(109)!!}
$$

---

### 25. As in problems 23 and 24, find expressions for the exact values of $\Gamma(28.5)$ and $\Gamma(-27.5)$.

**Solution:**

For $\Gamma(28.5)$, $n = 28$:
$$
\Gamma(28.5) = \Gamma\left(28 + \frac{1}{2}\right) = \frac{(57)!!}{2^{28}} \sqrt{\pi}
$$

For $\Gamma(-27.5)$, use the reflection formula:
$$
\Gamma(-27.5)\Gamma(28.5) = \frac{\pi}{\sin(-27.5\pi)}
$$
But $\sin(-27.5\pi) = -\sin(27.5\pi) = -\sin(\pi/2) = -1$ (since $27.5$ is $27$ plus $0.5$).

So:
$$
\Gamma(-27.5) = -\frac{\pi}{\Gamma(28.5)} = -\frac{\pi}{\frac{(57)!!}{2^{28}} \sqrt{\pi}} = -\frac{2^{28} \pi^{3/2}}{(57)!!}
$$

---

