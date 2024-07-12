---
layout: post
title: Entropy is Non-negative
author: Anthony
categories: literature
---

We need to proove that 

$$\begin{align}H(W) \geq 0 \end{align}$$

Consider two auxiliary functions,

$$\begin{align} f(x) &= log(x) \\ g(x) &= x - 1 \end{align}$$

Looking at the plots of the  two equations,
![](https://i.ibb.co/j3NgYT5/log-lin-plot.png)

Lets consider three situations, $$x = 1$$, $$x > 1$$ and $$0< x < 1$$

For $$x = 1$$,

$$\begin{align} f(x) &= log(1) \\ &= 0 \\ g(x) &= 1 -1 \\ &= 0 \end{align}
\\$$

For $$x > 1$$,  

$$\\
\begin{align} 
g(x) & \ldots \text{is increasing along with x and greater than 0} \\
f(x) &\ldots \text{is increasing, but slower than $g(x)$ but still greater than 0}
\end{align}
\\$$

For $$0 < x < 1$$, 

$$\begin{align} 
g(x) & \ldots \text{is decreasing along with x} \\
f(x) &\ldots \text{is decreasing, but faster than $g(x)$}
\end{align}$$

so,

$$\\
\begin{align} 
g(x) & \geq f(x) \ \space \ldots \text{ $\forall x > 0$}\\
x-1 & \geq log(x) \space \ldots \text{ $\forall x > 0$} \\
1-x & \leq -log(x) \space \ldots \text{ $\forall x > 0  \ldots (1)$}
\end{align}
\\$$ 

Now,

$$\\
\begin{align} 
H(W) &= - \sum_{i=1}^{W} p(w_{i}) \cdot log(p(w_{i}))\\
&= \sum_{i=1}^{W} p(w_i) \cdot (-log(p(w_{i)))}\\
&= \sum_{i=1}^{W}\underbrace{p(w_{i})}_\text{$ \geq 0$} \cdot \underbrace{(1 - p(w_{i}))}_\text{$ \geq 0$} \ldots \text{ from $(1)$}
\end{align}
\\$$
