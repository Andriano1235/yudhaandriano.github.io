---
title: "Solving PDF Integrals of Normal Distribution"
description: "A brief proof demonstrating that the total area under a probability density function must equal 1 to satisfy the fundamental requirement of probability theory."
pubDate: "Sep 12 2024"
heroImage: "/gauss-dist3.png"
tags: ["normal distribution","statistics"]
---

We know that a random variable distribution must satisfy the fundamental probability density function (PDF) requirements for a continuous random variable:

1. $f(x) \geq 0$, for all $x \in \mathbb{R}$

2. $\int_{-\infty}^{\infty} f(x)\,dx = 1$

3. $P(a < X < b) = \int_a^b f(x)\,dx$

These conditions ensure that the function is a valid probability model over the continuous sample space.

---

To prove that the total area under the normal distribution curve is equal to 1, we evaluate:

$$
P(-\infty < X < \infty)
=
\int_{-\infty}^{\infty} f(x)\,dx
$$

Substituting the normal distribution PDF:

$$
=
\int_{-\infty}^{\infty}
\frac{1}{\sigma\sqrt{2\pi}}
e^{-\frac{(x-\mu)^2}{2\sigma^2}}
dx
$$

---

## Standardization Transformation

Let:

$$
z = \frac{x-\mu}{\sigma}
$$

Then:

$$
x = \sigma z + \mu
$$

$$
dx = \sigma dz
$$

Substituting:

$$
=
\int_{-\infty}^{\infty}
\frac{1}{\sigma\sqrt{2\pi}}
e^{-\frac{(\sigma z + \mu - \mu)^2}{2\sigma^2}}
\sigma dz
$$

Simplifying:

$$
=
\int_{-\infty}^{\infty}
\frac{1}{\sqrt{2\pi}}
e^{-\frac{z^2}{2}}
dz
$$

$$
=
\frac{1}{\sqrt{2\pi}}
\int_{-\infty}^{\infty}
e^{-z^2/2}
dz
$$

---

## Relating to the Gaussian Integral

Recall:

$$
\int_{-\infty}^{\infty} e^{-y^2}\,dy = \sqrt{\pi}
$$

To match this form, let:

$$
y = \frac{z}{\sqrt{2}}
$$

Then:

$$
z = \sqrt{2}y
$$

$$
dz = \sqrt{2}\,dy
$$

Substituting:

$$
=
\frac{1}{\sqrt{2\pi}}
\int_{-\infty}^{\infty}
e^{-(\sqrt{2}y)^2/2}
\sqrt{2}\,dy
$$

Simplifying:

$$
=
\frac{1}{\sqrt{\pi}}
\int_{-\infty}^{\infty}
e^{-y^2}
dy
$$

Using the Gaussian integral result:

$$
=
\frac{1}{\sqrt{\pi}} \cdot \sqrt{\pi}
$$

$$
= 1
$$

---

## Final Result

$$
P(-\infty < X < \infty)
=
\int_{-\infty}^{\infty} f(x)\,dx
=
1
$$

Thus, it is proven that the total area under the normal distribution curve is exactly 1, satisfying the fundamental requirement of a valid probability density function.