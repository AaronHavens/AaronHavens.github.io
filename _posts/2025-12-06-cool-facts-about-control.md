---
layout: post
title: "A Necessary Stability Condition for Differentiable Autonomous Systems"
date: 2025-12-06
author: "Your Name"
tags: [control, dynamical-systems, math]
math: true
---

### (Under Construction)

Consider the differentiable function $f:\mathbb{R}^n \rightarrow \mathbb{R}^n$. Let $x^\* \in \mathbb{R}^n$ be an isolated equilibrium point. Because $x^\*$ is isolated, there exists $\varepsilon > 0$ such that for the ball $ B_{\varepsilon}(x^\*) $ centered at $x^\*$ there are no other equilibrium points. Let $ S_{\varepsilon}(x^\*) $ be the boundary of $ B_{\varepsilon}(x^\*) $. Then we can define the well-defined map

$$
f_{\varepsilon} : S_{\varepsilon}(x^*) \rightarrow S^{n-1}, \quad
x \mapsto \frac{f(x)}{\Vert f(x)\Vert}.
$$

We define the _index_ of the isolated equilibrium point $x^\*$ to be the topological degree of $f_{\varepsilon}$ around $x^\*$. Since $S_{\varepsilon}(x^\*)$ and $S^{n-1}$ are both compact smooth manifolds and $f_{\varepsilon}$ is differentiable on its domain, we can use a particular definition of degree with respect to some regular value $y \in S^{n-1}$:

$$
\text{Ind}_{x^{*}}(f) = \deg (f_{\varepsilon})
= \sum_{x\in f_{\varepsilon}^{-1}(y)}
\text{sign} \left( \det \left( \frac{\partial f_{\varepsilon}}{\partial x}\Big\rvert_{x} \right) \right).
$$

Note that because $S_{\varepsilon}(x^\*)$ is compact and $y$ is a regular value, the cardinality of $f_{\varepsilon}^{-1}(y)$ is finite. The index of a map around an equilibrium point can be useful since it provides a necessary condition for local asymptotic stability with the following statement.

<div class="theorem">
<p><strong>Theorem.</strong></p>

<p>
Consider the autonomous system
\[
\dot x = f(x)
\]
in dimension \( n \neq 4 \) with isolated equilibrium point \( x^* \).
Then \( x^* \) is locally asymptotically stable only if the index of \( f \) at \( x^* \) is \( (-1)^n \), that is
\[
\text{Ind}_{x^*}(f) = (-1)^n.
\]
</p>
</div>

This can be a useful condition to check for nonlinear systems as opposed to the sufficient Lyapunov test. However, the index is preserved under homotopy, which is a rather weak notion of equivalence. There are plenty of linear systems which are homotopic to one another but have different stability properties.

Note that the requirement of $n \neq 4$ is because we do not know yet if sublevel sets of a smooth Lyapunov function are diffeomorphic to a 3-dimensional disk. It seems likely due to Perelman's proof of the Poincaré conjecture, Wilson's theorem says that superlevel sets of smooth Lyapunov functions are diffeomorphic to $S^{n-1}$ for all dimensions. This condition can actually be removed by considering homeomorphism of trajectories ...
